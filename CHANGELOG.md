v0.4.0
------

- bump to ssh-audit 3.9+
  - bumps kex algorithms
  - bumps key algorithms
- drops EL 8 support/tests
- drops Ubuntu Focal support/tests
- adds Debian Bookworm and Trixie support/tests
- adds EL 10 support/tests
- adds Ubuntu Noble and Resolute support/tests
- bumps `/etc/ssh/sshd_config` templates
- ssh-audit: show pip install output for default installation

### CI

- bumps github actions
- bumps ansible version

### Fixes

- diff in `/etc/sshd_config` mode with EL
- `sshd -T` case matching in tests
- `ssh-audit` version printing in tests

v0.3.0
------

- adds latest RHEL 9 KEX algorithms recommendations
- fixes `INJECT_FACTS_AS_VARS` deprecation warning
- fixes conditional from int to bool conversion
- bumps archlinux template

v0.2.0
------

- fixes ssh key gen impotency
- adds missing host keys tag to vars
- adds argument specs
