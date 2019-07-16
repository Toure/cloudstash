CloudStash
=========

Backup solution for distributed compute platforms.

Rationale
---------

The goal of this role is to provide a means of protecting the data and configuration of a deployed cloud platform. This role will be centered around RHEL7+, RHOS, and Openshift (future releases.)

Configuration
-------------

First all project configurations will be located in the group_vars directory where attributes such as ip addresses, directory pathes, and other system information can be configured. Command line options can also be used to override configured options.

Example Playbook
----------------
To install packages and configure storage the following options should be used.

$> bash cloudstash.sh --install

To perform a backup on a group of servers use the following:

$> bash cloudstash.sh --backup

To build a rescue image:

$> bash cloudstash.sh --rescue


License
-------

Apache 2.0

Author Information
------------------

Toure Dunnon