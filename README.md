tlog
=========

This role configures a system for [Terminal session recording](https://github.com/scribery).
The role will configure tlog to log recording data to the systemd journal.

Requirements
------------

This role is only supported on RHEL8/CentOS8 and Fedora distributions.

Role Variables
--------------

Configure session recording with SSSD, the preferred way of managing recorded users or groups:

- `tlog_use_sssd` (default: `yes`)

Configure SSSD recording scope - `all` / `some` / `none`:

- `tlog_scope_sssd` (default: `none`)

YAML list of users to be recorded:

- `tlog_users_sssd` (default: `[]`)

YAML list of groups to be recorded:

- `tlog_groups_sssd` (default: `[]`)


Dependencies
------------

This role has no dependencies currently.

Example Playbook
----------------
~~~
---
- name: SR
  become: yes
  hosts: all
  roles:
    - role: tlog
      vars:
          tlog_scope_sssd:
            - some
          tlog_users_sssd:
            - recordeduser
~~~
Testing
-------
Testing is done with plays in the tests/ subdirectory.

License
-------

GPL v3.0

Author Information
------------------

- Nathan Kinder @nkinder

- Kirill Glebov @sabbaka
