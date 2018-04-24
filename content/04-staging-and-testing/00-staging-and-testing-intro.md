---
title: Staging and Testing Introduction
label: Staging and Testing Intro
---

Process:
1. [Develop iteratively](./): guidance from 18F / USDS on how to write code iteratively, doing code reviews and checks and deploying to staging frequently.
1. [Include automated 508 tests in each deployment](./automated-testing): instructions for how to incorporate automated 508 accessibility testing as you build.
1. [Include automated unit and end-to-end tests in each deployment](../vets-developer-docs/vets-website/unit-tests): examples and instructions for how this is done on Vets.gov for reference.
1. Perform usability testing: now that you have a flow up in staging, validate what challenges and successes users have interacting with it, and determine if there are any critical changes that need to be made prior to deployment. From the Discovery section, reference these resources:
  - <a href='https://methods.18f.gov/discover/' target="blank">Choose a research method for usability testing</a>: a list (again) of 18F's recommended Discovery methods. Browse to find a tactic that suits your projects needs at this phase, as well as instructions for how to perform that activity.
  - [Draft a usability testing plan](./draft-research-plan): a guide for thinking through what you want to validate and learn in this research, so you're prepared to make the most of your research sessions.
  - [Recruit users](./recruit-users): a guide for the kinds of channels and messaging to use when looking for Veterans, their family members, VSOs, or other potential users to talk to.
  - [Talk with users and stakeholders](./talk-with-users-and-stakeholders): tips on how to conduct research sessions.
  - [Synthesize your usability testing findings](./synthesize-your-findings): a template for presenting your findings in a way that's relevant for those making product or feature decisions.
1. [Perform end-to-end QA testing](./qa): a guide for making sure you catch bugs in staging across many devices and browsers.
1. [Set up analytics](../vets-developer-docs/google-analytics): examples of how analytics are set up on Vets.gov for reference.
1. [Load test your app](./): a guide for making sure your app can handle the anticipated request load without breaking.
