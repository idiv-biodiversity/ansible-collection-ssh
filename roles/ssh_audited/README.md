Ansible Role: ssh_audited
=========================

An Ansible role that configures OpenSSH based on the latest [ssh-audit][]
recommendations.

Table of Contents
-----------------

<!-- toc -->

- [Role Variables](#role-variables)
- [Dependencies](#dependencies)
- [Example Playbook](#example-playbook)
  * [Top-Level Playbook](#top-level-playbook)
  * [Role Dependency](#role-dependency)

<!-- tocstop -->

Role Variables
--------------

This role only **sets** variables for the `idiv_biodiversity.ssh.ssh` role.

**Note:** The hardened defaults that this role sets may be different based on
the targeted platform/OS/distro due to what its version of OpenSSH supports.

Dependencies
------------

```yml
---

# requirements.yml

collections:

  - name: idiv_biodiversity.ssh
    version: X.Y.Z

...
```

Example Playbook
----------------

### Top-Level Playbook

Write a top-level playbook:

```yml
---

- name: servers
  hosts: servers

  roles:

    - role: idiv_biodiversity.ssh.ssh_audited
      tags:
        - ssh

...
```

### Role Dependency

Define the role dependency in `meta/main.yml`:

```yml
---

dependencies:

  - role: idiv_biodiversity.ssh.ssh_audited
    tags:
      - ssh

...
```

[ssh-audit]: https://github.com/jtesta/ssh-audit
