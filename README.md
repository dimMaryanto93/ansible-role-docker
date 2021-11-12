`dimmaryanto93.docker`
=========

Repository ini digunakan untuk menginstall `docker`, `docker-compose` dan Docker Engine untuk Linux

Support platform

- Debian
- Ubuntu
- CentOS

Requirements
------------

Untuk menggunakan role ini, kita membutuhkan package/collection 

- [ansible.posix](https://github.com/ansible-collections/ansible.posix)

Temen-temen bisa install, dengan cara 

```bash
ansible-galaxy collection install ansible.posix
```

Atau temen-temen bisa menggunakan `requirement.yaml` file and install menggunakan `ansible-galaxy collection install -r requirement.yaml`, dengan format seperti berikut:

```yaml
---
collections:
  - ansible.posix
```

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
