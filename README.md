Role Name
=========

Download Dynatrace ActiveGate

Requirements
------------
Dynatrace Tenant

Role Variables
--------------
| Variable      | Description |
| ----------- | ----------- |
| dynatrace_environment_url      | URL to Dynatrace Tenant       |
| dynatrace_paas_token   | Dynatrace PasS Token        |


Dependencies
------------
Active Gate

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
      - dynatrace.activegate
      vars: 
       dynatrace_environment_url: <tenant_id>.live.dynatrace.com
       dynatrace_paas_token: <paas_token>


License
-------

BSD

Author Information
------------------

Kyle.Droulard@dynatrace.com
