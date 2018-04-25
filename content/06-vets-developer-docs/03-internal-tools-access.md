---
title: Internal Tools Access
label: Internal Tools Access
---

This document describes tools available to [name].gov developers, and configuration required to access them. You'll need access to these tools if you need:

* Build logs and details from Jenkins (linked to from GitHub PRs for each project)
* System metrics for diagnostic/troubleshooting purposes (Grafana/Prometheus)
* Exception reports and tracebacks (Sentry)

These internal tools are available on the `vetsgov-internal` domain, which is only accessible while your system is running a SOCKS proxy locally. Your SOCKS proxy will tunnel traffic over a secure channel to vets.gov servers, providing access to:

| Name                 | URL                                              | Description                  |
|----------------------|--------------------------------------------------| -----------------------------|
| Jenkins              | http://jenkins.vetsgov-internal                  | Build Details                |
| Grafana              | http://grafana.vetsgov-internal                  | Metrics / Dashboards         |
| Sentry               | http://sentry.vetsgov-internal                   | Exception Tracking           |
| Prometheus (dev)     | http://prometheus-dev.vetsgov-internal:9090/     | Metrics/Alerts (Detailed)    |
| Prometheus (staging) | http://prometheus-staging.vetsgov-internal:9090/ | Metrics/Alerts (Detailed)    |
| Prometheus (prod)    | http://prometheus-prod.vetsgov-internal:9090/    | Metrics/Alerts (Detailed)    |

You do not need to run the SOCKS proxy while you're developing unless you need access to one of the above tools.

## Requirements

### SSH Key

You'll need to submit your SSH public key to DSVA as part of your onboarding process. If you don't already have a SSH public key, or you're not sure if you do, here are the steps to create one:

1. First run the following command in your terminal: `cd ~/.ssh`.
  If this command returns the following error message, `cd: no such file or directory`,
  you will need to create a .ssh directory by following these steps:
  1. Create the directory by running `mkdir ~/.ssh`.
  2. Run `chmod 700 .ssh`. This sets the permissions on that directory to readable
  only by you since it has your private keys.
  3. Once the directory exists, cd into that directory by running `cd ~/.ssh`.

2. Once you have cd-ed into `~/.ssh`, check to see if you already have your
  SSH keys by running `ls`. If you see `id_rsa_vetsgov` and `id_rsa_vetsgov.pub`
  returned, you already have your keys and you can skip steps 3 and 4. If you don't see
  `id_rsa_vetsgov` or `id_rsa_vetsgov.pub` continue onto the next steps.

3. Run the following command `ssh-keygen -f id_rsa_vetsgov` to generate your public
   and private keys. It will prompt you for a passphrase; you should enter a secure passphrase
   to protect your private key.

4. Run `ls ~/.ssh` and confirm that you see `id_rsa_vetsgov` and `id_rsa_vetsgov.pub`.
   It's normal to see several other files, as well. Seeing `id_rsa_vetsgov` and `id_rsa_vetsgov.pub`
   means you now have your private and public (the one with the `.pub` extension) keys! Your
   private key should never leave your computer, and it's unnecessary and inadvisable to share it
   with anybody.

## Configuring the SOCKS proxy

These steps assume you're running on Linux or OSX. There are slightly
different commands to connect to the proxy depending on whether you
are connected to the VA network or not. You will need to run the SOCKS
proxy on your local system whenever you need access to tools on the
`vetsgov-internal` domain.

With your SSH Public Key, follow these steps:

1. Add the following to your `~/.ssh/config` file:

    ```
      ### Access to SOCKS proxy from public internet, by way of dev jumpbox
      Host socks
         HostName 172.31.2.171
         ProxyCommand ssh -l dsva -A 52.222.32.121 -W %h:%p
         User socks

      ### Access to SOCKS proxy from VA network, by way of dev jumpbox
      Host socks-va
         HostName 172.31.2.171
         ProxyCommand ssh -l dsva -A 10.238.66.162 -W %h:%p
         User socks

      Host *
        AddKeysToAgent yes
        #UseKeychain yes 		   # Uncomment if not using OSX
        IdentityFile ~/.ssh/id_rsa_vetsgov # This must match the public key that you provide during onboarding
    ```
1. Add your SSH key to your local agent with `ssh-add -K ~/.ssh/id_rsa_vetsgov`.

