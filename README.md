CloudStash
=========

Backup solution for distributed compute platforms.

Rationale
---------

The goal of this role is to provide a means of protecting the data and configuration of a deployed cloud platform. This role will be centered around RHEL7+, RHOS, and Openshift (future releases.)

Configuration
-------------

First all project configurations will be located in the defaults directory where attributes such as ip addresses, directory pathes, and other system information can be configured. Command line options can also be used to override configured options.

Example Playbook
----------------
To install packages and configure storage the following options should be used.

$> ansible-playbook -i inventory --tags install playbooks/cloudstash.yml

To perform a backup on a group of servers use the following:

$> ansible-playbook -i inventory --tags backup playbooks/cloudstash.yml

To build a rescue image:

$> ansible-playbook -i inventory --tags rescue playbooks/cloudstash.yml


License
-------

Apache 2.0

Author Information
------------------

Toure Dunnon