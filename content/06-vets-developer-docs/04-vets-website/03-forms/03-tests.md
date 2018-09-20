---
title: Writing Tests
label: Tests
---

### The content for this page has been migrated to the <a title="go to VA Digital Service Handbook" href="https://github.com/department-of-veterans-affairs/vets-work-practices/tree/master/Testing" target="_blank">work-practices repo</a>.
* <a title="go to VA Digital Service Handbook" href="https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/Testing/unit-testing.md" target="_blank">Unit Testing</a>.
* <a title="go to VA Digital Service Handbook" href="https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/Testing/end-to-end-testing.md" target="_blank">End-to-End Testing</a>.


<!--
We have two types of testing for forms, and code on Vets.gov in general: unit tests and end-to-end tests.

## Unit tests

As you build your form, you should be writing unit tests to make sure your form is behaving as you expect and to help guard against future bugs. We typically follow a pattern of creating a unit test file for each page in a form and testing the following scenarios:

- That the correct number of inputs show up when you render the page
- That the correct number of fields display validation errors if you submit without entering any information
- That any conditional logic on the page displays under the correct conditions

We have some helper utilities to make writing tests a little bit easier. Tests should go in a `tests` folder in your application folder. Here's an example unit test that would live at `src/applications/vic-v2/tests/config/veteranInformation.unit.spec.jsx`:

```js
import React from 'react';
import { expect } from 'chai';
import sinon from 'sinon';
import { mount } from 'enzyme';

import { DefinitionTester, fillData, selectRadio, fillDate } from '../../../../platform/testing/unit/schemaform-utils.jsx';
import formConfig from '../config/form.js';

describe('VIC veteran information', () => {
  const { schema, uiSchema } = formConfig.chapters.veteranInformation.pages.veteranInformation;
  it('should render', () => {
    const form = mount(
      <DefinitionTester
        definitions={formConfig.defaultDefinitions}
        schema={schema}
        data=\{{}}
        uiSchema={uiSchema}
        />
    );

    expect(form.find('input').length).to.equal(7);
    expect(form.find('select').length).to.equal(4);
  });

  ...
});
```

We've done some basic test set up at the top and also imported some helpers from `schemaform-utils.jsx`. The most important item in that list is `DefinitionTester`, which is a component we use to simulate a page being rendered, without having to set up a whole form application with all the dependencies. We write unit tests with [Enzyme](http://airbnb.io/enzyme/) and mount a `DefinitionTester` component that is passed in the schema information from our `veteranInformation` page as props. Then, we check to make sure that we have 7 `input`s and 4 `select`s on the page. When there are errors with definitions on our form pages, you will often see inputs not being rendered, so this helps check for that scenario.

It's also worth nothing that these aren't strictly "unit" tests, they're better described as integration tests that may execute multiple components and functions in our forms code. However, we run them using the same stack as our unit tests, so we generally refer to them as such.

The next test in the file checks to see that we have the right fields marked as required:

```js
  it('should not submit without required info', () => {
    const onSubmit = sinon.spy();
    const form = mount(
      <DefinitionTester
        onSubmit={onSubmit}
        definitions={formConfig.defaultDefinitions}
        schema={schema}
        data=\{{}}
        uiSchema={uiSchema}
        />
    );

    form.find('form').simulate('submit');

    expect(form.find('.usa-input-error').length).to.equal(6);
    expect(onSubmit.called).to.be.false;
  });
```

In this test, we simulate a form submission, then count the number of error elements on the page, which is expected to be 6. This way we can make sure our existing validation rules are still generally in place and that we haven't accidentally added another one.

Finally in this file we fill in all the data and submit:

```js
  it('should submit with all info filled in', () => {
    const onSubmit = sinon.spy();
    const form = mount(
      <DefinitionTester
        onSubmit={onSubmit}
        definitions={formConfig.defaultDefinitions}
        schema={schema}
        data=\{{}}
        uiSchema={uiSchema}
        />
    );

    fillData(form, 'input#root_veteranFullName_first', 'test');
    fillData(form, 'input#root_veteranFullName_last', 'test2');
    fillData(form, 'input#root_veteranSocialSecurityNumber', '233224343');
    selectRadio(form, 'root_gender', 'F');
    fillDate(form, 'root_veteranDateOfBirth', '1920-01-04');
    fillData(form, 'select#root_serviceBranch', 'F');
    form.find('form').simulate('submit');

    expect(form.find('.usa-input-error').length).to.equal(0);
    expect(onSubmit.called).to.be.true;
  });
```

We have some helper functions that will make the right Enzyme calls to fill in data for us, so we don't have a lot of repeated code. Those helpers are documented in the `schemaform-utils.jsx` file. And you can see at the end we check that no errors are displayed and that our `onSubmit` prop was called, which will only happen if our data passed all of the page's validation rules.

Now that you've see these three tests, you should be able to get started writing your own tests. Testing conditional logic works as you might expect, where we use our helpers to fill in data, then check to see that the right number of inputs appear in the page after that change. Some of our tests also directly test logic in `depends` functions on the page config, since that will often not get tested elsewhere.

## End-to-end tests

End-to-end (e2e) tests are tests that run in a browser and test that a user can fill out information and progress through the form. We typically have one e2e test per form, that fills in all the information for that form and submits to a mock service.

