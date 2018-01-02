Bootstrap
=========

Executes common tasks that are usually required to bootstrap a newly launched server.

Requirements
------------

No particular requirements.

Role Variables
--------------
List of group names to create:
```
bootstrap_groups: 
  - admin
  - webmaster
```
List of users to create:
```
bootstrap_users: 
  - name: hciftci
    groups: 
      - admin
      - webmaster
    state: present
    password: $6$Eds...
    public_key: ssh-rsa ...
```
Upgrade all packages:
```
bootstrap_upgrade_packages: false
```
Set selinux policy:
```
bootstrap_selinux_policy: targeted
```
Set selinux state:
```
bootstrap_selinux_state: disabled
```
Disable root login:
```
bootstrap_disable_root_login: false
```

Dependencies
------------

No dependencies.

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: memoryleak.bootstrap
```
License
-------

BSD

Author Information
------------------

* Haydar Ciftci <haydar.ciftci@gmail.com>