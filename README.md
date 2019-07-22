# Cloudstash

![N|Cloudstash](https://upload.wikimedia.org/wikipedia/commons/4/43/Stash_Logo.png)

Backup solution for distributed compute platforms.

  - Ansible
  - ReaR
  - Magic, just a little

The goal of this role is to provide a means of protecting the data and configuration of a deployed cloud platform. This role will be centered around RHEL7+, RHOS, and Openshift (future releases.)

### Tech

Cloudstash uses a number of open source projects to work properly:

* [Ansible] - software provisioning, configuration management, and application-deployment tool.
* [ReaR] - Linux bare metal disaster recovery solution

And of course Cloudstash itself is open source with a [toure/cloudstash][toure]
 on GitHub.

### Installation

Cloudstash requires [Ansible](https://www.ansible.com/) v2.5+ to run.

Install:

```sh
$ git clone https://github.com/Toure/cloudstash.git
$ cd cloudstash
```
Edit the inventory file: (with your favortie editor)

### Example Content:

```
[controller_nodes]
0.0.0.0  ansible_user=heat-admin
0.0.0.0  ansible_user=heat-admin

[undercloud]
0.0.0.0  ansible_user=stack

[hypervisor_nodes]
0.0.0.0  ansible_user=root

[nfs_servers]
0.0.0.0
```

### Install packages on all nodes:
```sh
$ bash cloudstash.sh --install
```

### Perform the first systems backup:
```sh
$ bash cloudstash.sh --backup
```

### Generate a rescue image:
```sh
$ bash cloudstash.sh --rescue
```

### Development

Want to contribute? Great! Please submit PRs with patches or
open a bug as a feature request.

### Todos

 - Write Tests
 - Add features which I couldn't think about.

License
----

Apache v2


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

[toure]: https://github.com/Toure/cloudstash.git
