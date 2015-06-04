NTP
==========

Ansible role to install and configure NTP daemon on RHEL based systems.

# Requirements

Ansible > 1.2

# Role variables
| Name | Description | Default value |
|:-----|:-----|:-----|
| ntp_package_name | Package name | ntp |
| ntp_package_state | Package state | installed |
| ntp_service_name | Service name | ntpd |
| ntp_service_state | service state | running |
| ntp_service_enabled | Boolean defining if NTP has to be started on system boot | true |
| ntp_config_file | File name of ntp.conf | /etc/ntp.conf |
| ntp_config_file_template | Name of Jinja2 template to use to generate the config file | ntp.conf.j2 |
| ntp_drift_file | File name of drift file | /var/lib/ntp/ntp.drift |
| ntp_key_file | File name of key file | /etc/ntp/keys |
| ntp_servers | List of ip addresses or hostnames of NTP servers | [0-3].de.pool.ntp.org |

# Example Playbook

```yaml
- hosts: all
  vars:
    ntp_servers:
    - 0.de.pool.ntp.org
    - 1.de.pool.ntp.org
    - 2.de.pool.ntp.org
    - 3.de.pool.ntp.org
  roles:
  - role: ntp
```

# T24 ntp endpoint

please refer to https://atlassian.office.tipp24.de/confluence/display/TP/Relevant+Service+Endpoint

# License

Apache 2.0

# Author information
[Thomas Krahn]

[Thomas Krahn]: mailto:ntbc@gmx.net
