Bootstrap
=========

Executes common tasks that are usually required to bootstrap a newly launched server.

Requirements
------------

No particular requirements.

Role Variables
--------------
List of packages to install:
```
bootstrap_packages:
  - vim
  - htop
  - lsof
```

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

SMTP relay settings:
```
bootstrap_setup_smtp: false
bootstrap_smtp_host: localhost
bootstrap_smtp_port: 25
bootstrap_smtp_user: john.doe@example.net
bootstrap_smtp_password: secret
```
System timezone:

```
bootstrap_timezone: Etc/UTC
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