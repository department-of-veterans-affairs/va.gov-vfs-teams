# This file is deprecated. The most recent information should be at https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/platform/design/working-with-platform-design-team.md

# UX/IxD/UI and Visual Design

### General

* **All teams working on the Veteran-facing Services Platform are required to follow the guidelines and patterns in the [Veteran-facing Services Platform Design System](https://department-of-veterans-affairs.github.io/design-system/).**
* **VFS teams should schedule the Design QA when the complete and final build is on staging.**
  * The Design QA should happen when the team is confident no further changes will happen before launch.

### Request a Design QA

1. File an issue in ```va-team repo```.
    * Title: ```Request Design QA```
    * Labels:
      * ```design```
      * ```product support```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```Andrea Hewitt```
    * Comment: Include the following information:
      * **Context:** Provide context for your team's project.
        * e.g., ```Functionality adds a new dataset to the Facility Locator so users can search for and view non-VA health providers on the map, as well as in list and detail views.```
      * **URL:** ```link to your project on staging```
      * **New Design Patterns (if any):** Note the places where you've created and used new design patterns (if any)
      * **Design Challenges (if any):** Note any unusual or tricky design problems you needed to solve in this work
      * TODO - provide an example here.
1. **Within 4 business days**, VSP will conduct a Design QA using the [Checklist below](#design-qa-checklist).
    * If you don't hear anything after 4 business days, reach out to your DSVA Contact.
1. VSP will update the Github issue with screenshots to show where design needs to be changed.
1. Complete all the changes requested in the screenshots.
    * If your team has questions (or disagrees with a requested change), use the Github issue to discuss that with DSVA and VSP.
1. When all changes are completed, close the issue.
1. When the issue is closed, this pre-launch activity is considered complete.

### Design QA Checklist

* [ ] New design patterns have been vetted by DSVA and documented
* [ ] Mobile, tablet, and desktop breakpoints have been accounted for
* [ ] Correct use of design patterns in context
  * [ ] Form chapters in place
  * [ ] Privacy policy is present
  * [ ] Address form follows pattern if applicable
  * [ ] Name form follows pattern if applicable
* [ ] Correct use of typography
* [ ] Padding and spacing has been applied appropriately
* [ ] Form components used correctly in context
* [ ] Consistent use of iconography
* [ ] Colors use are consistent with color palette
* [ ] Primary and secondary CTA buttons used correctly in context
* [ ] :hover and :focus states have been accounted for and are consistent with design patterns
* [ ] Alert messages have been used appropriately
* [ ] Error states have been accounted for and used appropriately
* [ ] Loading indicators have been used where appropriate
