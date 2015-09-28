vault
=====

[![Ansible Role](https://img.shields.io/ansible/role/3561.svg)](https://galaxy.ansible.com/list#/roles/3561)

Installs Vault

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name             | Default                                                          | Description                  |
|------------------|------------------------------------------------------------------|------------------------------|
| vault_version    | 0.3.0                                                            | Version of Vault to install  |
| vault_sha256sum  | 30b8953e98059d1e8d97f6a164aa574a346a58caf9c5c74a911056f42fbef4d5 | SHA 256 checksum of package  |

Dependencies
------------

- kbrebanov.unzip

Example Playbook
----------------

Install Vault
```
- hosts: all
  roles:
    - { role: kbrebanov.vault }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
