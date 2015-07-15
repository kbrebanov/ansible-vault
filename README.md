vault
=====

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kbrebanov.vault-660198.svg)](https://galaxy.ansible.com/list#/roles/3561)

Installs Vault

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name             | Default                                                          | Description                  |
|------------------|------------------------------------------------------------------|------------------------------|
| vault_version    | 0.2.0                                                            | Version of Vault to install  |
| vault_sha256sum  | b4b64fcea765ebfc7cdbae9cdd2c32bff130ca51f15b9cf47194f112fd5515cf | SHA 256 checksum of package  |

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
