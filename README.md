# exist-splunk-app
Splunk> apps to monitor eXist-db

## Introduction
This repository contains a number of Splunk> "apps" that allows to monitor
the eXist-db server. The apps provide "inputs", "sourcetypes", "index definitions"
and dashboards.

## Install
> The eXist-db install is assumed to be installed in `EXIST_HOME`, Splunk in
`SPLUNK_HOME`, the Splunk "Universal Forwarder" (UF) in `UF_HOME` etc.

### Inputs
The 'inputs' apps shall be installed in a UF on the host were eXist-db is running.
The apps must be copied into `UF_HOME/etc/apps` ; as these apps are actually
onboarding data, the apps need to be configured to know the location of eXist-db.

> Edit the file `UF_HOME/etc/apps/existdb-inputs/default/inputs.conf` and
fill in `EXIST_HOME` on the appropriate lines.

When eXist-db and Splunk run on the same server, the location of the app is
`SPLUNK_HOME/etc/apps/existdb-inputs`

### Other apps
The other apps (sourcetypes, index and main app), shall be copied into
`SPLUNK_HOME/etc/apps`; no additional configuration is required.

## References
- [Install and configure an Universal Forwarder](https://answers.splunk.com/answers/50082/how-do-i-configure-a-splunk-forwarder-on-linux.html)
- [Splunk documentation](http://docs.splunk.com)
