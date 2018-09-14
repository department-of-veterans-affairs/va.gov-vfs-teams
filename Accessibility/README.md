# Accessibility and 508 compliance

<hr>

* **This document applies only to External Contractors.**

**Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

  * *"External contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>


### General

**All applications and features on the Veteran Tools Platform are required to be accessible and 508 compliant.** 


### DSVA Accessibility Process

#### Request an Accessibility/508 review

1. File a Github issue in the ```vets.gov-team repo``` with the following information:
    * Title: ```Request VA 508 review```
    * Labels: 
      * ```508/Accessibility```
      * ```[your team's Github label]```, e.g., "BAH-526"
      * ```external-request```
    * Assign the issue to: ```[your DSVA contact]```
    * In the comments field: 
      * ```Requesting an Accessibility/508 review.```
      * ```Team name is [your team's name]```, e.g., "BAH"
      * ```Working on [the name of your team's project]```, e.g., "526 forms"
      * ```For this functionality: [link to working code on staging]``` 
      * Provide a high-level description of the functionality for which you're requesting this review, e.g., ```Functionality adds a new dataset to the Facility Locator so users can search for and view non-VA health providers on the map, as well as in list and details views.```     
1. Within XX business days [SLA TBD], DSVA will review your code and provide feedback on the changes you need to make.
    *  DSVA will create a separate Github issue for each Accesibility/508 problem found. 
    * Each issue will be assigned to the person who requested the review in Step #1. 
    * Each issue will describe the specific changes required to make the code Accessible/508 compliant - what the problem is, where the problem occurs, how to fix it, and the issue severity.
1. **Your team is expected to make all the changes prior to launch.**
    * When you've completed the changes, update each Github issue with the following comment
    * ```Changes completed in this code [link to the working code on staging]```
    * Close the issue.
    * At this point, your code is cleared to launch (provided you've completed all other pre-launch activities).


#### VA 508 Office review

Because all Veteran Tools Platform code goes through rigorous manual and automated 508 testing, the VA 508 office has approved DSVA to launch code before the VA 508 office reviews it. 

1. Once a month, DSVA meets with the VA 508 office. At the meeting, DSVA presents all code submitted in the preceding 30 days.

1. After the meeting, the VA 508 Office reviews the code and provides feedback/instructions to DSVA.

1. The VA 508 office may request additional changes to your code. If this happens, DSVA will create a new Github issue for each Accesibility/508 problem found by the VA 508 Office.
  * The issues will be assigned to the same person as above.
  * Each issue will describe the specific changes required to make the code Accessible/508 compliant - what the problem is, where the problem occurs, how to fix it, and the issue severity. 

1. **Your team is expected to make all the changes as quickly as possible, for example, in the next sprint following receipt of the requested changes.**
  * When you've completed the changes, update each Github issue with the following comment
  * ```Changes completed in this code [link to the working code on staging]```
  * **DO NOT close the issue.**
    * DSVA will confirm the changes have been made, close the issue, and notify the VA 508 Office that the problem has been resolved.