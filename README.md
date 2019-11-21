tlog
=========

This role configures a system for [Terminal session recording](https://github.com/scribery).

Requirements
------------

This role has no required pre-requisites currently.

Role Variables
--------------

Configure session recording with SSSD, the preferred way of managing recorded users or groups:

- `tlog_use_sssd` (default: `Yes`)

Configure SSSD recording scope - `all` / `some` / `none`:

- `tlog_scope_sssd` (default: `none`)

Comma-separated list of users to be recorded ( e.g. recordeduser, testuser1 ):

- `tlog_users_sssd` (default: `""`)

Comma-separated list of groups to be recorded ( e.g. recordedgroup, wheel, ):

- `tlog_groups_sssd` (default: `""`)

Log writer type(output destination) of tlog-rec-session. Possible values are: `rsyslog` , `journal`:

- `tlog_output` (default: `journal`)


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
          tlog_scope_sssd: "some"
          tlog_users_sssd: "recordeduser"
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
