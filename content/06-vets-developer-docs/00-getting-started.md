---
title: Getting Started
label: Getting Started
---

The Vets.gov Platform is broken into three parts: Vets-Website, which contains frontend applications and components that a Veteran interacts with, and Vets-API, a JSON-based API that the frontend uses to provide data to and from VA systems.

To build an Application on Vets.gov, which can be anything from a digital form to a map-based facility locator, developers will create a Frontend experience in React on Vets-Website, and connect it to an Integration on Vets-API, which manages the data flow to and from VA systems.

For forms, Vets-JSON-Schema contains shared resources used to structure and validate form data between Vets-Website and Vets-API.

Each of these parts are defined in separate open source repositories:

1. Vets-Website: https://github.com/department-of-veterans-affairs/vets-website
1. Vets-API: https://github.com/department-of-veterans-affairs/vets-api
1. Vets-JSON-Schema: https://github.com/department-of-veterans-affairs/vets-json-schema

## Onboarding

As part of the onboarding effort, you should provide your name, email address, SSH public key ([help generating one](./internal-tools-access/#requirements)), and GitHub username.

You'll be given access to the #dsva-platform-project support channel on the DSVA Slack, contributor access to all three repositories, credentials to access the shared test environments (https://dev.vets.gov, https://staging.vets.gov), and access to Internal Tools. **Your first step should be verifying that you have all of this**.

## Development

Developer documentation is split between frontend (Vets-Website) and backend (Vets-API) paths. To get started building the frontend user experience for your application, see the [Vets-Website Developer Process](./vets-website/vets-website-readme) documentation. To build the backend integration with a VA service and provide data services to the frontend of your application, see the [Vets-API Developer Process](./vets-website/vets-api-readme) documentation.

## Internal Tools

To access metrics, build logs, deployment information and exception details, please reference the [Internal Tools](./internal-tools-access) documentation.

## Questions

DSVA product and engineering resources are available to provide guidance and support through the development effort. If you encounter issues or have any questions, raise them in the #dsva-platform-project Slack channel.
