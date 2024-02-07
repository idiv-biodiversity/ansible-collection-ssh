# Ansible Collection - idiv_biodiversity.ssh

-   [idiv_biodiversity.ssh.ssh](roles/ssh/README.md)

    - installs OpenSSH server and configures it
    - this roles has almost no defaults, the stock `sshd` configuration of the
      distro is used

-   [idiv_biodiversity.ssh.ssh_audited](roles/ssh_audited/README.md)

    - depends on the above-mentioned `ssh` role
    - uses distro-specific defaults to configure `sshd`
    - follows the latest `ssh-audit` recommendations

-   [idiv_biodiversity.ssh.ssh_audit](roles/ssh_audit/README.md)

    - installs latest `ssh-audit`
    - used internally in `ssh_audited` to verify the configuration using
      molecule
