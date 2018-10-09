# Request access to tools

<hr>

* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal Contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

  * *"External Contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>


## Request Github and Slack access

To work on the Veteran Tools Platform, each team member needs access to the VA Github organization and access to DSVA Slack channels.

1. Have each team member review the [tips for creating a Github account](../Norms/Github/README.md#tips-for-creating-a-github-account) **before creating a Github account.**

1. Have everyone on the team create a Github account.

1. The **team Project Manager** should [use this spreadsheet](external-contractor-team-tracker.xlsx) to capture all names, email addresses, and Github usernames for the team.
    * Indicate which team members are developers (so we can give them access to developer code repos and tools).
    * Please rename the spreadsheet according to your team, e.g., BAH-team-tracker.xlsx.

1. Email the spreadsheet to your DSVA contact.

1. DSVA will add the people on the list to
    * The VA Github organization
    * Slack channels relevant to your project

1. Ask your team to add information to their Github and Slack profiles:
    * Organization: ```Your company name```
    * Working on: ```The project your team is working on```, e.g., "526 ancillary forms"
1. Developers must complete [additional onboarding steps](#additional-onboarding-steps-for-developers) to access the code repositories and tools they'll need for development and deployment. They should complete these steps as soon as they've received the email invitation to join the VA Github organization.

1. Understand the [norms for using these tools](../Norms/tools.md) when you're working on the Veteran Tools Platform.


#### Tip:

* If your team is new to Github, we can arrange a short meeting to show you how to use it share documents.

<hr>

## Additional onboarding steps for developers

1. Create [new SSH keys](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#create-an-ssh-public-key).

1. Request that your SSH keys be authorized so that you can use the developer tools.
    * File an issue in <a href="https://github.com/department-of-veterans-affairs/vets.gov-team" target="_blank">vets.gov-team repo</a>.
      * Title: ```Add SSH key for external developer```
      * Labels: 
        * ```external-request```
        * ```devops```
        * ```your teams' Github label```, e.g., "BAH-526"
      * Assign the issue to: ```your DSVA contact```
      * Comment: ```your public SSH key``` (NOT the fingerprint)    

1. When your key has been added, DSVA will close the Github issue, which will send a Github notification to you. This is your signal that you can continue to the next step.

1. Configure [the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#configure-the-socks-proxy---for-external-developers).

1. Understand [how to use the SOCKS proxy from inside the VA network and from the internet](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-va-network).

1. [Test and use the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#testing-and-using-the-socks-proxy).

