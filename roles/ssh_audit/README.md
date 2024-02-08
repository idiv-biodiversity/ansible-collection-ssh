Ansible Role: ssh_audit
=======================

An Ansible role that installs the latest [ssh-audit][].

Table of Contents
-----------------

<!-- toc -->

- [Dependencies](#dependencies)
- [Example Playbook](#example-playbook)
  * [Top-Level Playbook](#top-level-playbook)
  * [Role Dependency](#role-dependency)

<!-- tocstop -->

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

    - role: idiv_biodiversity.ssh.ssh_audit
      tags:
        - ssh

...
```

### Role Dependency

Define the role dependency in `meta/main.yml`:

```yml
---

dependencies:

  - role: idiv_biodiversity.ssh.ssh_audit
    tags:
      - ssh

...
```

[ssh-audit]: https://github.com/jtesta/ssh-audit
