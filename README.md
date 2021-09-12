About
-----

Ansible role for installing security updates automatically. Uses dnf-automatic on RedHat / CentOS and the likes.

Requirements
------------

...

Role Variables
--------------

Variables with examples:

```yml
# set upgrade_type, can be
# default                            = all available upgrades
# security                           = only the security upgrades
common_updates_simple_dnf_auto_upgrade_type:     "security"

# maximal random delay before downloading in seconds
common_updates_simple_dnf_auto_random_sleep:     "30"

# set this to 'yes' or 'no'
common_updates_simple_dnf_auto_download_updates: 'yes'

# set this to 'yes' or 'no' - useful to 'yes' when using only security updates
common_updates_simple_dnf_auto_apply_updates:    'yes'

# can be set to 'none' or
# any combination of stdio, email and motd , separated by ,
common_updates_simple_dnf_auto_emit_via:         'stdio'

# settings for e-mail:
common_updates_simple_dnf_auto_email_from:       'root@example.com'

# List of addresses to send messages to.
common_updates_simple_dnf_auto_email_to:         'root'

# Name of the host to connect to to send email messages.
common_updates_simple_dnf_auto_email_host:       'localhost'

# set debug level for dnf automatic if needed
common_updates_simple_dnf_auto_debuglevel:       1
```

Example Usage
-------------

```yml
roles:
  - ansible-role-common-updates-simple
```

Acknowledgements
----------------

Thanks to
* ...

See also
--------

...

License
-------

MIT
