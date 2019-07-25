# Request access to tools

<hr>

* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal Contractors" refers to DSVA's primary vendor contractor and its subcontractors.*

  * *"External Contractors" refers to any other contractor team working on the Veteran-facing Services Platform.*

<hr>


## Request Github and Slack access

To work on the Veteran-facing Services Platform, each team member needs to request access to the VA Github organization and to DSVA Slack channels.

**Team members must use their VA.gov email address to request access to Github and Slack.**
> If you don't have a VA.gov email address, ask your company Project Manager (or other project lead) for help.

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

1. Understand the [norms for using these tools](../Norms/norms-tools.md) when you're working on the Veteran-facing Services Platform.


#### Tip:

* If your team is new to Github, we can arrange a short meeting to show you how to use it share documents.

<hr>

## Additional onboarding steps for developers

The internal tools available include Grafana, Sentry, Prometheus and Jenkins. These tools are hosted internally and 
available for developers via proxy access. We use `ssh` and the Chrome plugin SwitchyOmega to route web requests from 
your browser to the SOCKS5 proxy for these private domains. For this we require the use of an `ssh` key pair to secure 
access which we will be walking through in the steps below. Please remember **do not initiate** the issue until your
PIV background check is underway. Opening the issue prematurely will slow down our ability to respond to you in a
timely manner.

#### 1. Create [new SSH keys](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#create-ssh-public-key).

#### 2. Request that your SSH keys be authorized so that you can use the developer tools such as Jenkins, Grafana and Sentry.
* File an issue in [va.gov-team repo](https://github.com/department-of-veterans-affairs/va.gov-team).
* Use the issue template `Environment Access Request Template`
  * Follow the template instructions
    * Provide the name of your Contracting Officer's Representative (COR)
    * Provide your name, role and company
    * Paste the public portion of your ssh key. The template has an example.
    * Grant AWS Console Access? Yes or No.
  * Tag group `@department-of-veterans-affairs/vsp-operations` to review
  * Monitor the issue for updates and respond to any questions from the operations group.
  * Occasionally operations will need to reach out via Slack for additional information.

#### 3. When your key has been added, the Github issue will be closed, which will send a notification to you. This is your signal that you can continue to the next step.

#### 4. Configure [the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#configure-the-socks-proxy).

#### 5. Understand [how to use the SOCKS proxy from inside the VA network and from the internet](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-va-network).

#### 6. [Test and use the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-the-internet).

#### 7. Jenkins, Grafana and Sentry
* Jenkins, Grafana and Sentry have been linked to GitHub for user authentication.
* When logging into these services for the first time click the button `Login with GitHub` or similar
  * You will be prompted to link your GitHub account and presented with a permissions dialog
  * Allow the service to access your account and view your Organization membership
* The services will not be accessible until the SOCKS proxy is configured and working properly.

#### 8. For AWS Console access
##### 8A. When your account has been setup, you will receive a Slack private message with your temporary password and login URL.
##### 8B. You are required to login and change the temporary password immediately.
* AWS will prompt you to change your password during first login
* Additionally you are required to setup a virtual MFA device in order to access services in the AWS cloud and programmatically via the CLI.
  * Follow the walk through for MFA setup [here](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/AWS%20Account%20Setup.md#mfa-virtual-device)


## Tools overview

### Jenkins

With the Socks proxy set up and running, go to http://jenkins.vfs.va.gov. You can see the builds without logging in, but will need to authenticate (with GitHub OAuth) to re-run failed builds. 

### Sentry

With the Socks proxy set up and running, go to http://sentry.vfs.va.gov. 

We do not really use Sentry teams except to separate production, staging, and dev errors. To view the most recent production errors, which is the most common thing to do while on call, go to http://sentry.vfs.va.gov/vets-gov/platform-api-production/

### Grafana
With the Socks proxy set up and running, go to http://grafana.vfs.va.gov/login. You can sign in using your GitHub account by clicking the "GitHub" button on the login page.

There are many dashboards and you should click around to get familiar with the variety of metrics being collected and visualized (make sure Data Source is set to Production). A few highlights are:

- [Site](http://grafana.vfs.va.gov/dashboard/db/site) to see overall metrics about the health of the site
- [External Service Status](http://grafana.vfs.va.gov/dashboard/db/external-service-status) to see the availability of the services vets.gov depends on. 
- [RDS](http://grafana.vfs.va.gov/dashboard/db/rds) to see the database statistics. 
- [Rev Proxy](http://grafana.vfs.va.gov/dashboard/db/revproxy) to see metrics on the reverse proxies.


