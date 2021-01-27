Dynatrace ActiveGate
=========
<strong>NOTE: </strong> This is only for Linux, Windows will be supported in a future version

<strong>Purpose: </strong> Automate the process of downloading and configuring the Dynatrace ActiveGate

Requirements
------------
Dynatrace Tenant

Installation
------------
Install the Role with: 
```
ansible-galaxy install droulard.dynatrace_activegate
```

Role Variables
--------------
| Variable      | Description |
| ----------- | ----------- |
| dynatrace_environment_url      | URL to Dynatrace Tenant       |
| dynatrace_paas_token   | Dynatrace PasS Token        |
| activegate_network_zone   | Network Zone to use for ActiveGate        |
| dynatrace_activegate_install_args   | Installation Arguments for installing the active gate    |


Dependencies
------------
+ Dynatrace Tenant
+ PaaS Token 
+ Network Zone (optional)


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


License
-------

BSD

Author Information
------------------

Kyle.Droulard@dynatrace.com
