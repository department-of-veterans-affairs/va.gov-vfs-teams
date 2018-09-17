---
title: Internal Tools Access
label: Internal Tools Access
---

This document describes tools available to Vets.gov developers, and configuration required to access them. You'll need access to these tools if you need:

* Build logs and details from Jenkins (linked to from GitHub PRs for each project)
* System metrics for diagnostic/troubleshooting purposes (Grafana/Prometheus)
* Exception reports and tracebacks (Sentry)

These internal tools are available on the `vetsgov-internal` domain, which is **only accessible while your system is running a SOCKS proxy locally**. To use the SOCKS proxy, you need to create new SSH keys and have them authorized. <a href="https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/Onboarding-External-Contractors/request-access-to-tools.md#additional-onboarding-steps-for-developers" target="_blank">Follow the instructions here</a>. 

Your SOCKS proxy will tunnel traffic over a secure channel to vets.gov servers, providing access to:

| Name                 | URL                                              | Description                  |
|----------------------|--------------------------------------------------| -----------------------------|
| Jenkins              | http://jenkins.vetsgov-internal                  | Build Details                |
| Grafana              | http://grafana.vetsgov-internal                  | Metrics / Dashboards         |
| Sentry               | http://sentry.vetsgov-internal                   | Exception Tracking           |
| Prometheus (dev)     | http://prometheus-dev.vetsgov-internal:9090/     | Metrics/Alerts (Detailed)    |
| Prometheus (staging) | http://prometheus-staging.vetsgov-internal:9090/ | Metrics/Alerts (Detailed)    |
| Prometheus (prod)    | http://prometheus-prod.vetsgov-internal:9090/    | Metrics/Alerts (Detailed)    |

You do not need to run the SOCKS proxy while you're developing unless you need access to one of the above tools.

<!--
## Requirements

*You'll be able to view the instructions at the followings links once you've been added to the VA Github organization.*

1. Create <a title="Go to create ssh keys" href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#create-an-ssh-public-key" target="_blank">new SSH keys</a>.
<br/><br/>

1. Configure <a title="Go to configure socks proxy" href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#configure-the-socks-proxy---for-external-developers" target="_blank">the SOCKS proxy</a>.
<br/><br/>

1. Learn how to <a title="Go to create ssh keys" href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#accessing-socks-proxy-from-va-network" target="_blank">access SOCKS proxy from the VA network and from the internet</a>
<br/><br/>

1. <a title="Go to create ssh keys" href="https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Internal%20Tools.md#testing-and-using-the-socks-proxy" target="_blank">Test and use the SOCKS proxy</a>
-->

<!-- Next Button -->
<a href='./vets-website/vets-website-readme'><div class="next-button"><h5 class="next-text">Next: Vets Website ReadMe</h5></div></a>
