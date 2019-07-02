# Day Three VSP Onboarding Meeting
The purpose of this document is to determine what items we need on Day Three to be productive. This could include things we want to know about the onboaring team, and things we want the onboarding team to provide during discussion.

## TODO Items to Iterate On
* Create templates for adding points of contact, project specifics
* Create a meeting notes template for Day Three discovery
* Define logistics of the day. Is this a one-hour meeting, is it all-day? What's the breakdown?

## Before Day Three Meeting
These are the items that need to be completed before the Day Three meeting(s). Having these items finished will make Day Three go smoothly and help teams learn more in discovery.

### What might the VSP team need to do one time?
* Create one to two templates for adding points of contact, project specifics
* Create a meeting notes template for Day Three meetings
* Define testing expectations (unit, e2e, integration, visual regression)
* Create a walkthrough for manual accessibility testing
* Create an axe e2e proof of concept
	* Nightwatch
	* Selenium
	* Test Cafe
	* other examples?

### What does the onboarding team need to do in advance?
* Fill out the intake questionnaire
* Identify team members who will be first point of contact
	* Product
	* Content
	* Information Architecture
	* Design
	* Development (could be front-end and back-end)
* Identify project scope
	* Greenfield or existing project
	* Goals and desired outcomes
	* Key performance metrics
* Identify project requirements
	* Requirements document
	* Congressional mandate
	* Soft deadlines
	* Hard deadlines
	* Planned promotional or marketing efforts
* Identify work in progress
	* Content / IA
	* Design
	* Development (front-end or back-end)

### What does the VSP team need to do in advance for every team?
* Review the intake questionnaire
* Start a project folder and related documents in Github TODO: Find a home for this
	* Points of contact
	* Project scope, requirements, work in progress

## Day Three Discovery Meeting
These goals and top-level sections are items we would want to discuss with the onboarding team. We want to discover as much as we can through question and answer sessions. By the end of the day, we should be writing tickets so the project team can get started with a clear set of next steps.

### Goals
* Ensure VSP understands the project parameters
* Write actionable tickets, so the onboarding team can start moving

### Getting Started
Review the project folder and related documents. Make sure onboarding team and VSP team have correct and complete information.

### Content & Information Architecture
* Review site architecture changes
* Review content strategy or copy

### Designs
* Review any designs in progress
	* Mobile, responsive
	* Design system

### Front-end Development
* Identify familiarity with Formation (design system)
* Review any code in progress
	* Any integration points for design system?
	* Helpers needed or missing
* Discuss testing strategies and expectations

### Back-end Development
* Identify integration points
	* Login flow
* Identify APIs required for the product to work
	* Existing API, or new integration?
	* Documentation
	* Endpoints needed
	* Methodology (REST, GraphQL)

### Accessibility
* Demo manual accessibility testing
	* [aXe plugin](https://deque.com/axe)
	* [keyboard testing](https://webaim.org/techniques/keyboard/)
	* [zoom testing](https://w3c.github.io/wcag21/understanding/21/reflow.html)
* Demo integrating axe.js into e2e pipeline

