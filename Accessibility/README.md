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
1. DSVA will review your code and update the Github issue with comments. The comments will tell you what you need to change in your code to make it 508 compliant. 

#### Recruit participants

1. Send the recruiting screener link out to potential participants.
1. Decide how long you want to run the screener, e.g., 1 week, 2 weeks, etc.
1. At the end of that period, update the same Github issue by adding a comment with the following information:
    * ```Please export the responses for this screener: [link to the screener].```
    * ```Send the responses to this email address: [email address]```
    * **Note**: the email address must be an official work email address associated with the external company working on the specific project, e.g., *somename@bah.com*
1. Within 2 business days, you will receive an **encrypted email** with the screener responses.  
    * If you don't get a response within 2 days, reach out to your DSVA contact.
1. Choose potential participants from the screener responses and continue with your normal recruiting process (i.e., setting up dates/times, etc.)
    * **External Contractors**: [See tips below](#tips).
    * **Note:** If you need specific participant types (e.g., Veterans with a MyHealtheVet account), call potential participants and ask them via phone. Questions asked via phone **are not subject to PRA,** so you can use a phone call to narrow your participant pool to the exact participant types you need.


#### Tips

* Start recruiting at least 2 weeks before you plan to run the research sessions.

* Be sure your recruiting pool includes the kinds of Veterans you need for this study.

* External Contractors are responsible for their own recruiting. If your team doesn't have in-house recruiters for user research, you can

	* Hire a recruiting firm to assist you.
	  * If you haven't done so already, talk to your COR about how to do this.
	* Try recruiting Veterans at Veteran-focused events.
	* If you have relationships with any VSOs, contact them to see if they can help you recruit Veterans.
	* Try recruiting Veterans through your own social networks.

* See <a href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Research/Request%20or%20Do%20Research/PRA%20and%20Recruiting/Outreachrecruiting-language-proposed.md" target="_blank">some examples of recruiting emails</a> at different points in the recruiting process (*after completing the onboarding steps, you’ll be able to see this content*).


