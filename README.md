# tlog

![CI Testing](https://github.com/linux-system-roles/tlog/workflows/tox/badge.svg)

This role configures a system for [Terminal session
recording](https://github.com/scribery). The role will configure tlog to log
recording data to the systemd journal.

## Requirements

This role is only supported on RHEL8/CentOS8 and Fedora distributions.

### Collection requirements

This role requires the `ini_file` module from `community.general`. If you are
using `ansible-core` you must install that collection.

```bash
ansible-galaxy collection install -vv -r meta/collection-requirements.yml
```

If you are using Ansible Engine 2.9, or are using an Ansible bundle which
includes these collections/modules, you should have to do nothing.

## Role Variables

Configure session recording with SSSD, the preferred way of managing recorded
users or groups. This causes the SSSD files provider to be enabled explicitly.

- `tlog_use_sssd` (default: `true`)

Configure SSSD recording scope - `all` / `some` / `none`:

- `tlog_scope_sssd` (default: `none`)

YAML list of users to be recorded:

- `tlog_users_sssd` (default: `[]`)

YAML list of groups to be recorded:

- `tlog_groups_sssd` (default: `[]`)

YAML list of users to be excluded from recording (only applicable when
scope=all):

- `tlog_exclude_users_sssd` (default: `[]`)

YAML list of groups to be excluded from recording (only applicable when
scope=all):

- `tlog_exclude_groups_sssd` (default: `[]`)

## Example Playbook

```yaml
- name: Deploy session recording
  hosts: all
  roles:
    - linux-system-roles.tlog
  vars:
    tlog_scope_sssd: some
    tlog_users_sssd:
      - recordeduser
```

## Testing

Testing is done with the `tests/tests_*.yml` playbooks.  See `contributing.md`.

## License

GPL v3.0

## Author Information

- Nathan Kinder @nkinder

- Kirill Glebov @sabbaka
