ansible-role-bootstrap
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Bootstrap a system (many flavors) to use Ansible, likely the first role to depend on. This role does not depend on other roles, but many others may depend on this role.

Requirements
------------

Access to a repository containing packages, likely on the internet.
Ansible 2.2 or higher.

Role Variables
--------------

None known.

Dependencies
------------

None known. This is likely the role that comes first when using Ansible, many others will depend on this role.

Example Playbook
----------------

```
---
- hosts: all
  gather_facts: no

  roles:
    - ansible-role-bootstrap

  tasks:
    - name: do something.
      ping:
```

Fact gathering will be done in the role when all required software is installed.
Tasks that require root access have "become" set to yes. Therefor this role can be included without become. (See example playbook above.)

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
