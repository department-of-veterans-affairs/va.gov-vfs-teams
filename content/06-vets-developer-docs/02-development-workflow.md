---
title: Development Workflow
label: Development Workflow
---
## Pull Requests

New features are merged to the Platform through a GitHub Pull Request. Your work
is applied to a Git branch on your local system. After pushing this
branch to GitHub, you'll open a Pull Request to let other developers on the
team know that your work is ready for review and subsequent deployment.

A Platform developer will perform a [Code
Review](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Code%20Review%20Norms.md)
and provide feedback on your changes. Once addressed, the reviewer will Approve
the Pull Request and the changes can be merged to master.

To gather comments and informal review during development, a Pull Request may
be titled with a "[WIP]" prefix. This indicates that the Pull Request is
a "Work in Progress", and should not be considered a candidate for merge.

Further Reading:

* https://git-scm.com/book/en/v2/Getting-Started-Git-Basics
* https://help.github.com/articles/github-flow/

TIP: Prefix your branch name with your team's initials for improved management.

## Review Instances

Open Pull Requests are automatically deployed to an isolated "Review Instance"
in the Vets.gov's development environment. A "View deployment" button on
the Pull Request page will provide the instance address. This can be
particularly useful for [WIP] testing and review.

Further Reading:
* [Review Instances](./review-instances)

## Automated Testing

Each Pull Request is automatically tested within the Platform's CI environment.
This testing includes unit tests, integration tests, security scans, coverage,
and code style checks. If any tests fail, the Pull Request cannot be merged.

These tests can be run locally on your system with `$ make ci`.

While our automated tests are extensive, they are not expected to catch all
issues. The manual Pull Request review process is carefully and completely
executed for all changes.

## Deployment

Once a Pull Request is merged, changes will be deployed to the development and
staging environments. These can be previewed at https://dev.vets.gov/ and
https://staging.vets.gov/, respectively. Changes are then deployed to
production Monday through Friday at 3:00PM ET.

Further Reading: (TODO migrate to contrib):

* [Deployment](./deployment)

## Security Considerations

The Vets.gov code base is public, but deployed to and hosted on heavily secured
infrastructure with connectivity to the VA network. Code is expected to
follow industry-standard best security practices, and never relies on secuirty
by obscurity. Refer to the [Settings](./vets-api/settings) to learn how to access
private information / secrets that are required by your integration when
running in a protected environment.

While the automated security scanning referenced above offers some protections,
it is not a substitute for an understanding of common best practices and web
security. Reviewers will work to catch security issues before they are
introduced, but please ensure that you are familiar with common
vulnerabilities and general security best practices before building an
integration.

Further Reading:

* https://en.wikipedia.org/wiki/Security_through_obscurity
* https://martinfowler.com/articles/web-security-basics.html
* https://www.owasp.org/index.php/Main_Page
* https://www.powerdown.io/blog/posts/stories/web-developer-security-checklist.html

<!-- Next Button -->
<a href='./internal-tools-access'><div class="next-button"><h5 class="next-text">Next: Internal Tools Access</h5></div></a>
