CloudStash
=========

A backup solution for your cloud platform.

Rationale
---------

The goal of this role is to provide a means of protecting the data and configuration of a deployed cloud platform. This role will be centered around RHEL7+, RHOS, and Openshift (future releases.)

Configuration
-------------

First all project configurations will be located in the defaults directory where attributes such as ip addresses, directory pathes, and other system information can be configured.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

Apache 2.0

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
