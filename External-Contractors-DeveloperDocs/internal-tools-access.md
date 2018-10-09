# Internal Tools Access

This document describes tools available to Vets.gov developers, and configuration required to access them. You'll need access to these tools if you need:

* Build logs and details from Jenkins (linked to from GitHub PRs for each project)
* System metrics for diagnostic/troubleshooting purposes (Grafana/Prometheus)
* Exception reports and tracebacks (Sentry)

These internal tools are available on the `vetsgov-internal` domain, which is **only accessible while your system is running a SOCKS proxy locally**. To use the SOCKS proxy, you need to create new SSH keys and have them authorized. [Follow the instructions here](https://github.com/department-of-veterans-affairs/vets-work-practices/blob/master/External-Contractors-Onboarding/request-access-to-tools.md#additional-onboarding-steps-for-developers). 

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

<hr>

Back: [Development Workflow](development-workflow.md)

Next: [Review Instances](review-instances.md)
