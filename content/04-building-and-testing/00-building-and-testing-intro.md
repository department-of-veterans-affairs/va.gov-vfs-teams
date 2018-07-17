---
title: Building and Testing Introduction
label: Build and Test Intro
---

Process:
1. [Start developing](../vets-developer-docs/getting-started): develop iteratively, code locally and deploy to staging as you go. Reference the Vets.gov workflow as an example.
1. Include automated testing in each deployment: here are examples and instructions for how this is done on Vets.gov for reference.
  - [Automated 508 accessibility tests](./automated-testing)
  - [Automated unit and end-to-end tests](../vets-developer-docs/vets-website/forms/tests)
1. Perform usability testing: now that you have a flow up in staging, validate what challenges and successes users have interacting with it, and determine if there are any critical changes that need to be made prior to deployment. Here are resources from the Discovery section for reference:
  - <a href='https://methods.18f.gov/discover/' target="blank">Choose a research method for usability testing</a>
  - [Draft a usability testing plan](../discovery/draft-research-plan)
  - [Recruit users](../discovery/recruit-users)
  - [Talk with users and stakeholders](../discovery/talk-with-users-and-stakeholders)
  - [Synthesize your usability testing findings](../discovery/synthesize-your-findings)
1. [Perform end-to-end QA testing](./qa): a guide for making sure you catch bugs in staging across many devices and browsers.
1. [Set up analytics](../vets-developer-docs/google-analytics): examples of how analytics are set up on Vets.gov for reference.
1. [Load test your app](./): a guide for making sure your app can handle the anticipated request load without breaking.
