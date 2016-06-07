Ansible Role: Passware Kit Agent for Linux
==========================================

An Ansible role that installs, configures and runs Passware Kit Agent on
CentOS 7.x or Ubuntu 14.04 LTS

Requirements
------------

In order to deploy Passware Kit Agent you will need:

* Ansible installed on your deployer machine

Installation
------------

In order to install Passware Kit Agent for Linux role you can use the following command.

```
$ ansible-galaxy install passware.passware-kit-agent

```


Role Variables
--------------

Available variables are listed below, along with default values:

```yaml
- vars:
    pk_agent_user_name: passware
    pk_agent_user_group: passware
    pk_agent_home_dir_name: /home/passware
    pk_agent_work_dir_name: /home/passware/passware-kit-agent
    pk_agent_logs_dir_name: /home/passware/logs
    pk_agent_service_name: passware-kit-agent
```

Deploying
---------

In order to deploy you need to perform some steps:

* Create a new `hosts` (a-ka `inventory`) file.
  Check [ansible inventory documentation](http://docs.ansible.com/intro_inventory.html)
  if you need help. This file will identify all the hosts where to deploy to.
* Create a new playbook for deploying, for example, `deploy.yml`
* Customize role variables (see [Role Variables](#role-variables))
* Include the `passware.passware-kit-agent` role as part of a play
* Run the deployment playbook

```ansible-playbook -i hosts deploy.yml```


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: passware.passware-kit-agent }

License
-------

MIT

Author Information
------------------

Passware. Inc
800 West El Camino Real, Suite 180
Mountain View, CA  94040
