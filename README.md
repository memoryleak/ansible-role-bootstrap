Bootstrap
=========

Executes common tasks that are usually required to bootstrap a newly launched server.

Requirements
------------

No particular requirements.

Role Variables
--------------
Define the packages you want to be installed:

```
bootstrap_packages:
  - vim
  - htop
  - lsof
```
Create a list of groups:
```
new_groups: []
```

The list of users to be created:
```
users: []
```

Set if packages should be upgraded.
```
boostrap_upgrade_packages: false
```

Define the PS1 prompt to be used:
```
bootstrap_ps1: \[\e[0;30m\][ \[\e[0;37m\]\t \[\e[0;31m\]\u\[\e[0;37m\]@\[\e[0;34m\]\h \[\e[0;33m\]\W \[\e[0;30m\] ] \[\e[0m\]
```
Dependencies
------------

No dependencies.

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: hciftci.bootstrap
```
License
-------

BSD

Author Information
------------------

* Haydar Ciftci <haydar.ciftci@gmail.com>