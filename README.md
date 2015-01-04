ansible-role-ntp
==========

Ansible role to install and configure NTP daemon on RHEL based systems.

Requirements
==========

Ansible 1.2

Example
==========

    - hosts: ntp-servers
      vars:
        ntp_servers:
        - 0.de.pool.ntp.org
        - 1.de.pool.ntp.org
        - 2.de.pool.ntp.org
        - 3.de.pool.ntp.org

