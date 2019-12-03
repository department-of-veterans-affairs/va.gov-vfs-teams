# Request access to tools

## Configure your Github and Slack accounts

To work on the Veteran-facing Services Platform, each team member needs to use the Department of Veterans Affairs Github organization and DSVA Slack channels.

## Slack
1. If you haven't already, check your email for an invitation to join Digital Service at VA on Slack, and join!

1. Add information to your Slack profile:
    * Profile image
    * Full name
    * What I do (i.e. your practice area: Front-end Engineer, Designer, etc)
    * Time zone
    * Pronouns
    * GitHub (i.e. the account handle / username you created when you set up your GitHub account)

## GitHub

1. If you haven't already, check your email for an invitation to the Department of Veterans Affairs GitHub o rganization, and join!

1. Make sure you have "Read" access (not just "Write" access) to the [va.gov-team GitHub repository](https://github.com/department-of-veterans-affairs/va.gov-team). If you don't have the appropriate access, or if you're unsure, let VSP know in the #vfs-platform-support Slack channel.

1. Add information to your Github profile:
    * Organization: ```Your company name```
    * Working on: ```The project your team is working on```, e.g., "526 ancillary forms"

1. Developers, complete the [additional onboarding steps](#additional-onboarding-steps-for-developers) below to access the code repositories and the tools you'll need for development and deployment.

## Additional onboarding steps for developers

The internal tools available include Grafana, Sentry, Prometheus, and Jenkins. These tools are hosted internally and
available for developers via proxy access. We use `ssh` and the Chrome plugin SwitchyOmega to route web requests from
your browser to the SOCKS5 proxy for these private domains. For this we require the use of an `ssh` key pair to secure access, which we walk through in the steps below.

### GitHub Teams
We authorize users for SSH via GitHub teams.  Every time a resource is deployed (like the jump box), the users that are part of the GitHub teams that are tied to that resource are added along with any public keys stored under their GitHub user.  Here's the steps you should take:

#### 1. Create SSH key, add it to your GitHub user, and test that it works ( [See GitHub's SSH key documentation](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh) )

Once you've added an SSH key to your GitHub user, and your GitHub user has been added to the relevant DSVA GitHub team, your GitHub user will automatically be added to the boxes you should have access to on the *next deploy*.  User names are lowercased when added.

#### 2. Configure [the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#configure-the-socks-proxy).

#### 3. Understand [how to use the SOCKS proxy from inside the VA network and from the internet](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-va-network).

#### 4. [Test and use the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-the-internet).

#### 5. Jenkins, Grafana, and Sentry

Jenkins, Grafana, and Sentry have been linked to GitHub for user authentication.
* The services will not be accessible until the SOCKS proxy is configured and working properly.
* When logging into these services for the first time click the button `Login with GitHub` or similar
  * You'll be prompted to link your GitHub account and presented with a permissions dialog
  * Allow the service to access your account and view your organization membership

#### 6. For AWS Console access
##### 6A. When your account has been set up, you'll receive a private Slack message with your temporary password and login URL.
##### 6B. You're required to log in and change the temporary password immediately.
* AWS will prompt you to change your password the first time you log in.
* Additionally you're required to set up a virtual MFA device in order to access services in the AWS cloud and programmatically via the CLI.
  * Follow the walkthrough for MFA setup [here](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/AWS%20Account%20Setup.md#mfa-virtual-device)


#### Once you've completed all of these steps, make sure to skip the `Non-GitHub Teams Method` section below.
<br>
<details>
<summary>Non-GitHub Teams Method (Deprecated)</summary>
<p>

#### 1. Create [new SSH keys](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#create-ssh-public-key).

#### 2. Request that your SSH keys be authorized so that you can use the developer tools such as Jenkins, Grafana, and Sentry.
* File an issue in [va.gov-team repo](https://github.com/department-of-veterans-affairs/va.gov-team).
* Use the issue template `Environment Access Request Template`
  * Follow the template instructions
    * Provide the name of your Contracting Officer's Representative (COR)
    * Provide your name, role, and company
    * Paste the public portion of your ssh key. The template has an example.
    * Grant AWS Console Access? Yes or No.
  * Tag group `@department-of-veterans-affairs/vsp-operations` to review
  * Monitor the issue for updates and respond to any questions from the operations group.
  * Occasionally operations will need to reach out via Slack for additional information.

#### 3. When your key has been added, the Github issue will be closed. This will send a notification to you. This is your signal that you can continue to the next step.

#### 4. Configure [the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#configure-the-socks-proxy).

#### 5. Understand [how to use the SOCKS proxy from inside the VA network and from the internet](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-va-network).

#### 6. [Test and use the SOCKS proxy](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-the-internet).

#### 7. Jenkins, Grafana, and Sentry

Jenkins, Grafana, and Sentry have been linked to GitHub for user authentication.
* The services will not be accessible until the SOCKS proxy is configured and working properly.
* When logging into these services for the first time click the button `Login with GitHub` or similar
  * You'll be prompted to link your GitHub account and presented with a permissions dialog
  * Allow the service to access your account and view your organization membership

#### 8. For AWS Console access
##### 8A. When your account has been set up, you'll receive a private Slack message with your temporary password and login URL.
##### 8B. You're required to log in and change the temporary password immediately.
* AWS will prompt you to change your password the first time you log in.
* Additionally you're required to set up a virtual MFA device in order to access services in the AWS cloud and programmatically via the CLI.
  * Follow the walkthrough for MFA setup [here](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Practice%20Areas/Engineering/AWS%20Account%20Setup.md#mfa-virtual-device)
</p></details>

## Tools overview

### Jenkins

With the Socks proxy set up and running, go to http://jenkins.vfs.va.gov.

You can see the builds without logging in, but you'll need to authenticate (with GitHub OAuth) to re-run failed builds.

### Sentry

With the Socks proxy set up and running, go to http://sentry.vfs.va.gov.

We don't really use Sentry teams except to separate production, staging, and dev errors. To view the most recent production errors, which is the most common thing to do while on call, go to http://sentry.vfs.va.gov/vets-gov/platform-api-production/.

### Grafana
With the Socks proxy set up and running, go to http://grafana.vfs.va.gov/login.

You can sign in using your GitHub account by clicking the "GitHub" button on the login page.

There are many dashboards and you should click around to get familiar with metrics being collected and visualized (make sure Data Source is set to Production). A few highlights are:

- [Site](http://grafana.vfs.va.gov/dashboard/db/site) to see overall metrics about the health of the site
- [External Service Status](http://grafana.vfs.va.gov/dashboard/db/external-service-status) to see the availability of the services VA.gov depends on
- [RDS](http://grafana.vfs.va.gov/dashboard/db/rds) to see the database statistics
- [Rev Proxy](http://grafana.vfs.va.gov/dashboard/db/revproxy) to see metrics on the reverse proxies
