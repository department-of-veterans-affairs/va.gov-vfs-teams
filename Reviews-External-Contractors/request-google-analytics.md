# Google Analytics - IN PROGRESS - DO NOT USE YET

* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

  * *"External contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>

* [General](#general)
* [Prepare for Google Analytics](#prepare-for-google-analytics)
* [Request Google Analytics](#request-google-analytics)

<hr>

### General

* **All teams working on the Veteran Tools Platform are required to integrate VA's Google Analytics into their services.**
* **External Contractor teams should request Google Analytics when**
  * The complete and final build is on staging and you're confident it's ready to launch. 
  * At least 2 weeks before planned launch date

<hr>

### Prepare for Google Analytics

Answer the following questions in a Word document:

* What is the final step a user will take in their user experience?
* What steps in the user experience would you like to measure to understand progress and abandonment?
* What other user interactions, like Print or Save, are key to understanding the behavior of your users?
* What other navigation elements on the site will help you understand how your users navigate to, and use, your service?
* What success metrics have you identified for your service?
* What user interaction or behavior do you want to count as a "transaction" to track? What are your goals for each of these transactions?
* What are other events, interactions, behavior you want to track that aren't covered by the above questions?

<hr>

### Request Google Analytics

1. File an issue in ```vets-team repo```.
    * Title: ```Request Google Analytics```
    * Labels: 
      * ```analytics```
      * ```external-request```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Comment: 
      * **Context**: Provide some context for your team's project.
        * e.g., ```Functionality adds a new dataset to the Facility Locator so users can search for and view non-VA health providers on the map, as well as in list and detail views.```
      * **Tracking information**: Upload the Word document you prepared above.
      * **URL**: ```link to your project on staging```
1. **Within 4 business days**, DSVA will create an implementation approach for Google Analytics in your project.
    * If you don't hear anything after 4 business days, reach out to your DSVA Contact.
    * There may be some back-and-forth in the Github issue comments as DSVA gathers the information needed to set up GA for your project.
1. When this is done, DSVA will update the Github issue.
    * *If custom events are required, DSVA will*
      1. Update the issue with a description of how to implement the custom events in the code.
      1. Your team will make the necessary code changes and push them to staging.
      1. Your team will update the issue with this comment: ```Custom events are set up```
    * *If custom events are not required*, DSVA will continue to the next step.
1. DSVA will verify that Google Analytics is working properly in your project on staging.
    * If there are any issues, DSVA will fix them and re-verify.
1. When DSVA is confident Google Analytics is working properly for your project, DSVA will
    * Add a comment to the Github issue: ```GA ready to go```
    * Close the issue.
1. When the issue is closed, Github will send a notification to the issue creator. This is your team's signal that this pre-launch activity is complete.

