---
title: Guide to Launch a Product on Vets.gov
label: Guide to Launch a Product
---
## Define, Design, and Build the form:

1. [Define the project and requirements](jump link to Define section)
2. Email **Angela Gantt-Curtis** and **Marvoureen Dolor** to get the green light to start building **Required**
3. [Design the form](jump link to Design section), referring to the various [design components](jump link) to see what you may want to use for the various form interactions.
  - [Form samples to look at before you get started - both schema, FE, any design system components that make sense]
4. Email ATO documentation to Vets.gov Privacy and ATO Officers **Required**
  - If using an existing API, there&#39;s a certain amount of ATO already in place. The additional things you&#39;d need to get in place to be covered are:
    - Add a new section to [System Security Plan](link?)
      - [Examples / how to]
    - Add new fields to the [PIA and PTA docs](link?)
      - [Examples / how to]
    - If there&#39;s a new connection involved, then you&#39;ll need an MOU
      - [Examples / how to]
    - [Where to link to this info, right now it&#39;s vets-ato, can they access that?]
5. Slack the Platform team to kick off implementation activities **Required**
  - Include link to description in vets-contrib including
    - What problem the feature is solving
    - What the feature will do
    - What data it will consume, and from what APIs
    - Whether it will submit data to any APIs and what data
  - Include names and contact info for engineering support to be included in pager duty
  - Storage and connection configurations will get spun up
  - There will likely be questions about architecture and data review needed at this point to set up infrastructure, so you can expect an app walkthrough meeting that the Platform team will coordinate.
  - **NOTE**: at this time, any features that require custom storage within vets-api are not supported (to avoid data migrations or new tables). In the next iteration of this documentation, we hope to provide an approach allowing for this.*
6. Create your own branch off of vets-json-schema **Required**
  - [Reference this schema development guide to ensure your PR will pass the various merge requirements](link to doc enumerating schema details...)
  - This is for the back-end: set up the form schema there to incorporate into your form
  - This is for the basic structure for submission to the API and contains some required fields and some basic validation
  - Use common definitions for schema elements
7. Create your own branch off of vets-website **Required**
  - [Reference this front-end development guide to ensure your PR will pass the various merge requirements](link to doc enumerating details from Jeff)
  - This is where you&#39;ll build the front-end of the form
  - This is where you&#39;ll incorporate most of the validation and conditional fields
  - Use this [Yeoman form generator](https://github.com/department-of-veterans-affairs/generator-vets-website) to create a React skeleton for the form on your new vets-website branch **Required**
8. Create your own branch off of vets-api that takes in the form data and saves it **Required**
  - Reference this [back-end development guide](need link from James) to ensure your PR will pass the various merge requirements
  - This normally will happen in parallel with the vets-website build
9. Slack the Platform team to add your URL to the server config **Required**
  - By default, the app will be password protected in dev, staging, and production (though remember the page won&#39;t exist in production because of the production:false flag).
10. Build your app by submitting PRs iteratively to have code merged to master **Required**
  - Submit PRs for vets-json-schema, vets-website, and vets-api when you&#39;ve completed enough code that you&#39;re ready to start verifying your progress in staging.
    - If the PRs are related to or dependent on each other, make sure they reference each other
    - Use [WIP] in your PR titles if you have a PR open but aren&#39;t ready for it to be reviewed and merged to master.
    - Request a Review from [who? how?]
    - [Naming convention or label needed]
    - **RISK:** since other teams don&#39;t use our same tracking system (Rational vs GitHub), we won&#39;t be able to have context for code reviews. We&#39;ll be limited to checking architecture, regression testing, and code cleanliness.
  - You'll get a code review from the digital service team for each PR you merge
    - Reviewer will perform a code review: [https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Code%20Review%20Norms.md#specific-questions-to-ask-when-code-reviewing](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Code%20Review%20Norms.md#specific-questions-to-ask-when-code-reviewing)) including things like regression testing, checking code style, unit test coverage, etc.
    - Expect some collaborative conversation with the Reviewer as this is underway
    - An accessibility review will be a part of this too.
  - Once approved, your PRs will be merged into master, and your app will be deployed to the Dev and Staging environments
    - Note: by default, all forms built using the Form Generator will have a gate on them to prevent the application from appearing in production
    - **RISK:** right now, the team building this could remove the production:false flag on their own if they wanted to (i.e. without the app going through the proper reviews etc). Do we want to prevent that systematically, or not?
    - **NOTE:** may want to consider moving to a fork model long term, while just putting a cap on the volume of app builds in the short term so that it can be handled in the manner described here.
    - QUESTION: do we want to set up GitHub roles for non-DS teams such that they don&#39;t have Review or Approve access? Not sure if it&#39;s possible…
  - If you have static content to support the app, add it to the [ignore list] ( [https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114](https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114) ), which will automatically be prevented from building in production.
  - **Rachael ^ add something about also not including nav for the static content until go live**
  - Continuously perform 508 testing (jump link)
11. When it&#39;s robust enough, perform [usability testing](jump link)
12. Send a [product guide](link to template) to the **Call Center or Aubrey??** so they can prepare their scripts and train their teams

## Launch Your Form!

1. Slack the platform team to schedule a launch review **Required**
  - Include load testing specs in the request
  - This review will consist of a screenshare walkthrough of your app to check:
    - **i.** General architecture review
    - **ii.** Interface documentation overview
    - **iii.** Authentication and authorization checks
    - **iv.** Confirmation of data scoping
    - **v.** Checks for adequate logging
    - **vi.** Appropriate external service request patterns
    - **vii.** Rate limiting requirements
  - Make any updates that are needed from your review
2. Schedule walkthrough with VA&#39;s 508 Office
  - And check to make sure the automated tests are running properly
  - Make any updates required by 508 office
3. Slack the QA team to schedule testing **Required**
  - **Note:** how can we actually understand the business requirements enough to be responsible for QA? But at the same time, how can we ensure that good quality apps are being launched if we entrust QA in a separate team?
4. Slack Platform team to enable vets-api **Required**
5. Set launch criteria
  - How will you know that you&#39;re ready for soft launch?
  - How will you know that you&#39;re ready for hard launch?
6. Submit PR for Soft Launch **Required**
  - Remove the production:false flag from the application itself
  - **Rachael add somewhere above: don&#39;t do navigation changes yet**
  - Your form will now be available in production, password protected, with no navigation and supporting static content hidden
  - Pre-launch code review includes a few extra elements:
    - Check for 508 automated tests
    - Verify that e2e tests exist
    - Verify that unit test coverage is satisfactory on FE (BE is checked automatically)
    - Verify that the launch review is good to go
  - LONG TERM:** would like feature flags to be able to hide navigation-related menu items and static content.
7. Perform User Acceptance Testing(jump link to section above)
8. Check that analytics and monitoring are working properly
9. Confirm that Call Center is ready to handle the new traffic to this tool
10. Slack Platform team to have password removed **Required**
  - Include links to your PRs from here so that Platform team can coordinate this happening at the same time as your Hard Launch PRs.
  - This step will allow your link to be visible to Google in the site map, so users may find it and use it, even if there's no navigation to it from the live site itself.
11. Submit PR for Hard Launch **Required**
  - Remove static content from the [ignore list]( [https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114](https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114) )
  - Add navigation to static content and the app
  - [What to call this bc Launch Prep PR isn&#39;t right. Labels / title standards to apply so we know it&#39;s the finished product?]
  - **Note:** prior to merge, double check that the password has been removed


## Samples
- Sample Health Care Application (Form 10-10EZ) [https://www.vets.gov/health-care/apply/application/veteran-information/personal-information](https://www.vets.gov/health-care/apply/application/veteran-information/personal-information)

- Sample Health Care Application (Form 10-10EZ) schema: [https://github.com/department-of-veterans-affairs/vets-json-schema/blob/master/src/schemas/10-10EZ/schema.js](https://github.com/department-of-veterans-affairs/vets-json-schema/blob/master/src/schemas/10-10EZ/schema.js)

- Sample Health Care Application (Form 10-10EZ) front-end: [https://github.com/department-of-veterans-affairs/vets-website/tree/master/src/applications/hca](https://github.com/department-of-veterans-affairs/vets-website/tree/master/src/applications/hca)


### What happens when there&#39;s an error in production? And is our call center process (i.e. Aubrey) supporting these apps?
[To be filled out later]
