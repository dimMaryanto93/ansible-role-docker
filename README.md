`dimmaryanto93.docker`
=========

Repository ini digunakan untuk menginstall `docker`, `docker-compose` dan Docker Engine untuk Linux

Support platform

- Debian
- Ubuntu
- CentOS


Ansible - User Guide
------------

Persiapan yang harus di lalukan, diantaranya

1. Create new user on your server, Recomend using **very-very Strong Password** or using password generator. 
  ```bash
  adduser <username>
  ```

2. Granted to sudoers with NOPASSWD, using `visudo`
  ```ini
  username    ALL=(ALL) NOPASSWD:ALL
  ```

3. Authenticate with private-key for login ssh, generate ssh key on your local machine then use `ssh-copy-id user@your-ip-server` to copy public key to your server.


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

Ada beberapa variable yang temen-temen bisa gunakan untuk setting docker daemon, diantaranya seperti berikut:

| Variable name                 | Example value | Description |
| :---                          | :---          | :---        |
| `docker_storage_driver`       | `overlay2`    | Default value untuk driver storage adalah `overlay2` tapi temen-temen bisa ganti drivernya sesuai dengan dokumentasi [berikut](https://docs.docker.com/storage/storagedriver/select-storage-driver/) |
| `docker_insecure_registries`  | `[]`          | Default value untuk `insecure-registries` ada kosong tapi temen-tement bisa tambahkan value untuk url insecure registrynya sebagai array contohnya `["registry.example.com:8086", "registry.example.com:8087"]` |
| `docker_insecure_user`        | `-`            | Default value untuk melakukan authentication ke insecure registry |
| `docker_insecure_password`    | `-`            | Default value untuk melakukan authentication ke insecure registry |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: true
      roles:
         - { role: dimmaryanto93.docker }

License
-------

MIT
