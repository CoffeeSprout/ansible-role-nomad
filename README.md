coffeesprout.nomad
=========

The `coffeesprout.nomad` Ansible role installs HashiCorp Nomad, a cluster manager and scheduler, for both client and server operations. This role uses default settings that work for the author, but allows for customization through variables.

This role supports both FreeBSD and CentOS 7/8.

Requirements
------------

There are no specific requirements for using this role.

Role Variables
--------------

The following variables can be customized:

- `nomad_datacenter`: This variable sets the Nomad datacenter. The default value is `"dc1"`.
- `download_cache`: This variable sets the directory where Nomad downloads are stored. The default value is `"~/nomad-downloads"`.
- `nomad_dependencies`: This variable sets a list of dependencies required for Nomad installation. The default value is `["unzip"]`.

Example Playbook
----------------

Here's an example playbook that uses this role:

```yaml
- hosts: nomad-servers:nomad-clients
  roles:
    - role: coffeesprout.nomad
      nomad_datacenter: "mydatacenter"
      download_cache: "/opt/nomad-downloads"
      nomad_dependencies:
        - unzip
        - curl

