# Contact Center
* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

  * *"External contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>

* [General](#general)
* [Prepare for a Contact Center review](#prepare-for-a-contact-center-review)
* [Request a Contact Center Review](#request-a-contact-center-review)

<hr>

### General

* All applications on the Veteran Tools Platform include a phone number Veterans can call to ask questions about the application's functionality.
* **Before applications (or new features) launch on the Veteran Tools Platform, all teams must review functionality with the Contact Center to ensure that Contact Center Representatives are prepared to answer questions about the functionality.**
  * This meeting will be arranged and facilitated by DSVA.
* **External Contractor teams should initiate the Contact Center Review when** 
  1. The complete and final build is on staging,
  1. After they've completed the [Prepare for a Contact Center Review steps](#prepare-for-a-contact-center-review), and
  1. At least 2 weeks prior to the launch date.
    * If your team thinks it will have trouble meeting the "2 weeks prior to launch" date, reach out to your DSVA Contact to determine how to move forward.

<hr>

## Prepare for a Contact Center Review

### Step 1: Create the Product Guide

* <a href="https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/Templates/sample-product-guide-1.pdf" target="_blank">Example Product Guide 1</a>
* <a href="https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/Templates/sample-product-guide-2.pdf" target="_blank">Example Product Guide 2</a>

*If you're building a brand new service*:

  1. Create a Product Guide that covers all the functionality, the main user flow(s), any error conditions, and how the user can resolve those errors.
  1. Store the Product Guide in your team's Product folder on Github in a new folder called ```Contact Center.```

*If you're building new features for an existing service*:

  1. You'll need to update the existing Product Guide.
      * If you can't find the existing Product Guide on Github, ask your DSVA Contact to find it for you.
  1. Store the updated Product Guide in its original location.


### Step 2: Create the Product Video

*For new services and updates to existing services*:

  1. Create a Product Video (with audio) that steps through the primary user flows.
  1. Store the Product Video in the same folder as the Product Guide.  

<hr>

## Request a Contact Center Review

1. File an issue in ```vets-team repo```.
    * Title: ```Request Contact Center Review```
    * Labels:
      * ```call center```
      * ```external-request```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Comment: Include the following information.
      * **Context**: Provide a high-level description of the functionality for which you're requesting this review, for example:
        * ```Functionality adds a new dataset to the Facility Locator so users can search for and view non-VA health providers on the map, as well as in list and detail views.```
      * **URL**: ```link to your project on staging```
      * **Product Guide**: ```link to the Product Guide on Github```
      * **Product Video**: ```link to the Product Video on Github```
      * **Contact Person**: Provide the name, email address, and Slack username for the person on your team who schedules meetings, e.g., your Project Manager.

1. **Within 2 business days**, DSVA will contact the Contact Person (the person who created the Github issue) to arrange a day/time for the Contact Center Review meeting.
    * If you don't hear anything after 2 business days, reach out to your DSVA Contact.
    * Plan for some back and forth in the Github issue to find a day/time that works for your team and the Contact Center team.
1. At the Contact Center Review meeting, your team will demo the functionality for the Contact Center Representatives and answer any questions they may have about the functionality.
1. At the end of the Contact Center Review meeting, DSVA will close the Github issue.
    * Github will send the Contact Person (the person who created the Github issue) a notification. This is your team's signal that this pre-launch activity is complete.
