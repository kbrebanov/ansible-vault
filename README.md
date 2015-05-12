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
| vault_version    | 0.1.2                                                            | Version of Vault to install  |
| vault_sha256sum  | 12c28cf7d6b6052c24817072fb95d4cfa2a391b507c705e960faf11afb5ee6ad | SHA 256 checksum of package  |

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
