vault
=====

Installs Vault

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name             | Default                                                          | Description                  |
|------------------|------------------------------------------------------------------|------------------------------|
| vault_version    | 0.1.0                                                            | Version of Vault to install  |
| vault_sha256sum  | f6a8674a54f5b6288ba705bd21843cb1c848107e9ff6e7c17b4cc82cdb46789a | SHA 256 checksum of package  |

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