### Accessing SOCKS proxy from VA network

The `~/.ssh/config` file on your local system contains configuration to access the SOCKS proxy from the VA network.

1. Run `ssh socks-va -D 2001 -N &`
   _Note: the first time you connect to the jumpbox, ssh will prompt to ask
   if you are sure you want to connect to a new host. You will be unable to
   respond "yes" if ssh is in the background, so either bring it to the
   foreground with `fg` or omit the `&` character from the above command._

1. Follow the instructions below to configure your browser.

### Accessing SOCKS proxy from the internet

The `~/.ssh/config` file on your local system contains configuration to access the SOCKS proxy from outside the VA network.

1. Run `ssh socks -D 2001 -N &`
   _Note: the first time you connect to the jumpbox, ssh will prompt to ask
   if you are sure you want to connect to a new host. You will be unable to
   respond "yes" if ssh is in the background, so either bring it to the
   foreground with `fg` or omit the `&` character from the above command._

1. Follow the instructions below to configure your browser.

## Testing and Using the SOCKS proxy

Use the following steps to verify that the proxy connection is working, and to configure your
browser to use the proxy connection. Note that the proxy only allows access to our internal
tools, not to the internet at large. So you need to configure your browser to either use the proxy
only for the `vetsgov-internal` domain (as described below for Chrome); enable/disable the proxy
connection as needed; or use a separate browser for accessing the internal tools vs. for general
use.

### Curl

To test your proxy connectivity, the best option is to run the following command:

`$ curl -v --proxy socks5h://127.0.0.1:2001 sentry.vetsgov-internal`

You should get output that includes `HTTP/1.1 302 FOUND`. If not, check that the
SOCKS proxy server is running. You can `$ nc -z 127.0.0.1 2001` as a first step.

### Chrome

1. Install Proxy SwitchyOmega

   https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif

1. Configure the `proxy` profile like this:

   ![](/va-digital-services-platform-docs/assets/develop/images/switchy-omega-config-1.png)

1. Configure the `auto switch` profile like this:

   ![](/va-digital-services-platform-docs/assets/develop/images/switchy-omega-config-2.png)

1. In Chrome's menu bar, click on the proxy app and change the setting to 'auto switch':

   ![](/va-digital-services-platform-docs/assets/develop/images/switch-omega-auto-switch.png)

1. NOTE: You may have to uncheck a settings flag in Chrome, see

   https://github.com/FelisCatus/SwitchyOmega/wiki/DNS-and-SOCKS-proxy

1. Check your connection by navigating to Sentry at
   http://sentry.vetsgov-internal.

### Firefox

1. Install Proxy Switcher
   https://addons.mozilla.org/en-US/firefox/addon/proxy-switcher/
1. create a file on your system with the following contents
    ```
    function FindProxyForURL(url, host) {
		     if( /.*\.vetsgov-internal$/.test(host) ) {
    		 	 return 'SOCKS5 localhost:2001';
		     }
    		 return 'DIRECT';
    }
    ```
1. Configure the `automatic` tab by setting the path to be the file created above
1. Press the reload button in the proxy switcher configuration dialog
1. Check your connection by navigating to Sentry at
   http://sentry.vetsgov-internal.

## Tools

### Jenkins
With the Socks proxy set up and running, go to http://jenkins.vetsgov-internal. You can see the builds without logging in, but will need to authenticate (with GitHub) to re-run failed builds.

### Sentry

With the Socks proxy set up and running, go to http://sentry.vetsgov-internal. You will need to register for Sentry, but after creating any username/password, you will have access. We do not really use Sentry teams except to separate production, staging, and dev errors. To view the most recent production errors, which is the most common thing to do while on call, go to http://sentry.vetsgov-internal/vets-gov/platform-api-production/

### Grafana
With the Socks proxy set up and running, go to http://grafana.vetsgov-internal. You will need to register for Grafana, but after creating any username/password, you will have access.

There are many dashboards and you should click around to get familiar with the variety of metrics being collected and visualized (make sure Data Source is set to Production). A few highlights are:

- [Site](http://grafana.vetsgov-internal/dashboard/db/site) to see overall metrics about the health of the overall site.
- [External Service Status](http://grafana.vetsgov-internal/dashboard/db/external-service-status) to see the availability of external services vets.gov depends on.
