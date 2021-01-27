Dynatrace ActiveGate
=========
<strong>NOTE: </strong> This is only for Linux, Windows will be supported in a future version

<strong>Purpose: </strong> Automate the process of downloading and configuring the Dynatrace Environment ActiveGate

Requirements
------------
+ Dynatrace Tenant
+ PaaS Token 
+ Network Zone (optional)

Installation
------------
Install the Role with: 
```
ansible-galaxy install droulard.dynatrace_activegate
```

Role Variables
--------------
| Variable      | Description | Optional |
| ----------- | ----------- | ----------- |
| dynatrace_environment_url      | URL to Dynatrace Tenant | Required |
| dynatrace_paas_token   | Dynatrace PasS Token        | Required |
| activegate_network_zone   | Network Zone to use for ActiveGate        | Optional |
| dynatrace_activegate_install_args   | Installation Arguments for installing the active gate    | Optional |


Dependencies
------------
+ None as of now



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
      - droulard.dynatrace_activegate
      vars: 
       dynatrace_environment_url: <tenant_id>.live.dynatrace.com
       dynatrace_paas_token: <paas_token>
       activegate_network_zone: default
       dynatrace_activegate_install_args:
         PROXY: myproxy:888
         INSTALL: /application/dynatrace
         LOG: /application/dynatrace/logs
         CONFIG: /application/dynatrace/config
         TMP: /application/dynatrace/tmp
         PACKAGES_DIR: /application/dynatrace/packages

Currently Supported
---
+ Environment ActiveGate
+ Custom Installation allows you to set:
    + PROXY=<proxy_address>:<proxy_port>
    + USER=<user>
    + INSTALL=<folder>
    + PACKAGES_DIR=<folder>
    + LOG=<folder>
    + CONFIG=<folder>
    + TEMP=<folder>
    + --set-network-zone=<name>

In Development
---
+ Windows AG Support
+ Synthetic and z/OS routing Active Gates
+ CA Cert Support


License
-------

BSD

Author Information
------------------

Kyle.Droulard@dynatrace.com
