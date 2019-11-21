systemd-statusmail
=========

Like cron, systemd services should be able to send a mail notification on failure.
Just add `OnFailure=status-email-admin@%n.service` to your service file.

Requirements
------------

This role works only on systems running with systemd.

Role Variables
--------------

- `admin_mail`: Email address of the admin. This can be set e.g. as global variable in `group_vars/all/main.yml`


Example Playbook
----------------

```
- hosts: servers
  roles:
    - role: systemd-statusmail
      admin_mail: admin@example.com
```

License
-------

MIT

Author Information
------------------

[Conrad Sachweh](conrad-sachweh.de).
