# Request access to AWS

<hr>

* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal Contractors" refers to DSVA's primary vendor contractor and its subcontractors.*

  * *"External Contractors" refers to any other contractor team working on the Veteran-facing Services Platform.*

<hr>

## For AWS Console access:

Our infrastructure is hosted in and makes use of services in AWS GovCloud. This account is shared amongst many different
teams; changes made to resources in this account will affect many services. You will need access to AWS for troubleshooting, 
log file review and to apply changes to the running instances and services.
 
**Do not initiate** this process until PIV background check is underway.
#### 1. Request to create account
* File an issue in [va.gov-team repo](https://github.com/department-of-veterans-affairs/va.gov-team).
  * Request type: AWS Console
  * Tag group `vsp-operations` to review
  * Monitor the issue for updates and respond to any questions from the operations group.
  * Occasionally operations will need to reach out via Slack for additional information.

#### 2. When your account has been setup, you will receive a Slack private message with your temporary password and login URL.
#### 3. You are required to login and change the temporary password immediately.
* AWS will prompt you to change your password during first login
* Additionally you are required to setup a virtual MFA device in order to access services in the AWS cloud and programmatically via the CLI.
  * Follow the walk through for MFA setup [here](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/AWS%20Console%20Setup.md#mfa-virtual-device)
