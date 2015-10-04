vault
=====

[![Ansible Role](https://img.shields.io/ansible/role/3561.svg)](https://galaxy.ansible.com/list#/roles/3561)

Installs and configures Vault

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                                   | Default                                                          | Description                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| vault_version                          | 0.3.0                                                            | Version of Vault to install                                                                                                   |
| vault_sha256sum                        | 30b8953e98059d1e8d97f6a164aa574a346a58caf9c5c74a911056f42fbef4d5 | SHA 256 checksum of package                                                                                                   |
| vault_backend                          | consul                                                           | Configures the storage backend where Vault data is stored                                                                     |
| vault_disable_mlock                    | false                                                            | If true, this will disable the server from executing the mlock syscall to prevent memory from being swapped to disk           |
| vault_default_lease_ttl                | "720h"                                                           | Configures the default lease duration for tokens and secrets, specified in hours                                              |
| vault_max_lease_ttl                    | "720h"                                                           | Configures the maximum possible lease duration for tokens and secrets, specified in hours                                     |
| vault_telemetry                        | false                                                            | Enable or disable telemetry                                                                                                   |
| vault_backend_consul_advertise_addr    | ''                                                               | For backends that support HA, this is the address to advertise to other Vault servers in the cluster for request forwarding   |
| vault_backend_consul_path              | "vault/"                                                         | The path within Consul where data will be stored                                                                              |
| vault_backend_consul_address           | ''                                                               | The address of the Consul agent to talk to                                                                                    |
| vault_backend_consul_scheme            | ''                                                               | "http" or "https" for talking to Consul                                                                                       |
| vault_backend_consul_datacenter        | ''                                                               | The datacenter within Consul to write to                                                                                      |
| vault_backend_consul_token             | ''                                                               | An access token to use to write data to Consul                                                                                |
| vault_backend_consul_tls_skip_verify   | false                                                            | Enable or disable TLS host verification for Consul communication                                                              |
| vault_backend_consul_tls_ca_file       | ''                                                               | The path to the CA certificate used for Consul communication                                                                  |
| vault_backend_consul_tls_cert_file     | ''                                                               | The path to the certificate for Consul communication                                                                          |
| vault_backend_consul_tls_key_file      | ''                                                               | The path to the private key for Consul communication                                                                          |
| vault_backend_zookeeper_advertise_addr | ''                                                               | For backends that support HA, this is the address to advertise to other Vault servers in the cluster for request forwarding   |
| vault_backend_zookeeper_path           | "vault/"                                                         | The path within Zookeeper where data will be stored                                                                           |
| vault_backend_zookeeper_address        | "http://localhost:4001"                                          | The address(es) of the Zookeeper instance(s) to talk to. Can be comma separated list (host:port) of many Zookeeper instances  |
| vault_backend_etcd_advertise_addr      | ''                                                               | For backends that support HA, this is the address to advertise to other Vault servers in the cluster for request forwarding   |
| vault_backend_etcd_path                | "vault/"                                                         | The path within etcd where data will be stored                                                                                |
| vault_backend_etcd_address             | "localhost:2181"                                                 | The address(es) of the etcd instance(s) to talk to. Can be comma separated list (protocol://host:port) of many etcd instances |
| vault_backend_s3_advertise_addr        | ''                                                               | For backends that support HA, this is the address to advertise to other Vault servers in the cluster for request forwarding   |
| vault_backend_s3_bucket                | ''                                                               | The name of the S3 bucket to use                                                                                              |
| vault_backend_s3_access_key            | ''                                                               | The AWS access key                                                                                                            |
| vault_backend_s3_secret_key            | ''                                                               | The AWS secret key                                                                                                            |
| vault_backend_s3_session_token         | ''                                                               | The AWS session_token                                                                                                         |
| vault_backend_s3_region                | "us-east-1"                                                      | The AWS region                                                                                                                |
| vault_backend_mysql_advertise_addr     | ''                                                               | For backends that support HA, this is the address to advertise to other Vault servers in the cluster for request forwarding   |
| vault_backend_mysql_username           | ''                                                               | The MySQL username to connect with                                                                                            |
| vault_backend_mysql_password           | ''                                                               | The MySQL password to connect with                                                                                            |
| vault_backend_mysql_address            | "127.0.0.1:3306"                                                 | The address of the MySQL host                                                                                                 |
| vault_backend_mysql_database           | "vault"                                                          | The name of the database to use                                                                                               |
| vault_backend_mysql_table              | "vault"                                                          | The name of the table to use                                                                                                  |
| vault_backend_mysql_tls_ca_file        | ''                                                               | The path to the CA certificate to connect using TLS                                                                           |
| vault_backend_file_path                | ''                                                               | The path on disk to a directory where the data will be stored                                                                 |
| vault_listener_tcp_address             | "127.0.0.1:8200"                                                 | The address to bind to for listening                                                                                          |
| vault_listener_tcp_tls_disable         | true                                                             | Enable or disable TLS                                                                                                         |
| vault_listener_tcp_tls_cert_file       | ''                                                               | The path to the certificate for TLS                                                                                           |
| vault_listener_tcp_tls_key_file        | ''                                                               | The path to the private key for the certificate                                                                               |
| vault_listener_tcp_tls_min_version     | "tls12"                                                          | Specifies the minimum supported version of TLS. Accepted values are "tls10", "tls11" or "tls12"                               |
| vault_telemetry_statsite_address       | ''                                                               | An address to a Statsite instance for metrics                                                                                 |
| vault_telemetry_statsd_address         | ''                                                               | An address to a StatsD instance for metrics                                                                                   |
| vault_telemetry_disable_hostname       | false                                                            | Whether or not to prepend runtime telemetry with the machines hostname                                                        |

Dependencies
------------

- kbrebanov.unzip

Example Playbook
----------------

Install Vault using Consul backend
```
- hosts: all
  roles:
    - kbrebanov.vault
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
