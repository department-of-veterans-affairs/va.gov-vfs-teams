# Getting Started


To build a service on the Veteran Tools Platform, which can be anything from a digital form to a map-based facility locator, developers will create a Frontend experience in React on Vets-Website, and connect it to an Integration on Vets-API, which manages the data flow to and from VA systems.

<hr>

* [Get started](#get-started)
* [Development](#development)
* [Get help](#get-help)

<hr>

## Get started

1. Confirm that your team's Project Manager has added your name, email address, and Github username to the team spreadsheet and sent it to DSVA. You'll know when you can visit [this Github repo and see the content](https://github.com/department-of-veterans-affairs/vets.gov-team).

1. Follow the steps to [create new SSH keys, configure, and test the SOCKS proxy](../External-Contractors-Onboarding/request-access-to-tools.md#additional-onboarding-steps-for-developers).

1. Verify that you have

  * Have access to the [Veteran Tools Platform code repositories](#code-repositories)

  * Have credentials for the shared testing environments &mdash;  [dev.vets.gov](https://dev.vets.gov) and [staging.vets.gov](https://staging.vets.gov).

  * Have access to [Internal Tools](internal-tools-access.md)

  * **Tip**: If you have a problem or can't get access, post in the *#support-external* Slack channel or reach out to your DSVA contact.

1. Review all the content the External-Contractors-DeveloperDocs section (everything after this page).

1. Review the frontend documentation for [Vets-Website](vets-website/README.md).
<br/><br/>

1. Review the backend documentation for [Vets-API](vets-api/README.md).

<hr>

## Development

#### Code repositories

The Veteran Tools Platform is broken into three parts:

1. [Vets-Website](https://github.com/department-of-veterans-affairs/vets-website), which contains frontend applications and components users interact with

2. [Vets-API](https://github.com/department-of-veterans-affairs/vets-api), a JSON-based API used by the frontend to provide data to and from VA systems

3. [Vets-JSON-Schema](https://github.com/department-of-veterans-affairs/vets-json-schema), which contains shared resources used to structure and validate form data between Vets-Website and Vets-API.


#### Internal Tools

To get access to metrics, build logs, deployment information and exception details, see [Internal Tools Access](internal-tools-access.md) documentation.

<hr>

## Get help

DSVA engineering resources are available to provide guidance and support through the development effort.

If you encounter issues or have any questions, raise them in hte *#support-external* Slack channel, or reach out to your DSVA contact.

<hr>

[Next: Environments](environments.md)

[Back: Developer Docs Introduction](README.md)
