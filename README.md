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
| vault_version    | 0.1.1                                                            | Version of Vault to install  |
| vault_sha256sum  | 856a9c89bada1b8007d85dd2ccd81bb19414691a7e16476282cf1acd920c484a | SHA 256 checksum of package  |

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
