coffeesprout.nomad
=========

Installs Nomad both for client and server operations. There are other roles out there that do much more, but none of them were simple enough.
This role uses defaults that work for me and requires just the encryption key.

Supports both FreeBSD and CentOS 7/8

Requirements
------------



Role Variables
--------------

    nomad_datacenter: "dc1"

Nomad datacenter; see https://www.nomad.io/docs/agent/options.html#_datacenter

    download_cache: "~/nomad-downloads"

Where to store the nomad downloads

    nomad_dependencies:
    - unzip


Example Playbook
----------------

As always with my role, there are a few required settings that you need to specify. Below is the minimum to get this rolling

    - hosts: nomad-servers:nomad-clients
      roles:
      - role: coffeesprout.nomad
        
License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