We use [Nightwatch](http://nightwatchjs.org/), which runs on top of Selenium, to write our tests.

You should take a look at an [existing e2e test](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/applications/burials/tests/00-all-fields.e2e.spec.js) to get a sense of how they're written, but there are some basic steps to follow:

1. Set up [Redux dev tools](https://github.com/zalmoxisus/redux-devtools-extension). This will let you pull out some information from your form more easily.
2. Step through your form, filling out all the fields
3. Before submitting, open the Redux dev tools and copy out the form data object into a `schema/maximal-test.json` file in your `tests` folder:

![](/va-digital-services-platform-docs/assets/develop/images/forms/redux_dev.png)

Once you've done this, you should be all set to start. We'll step through the burials form e2e tests to see how it works:

```js
const E2eHelpers = require('../../../platform/testing/e2e/helpers');
const Timeouts = require('../../../platform/testing/e2e/timeouts');
const PageHelpers = require('./burial-helpers');
const testData = require('./schema/maximal-test.json');

const runTest = E2eHelpers.createE2eTest(
  (client) => {
    PageHelpers.initApplicationSubmitMock();

    // Ensure introduction page renders.
    client
      .url(`${E2eHelpers.baseUrl}/burials-and-memorials/application/530`)
      .waitForElementVisible('body', Timeouts.normal)
      .assert.title('Apply for burial benefits: Vets.gov')
      .waitForElementVisible('.schemaform-title', Timeouts.slow)  // First render of React may be slow.
      .click('.usa-button-primary');

      E2eHelpers.overrideVetsGovApi(client);
      E2eHelpers.overrideSmoothScrolling(client);
      E2eHelpers.expectNavigateAwayFrom(client, '/introduction');
```

Up at the top we're importing some helpers, including `./burial-helpers`, which is where most of the actual testing code lives. In the actual test function, we start up an application submit mock so that we can submit the form at the end. Then we open the form, wait for it to load, and click the Start button. There's also some set up code after that (the last three lines).

Next, we jump into testing the first page of the form:

```js
    // Claimant Information page
    client.waitForElementVisible('input[name="root_claimantFullName_first"]', Timeouts.normal);
    client.assert.cssClassPresent('.progress-bar-segmented div.progress-segment:nth-child(1)', 'progress-segment-complete');
    PageHelpers.completeClaimantInformation(client, testData.data);
    client.axeCheck('.main')
      .click('.form-panel .usa-button-primary');
    E2eHelpers.expectNavigateAwayFrom(client, '/claimant-information');
```

This is largely the same for each page; we check for an element to make sure the page has loaded, we check that the progress bar is at the right point, then we fill out the fields on the page (`PageHelpers.completeClaimantInformation`). After that, we run our accessibility checker and move on to the next page.

In our helpers file, the `completeClaimantInformation` function looks like:

```
function completeClaimantInformation(client, data) {
  client
    .fillName('root_claimantFullName', data.claimantFullName)
    .selectRadio('root_relationship_type', data.relationship.type);

  if (data.relationship.type === 'other') {
    client
      .waitForElementVisible('input[name="root_relationship_other"]', Timeouts.normal)
      .fill('input[name="root_relationship_other"]', data.relationship.other)
      // Not sure what to do with this, exactly, but I'll make it an option.
      .clickIf('#root_relationship_view:isEntity', data.relationship.isEntity);
  }
}
```

You can see that we're using the [Nightwatch API](http://nightwatchjs.org/api) and some [custom helpers](https://github.com/department-of-veterans-affairs/vets-website/tree/master/src/platform/testing/e2e/nightwatch-commands) to fill in information on the form.

You can follow the above pattern for each page in your form, and then at the end submit:

```js
    // Review and Submit Page.
    client
      .waitForElementVisible('label[name="privacyAgreement-label"]', Timeouts.slow)
      .pause(1000)
      .click('input[type="checkbox"]')
      .axeCheck('.main')
      .click('.form-progress-buttons .usa-button-primary');
    E2eHelpers.expectNavigateAwayFrom(client, '/review-and-submit');
    client.expect.element('.js-test-location').attribute('data-location')
      .to.not.contain('/review-and-submit').before(Timeouts.slow);

    // Submit message
    client.waitForElementVisible('.confirmation-page-title', Timeouts.normal);

    client.axeCheck('.main');

    client.end();
```

Here we're submitting the form on the review page and making sure the page changes to the confirmation page. At this point, you will need to fill out your `initApplicationSubmitMock` function, if you haven't yet. This is so we can simulate a successfull response from the API we're calling:

```js
function initApplicationSubmitMock() {
  mock(null, {
    path: '/v0/burial_claims',
    verb: 'post',
    value: {
      data: {
        attributes: {
          regionalOffice: [],
          guid: '1234',
          confirmationNumber: '123fake-submission-id-567',
          submittedAt: '2016-05-16'
        }
      }
    }
  });
  mock(null, {
    path: '/v0/burial_claims/1234',
    verb: 'get',
    value: {
      data: {
        attributes: {
          state: 'success',
        }
      }
    }
  });
}
```

The burial form submission process uses polling, so there are two mocked API responses, but for most forms you'll have just one. Our `mock` helper calls our mock API server and adds a mock response, so that when the form makes a request to the url at the `path` property with the `verb` action, it gets the `value` data back.
-->

<!-- Next Button -->
<a href='./submitting'><div class="next-button"><h5 class="next-text">Next: Submitting</h5></div></a>
