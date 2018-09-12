# Accessibility and 508

<hr>

**Definitions for terms used in this folder:**

* *"DSVA" refers to DSVA team members and DSVA detailees.*

* *"Internal contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

* *"External contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>


### General

**All teams working on the Veteran Tools Platform are required to follow the DSVA process for screening participants for any research study related to the Veteran Tools Platform.** 

* The <a href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Research/Request%20or%20Do%20Research/PRA%20and%20Recruiting/PRA/Screener%20Questionnaire%202900-0770/Digital%20Service%20User%20Screener%20Questionnaire.docx" target="_blank">DSVA screener form</a> has PRA clearance and an established OMB form control number.
  * **For DSVA and Internal Contractors**: Follow the process for your specific team.
  * **For External Contractors**: Follow the process [outlined below](#screening-participants-for-external-contractors).


### Screening participants (for External Contractors)

DSVA uses Optimal Workshop to host its recruiting screener. This allows us to collect responses in an organized way and allows us to report PRA "burden hours" (as required by law) for the screener form.


#### Request a 508 review from VA's 508 Office

1. File a Github issue in the ```vets.gov-team repo``` with the following information:
    * Title: ```Request VA 508 review```
    * Labels: 
      * ```508/Accessibility```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * In the comments field: 
      * ```External contractor team requesting a VA 508 review.```
      * ```Team name is [your team's name]```, e.g., "BAH"
      * ```Working on [the name of your team's project]```, e.g., "526 forms"
      * ```For this functionality: [link to working code on staging]```      
1. Within 3 business days, DSVA will review your code and update the Github issue with comments. 
    * The comments will tell you what you need to change in your code to make it 508 compliant. 
1. Your team must complete all the changes before launch. 
    * Plan for some back and forth in the Github issue, e.g., you may have questions about how to implement the requested changes.
1. When you've completed all the changes, update the Github issue with the following comment
    * ```Changes completed in this code [link to the working code on staging]```
    * At this point, your code is cleared to launch (provided you've completed all over pre-launch activities).
1. DSVA has approval to launch code before the VA 508 office approves it (because all code goes through rigorous automated testing before launch). 
    * Once a month, DSVA meets with the VA 508 office in which VA reviews all code submitted for review in that month. 
    * DSVA will present your code to the VA 508 office. 
    * The VA 508 office may request additional changes to your code. If this happens, DSVA will update the Github issue with the changes requested by the VA 508 office. You are expected to make these changes as soon as possible, for example, in the next sprint following receipt of the requested changes.

