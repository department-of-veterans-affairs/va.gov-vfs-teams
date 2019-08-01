# Product development checklist

Status: **DRAFT** / not official

---

# 1. Read through these things and understand how to work with VSP to design and build things on VA.gov.

### Content
- [Here are the best practices on writing great, plain language content on VA.gov](https://design.va.gov/content-style-guide/)
- You'll need reviews from VSP to help you make sure you're on track! [Here's what to expect, and how to request a content review](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/Practice%20Areas/Content/content-review-process.md)

### IA
- [Here are the best practices on writing URLs](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Information%20Architecture/URL%20Creation%20Process%20and%20Guidelines.md).
- You'll need check ins with VSP to help you make sure you're on track! Reach out to #vfs-platform-support in Slack to schedule a 1:1 with us so we can decide on your cadence for IA check ins.

### Design
- [Here's how to create great user-centered designs for VA.gov solutions](https://design.va.gov/documentation/designers).
- You'll need reviews from VSP to help you make sure you're on track! [Here's what to expect, and how to request a design review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-design-qa.md)

### Engineering
- [Here's how to write great FE code for VA.gov solutions](https://department-of-veterans-affairs.github.io/veteran-facing-services-tools/).
- [Here's how to write great BE code for VA.gov solutions](https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Practice%20Areas/Engineering/Backend).
- You'll need frequent (usually around weekly) code reviews from VSP to hep you make sure you're on track! [Here's what to expect, and how to request a code review](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/Practice%20Areas/Engineering/code_review_guidelines.md)

### Product
- [Here's how to write a great Product Outline](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Product/ProductOutline.md).
- We are undergoing some repository construction, so this may change in the future, but for now please store your VA.gov Product documentation in the [vets.gov-team repo product folders](https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Products).
- [Here's how to use ZenHub to manage your projects](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Onboarding/zenhub_product_management.pdf)

### 508
- [Here's how to write and test FE code for 508 Accessibility](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Onboarding/508-accessibility-best-practices.md)
- You'll need reviews from VSP to help ensure accessibility of your solutions! [Here's what to expect, and how to request a 508 review](/)

### Analytics
- [Here's how to set KPIs to track the success of your VA.gov solutions](/)
- [Here's how to incorporate analytics into your VA.gov solutions](/)
- VSP is here to help you as you set up analytics in your code. [Here's how to request Analytics support](/)
- You'll need reviews from VSP to help you make sure you're on track! [Here's what to expect, and how to request an Analytics review](/)

### QA

- [Here's how to QA your solutions](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/QA/How%20To%20Coordinate%20QA%20Testing.md)
- [Here's how to incorporate QA testing in development](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/tree/master/DeveloperDocs/testing)
- VSP is here to help you as you test to ensure your solutions are top quality! Reach out to #vfs-platform-support in Slack to ask questions, or schedule a meeting with us so we can help when you need it.

### ATO
- You'll need to ensure the solution you're building has the authority to operate (ATO). [Here's what to expect, and how to request an ATO review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-ato-reviews.md)

- [ ]   Release plan review
    *   Review release phases and criteria for moving between them. This should include rollout schedule, success/rollback criteria, any pre- and post-launch user testing and monitoring, external documentation and comms.
- [ ]   [IA review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-ia-review.md)
    *   Should include review of URLs, navigation hierarchy, crosslinks/redirects, SEO
- [ ]   Security review
    *   Review looking for potential technical security issues / vulnerabilities, focusing particularly on frontend-backend interactions, anything involving certificates or cookies, and any new interactions with dependent backends.
- [ ]   Privacy review
    *   Review looking for potential user data issues, including affirming best practices around handling PII.
- [ ]   Production readiness / infrastructure review
    *   Review of technical architecture, looking for potential scaling concerns, dependency analysis, SLO assessment

---

# 2. Build, Measure, Learn! As you go, each of these items represent work that must be completed and signed off on by VSP before a new application launches.

These processes are here to help ensure we're launching features that are:
* in line with VA.gov's standards for design, UX, reliability, and availability
* maintainable over time
* have measurable analytics and success metrics to empower future planning and development

## Launch reviews

Each of these reviews MUST be scheduled with the appropriate VSP contact, and completed by VSP before application launch.

- [ ]   [Accessibility / 508 review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-508-review.md)
- [ ]   [ATO review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-ato-reviews.md)
- [ ]   [Content QA](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-content-qa.md) / review(?)
- [ ]   [Design QA](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-design-qa.md) / review(?)
- [ ]   Analytics / Product Health Report review
    *   Reviewing analytics that will be used to just the product health / success, and making recommendations as appropriate.
- [ ]   Release plan review
    *   Review release phases and criteria for moving between them. This should include rollout schedule, success/rollback criteria, any pre- and post-launch user testing and monitoring, external documentation and comms.
- [ ]   [IA review](https://github.com/department-of-veterans-affairs/va.gov-vfs-teams/blob/master/Request-Reviews/request-ia-review.md)
    *   Should include review of URLs, navigation hierarchy, crosslinks/redirects, SEO
- [ ]   Security review
    *   Review looking for potential technical security issues / vulnerabilities, focusing particularly on frontend-backend interactions, anything involving certificates or cookies, and any new interactions with dependent backends.
- [ ]   Privacy review
    *   Review looking for potential user data issues, including affirming best practices around handling PII.
- [ ]   Production readiness / infrastructure review
    *   Review of technical architecture, looking for potential scaling concerns, dependency analysis, SLO assessment
    
## Other launch requirements

These are other launch requirements that don't have formal reviews but also MUST be completed before launching.

- [ ]   Documentation for quickly addressing when things go wrong
    - [ ]   Contacts for oncall support: who do we contact if the application is failing? What kinds of failure modes are likely?
    - [ ]   Documentation and points of contact for any new backend dependencies
    - [ ]   Links to important dashboards for investigating relevant issues
- [ ]   No high-severity bugs present
- [ ]   Testing requirements
    - [ ]   E2e tests, running in CI/CD, passing on all browsers
    - [ ]   Code coverage requirements
    - [ ]   Load testing
- [ ]   Monitoring requirements
    - [ ]   Contact (mailing list? Slack channel?) for errors to be reported to
    - [ ]   Errors getting sent directly to team
- [ ]   Contact center(s) are prepared for this launch, with updated scripts/documentation as needed
- [ ]   VA web comms team is aware of this launch and has accurate messaging
- [ ]   Product Outline w/critical criteria up-to-date
- [ ]   Tested in prod with VA back-of-house people and systems
- [ ]   Entrance pages (i.e. supporting static content) in place
- [ ]   Downtime UX and error messaging documentation complete
- [ ]   "Learn and Improve" plan written: KPI measurements, analytics reporting, next phase of features to build
