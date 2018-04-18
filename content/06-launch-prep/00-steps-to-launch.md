---
title: Steps to Launch
label: Steps to Launch
---
You're almost ready to launch your new app! Here is a step by step guide to get you over the finish line:

1. Slack the platform team to schedule a launch review <span style="color: red; font-weight:bold;">Required*</span>
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
3. Slack the QA team to schedule testing <span style="color: red; font-weight:bold;">Required*</span>
  - **Note:** how can we actually understand the business requirements enough to be responsible for QA? But at the same time, how can we ensure that good quality apps are being launched if we entrust QA in a separate team?
4. Slack Platform team to enable vets-api <span style="color: red; font-weight:bold;">Required*</span>
5. Set launch criteria
  - How will you know that you&#39;re ready for soft launch?
  - How will you know that you&#39;re ready for hard launch?
6. Submit PR for Soft Launch <span style="color: red; font-weight:bold;">Required*</span>
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
10. Slack Platform team to have password removed <span style="color: red; font-weight:bold;">Required*</span>
  - Include links to your PRs from here so that Platform team can coordinate this happening at the same time as your Hard Launch PRs.
  - This step will allow your link to be visible to Google in the site map, so users may find it and use it, even if there's no navigation to it from the live site itself.
11. Submit PR for Hard Launch <span style="color: red; font-weight:bold;">Required*</span>
  - Remove static content from the [ignore list]( [https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114](https://github.com/department-of-veterans-affairs/vets-website/blob/master/script/build.js#L114)
  - Add navigation to static content and the app
  - [What to call this bc Launch Prep PR isn&#39;t right. Labels / title standards to apply so we know it&#39;s the finished product?]
  - **Note:** prior to merge, double check that the password has been removed
