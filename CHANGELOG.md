Changelog
=========

[1.2.9] - 2022-07-19
--------------------

### New Features

- none

### Bug Fixes

- none

### Other Changes

- make min_ansible_version a string in meta/main.yml (#54)

The Ansible developers say that `min_ansible_version` in meta/main.yml
must be a `string` value like `"2.9"`, not a `float` value like `2.9`.

- Add CHANGELOG.md (#55)

[1.2.8] - 2022-05-06
--------------------

### New Features

- none

### Bug Fixes

- none

### Other Changes

- Use meta/collection-requirements.yml for collection dependencies
- bump tox-lsr version to 2.11.0; remove py37; add py310

[1.2.7] - 2022-04-18
--------------------

### New Features

- support gather\_facts: false; support setup-snapshot.yml

### Bug Fixes

- none

### Other Changes

- Add test for sssd files domain configured properly

[1.2.6] - 2022-04-06
--------------------

### New Features

- Execute authselect to update nsswitch

### Bug Fixes

- none

### Other Changes

- bump tox-lsr version to 2.10.1

[1.2.5] - 2022-02-16
--------------------

### New Features

- none

### Bug Fixes

- tlog does not own sssd.conf - so use ini\_file to manage it

### Other Changes

- none

[1.2.4] - 2022-02-08
--------------------

### New Features

- System Roles should consistently use ansible\_managed in configuration files it manages

### Bug Fixes

- none

### Other Changes

- bump tox-lsr version to 2.9.1

[1.2.3] - 2022-01-11
--------------------

### New Features

- none

### Bug Fixes

- none

### Other Changes

- change recursive role symlink to be non-recursive
- bump tox-lsr version to 2.8.3
- Run the new tox test

[1.2.2] - 2021-11-08
--------------------

### New Features

- support python 39, ansible-core 2.12, ansible-plugin-scan

### Bug Fixes

- none

### Other Changes

- update tox-lsr version to 2.7.1

[1.2.1] - 2021-09-13
--------------------

### New Features

- none

### Bug Fixes

- none

### Other Changes

- use apt-get install -y
- use tox-lsr version 2.5.1

[1.2.0] - 2021-08-10
--------------------

### New Features

- Drop support for Ansible 2.8 by bumping the Ansible version to 2.9

### Bug Fixes

- none

### Other Changes

- none

[1.1.1] - 2021-04-07
--------------------

### New Features

- Always install sssd.conf to enable files domain

### Bug Fixes

- Cleaning up ansible-lint errors
- Fix ansible-test errors
- Fix centos6 repos; use standard centos images; add centos8

### Other Changes

- Remove python-26 environment from tox testing
- update to tox-lsr 2.4.0 - add support for ansible-test sanity with docker
- use tox-lsr 2.3.0 and enable ansible-test
- CI: Add support for RHEL-9
- use molecule v3, drop v2 - use tox-lsr 2.1.2
- remove ansible 2.7 support from molecule
- use tox for ansible-lint instead of molecule
- use new tox-lsr plugin
- use github actions instead of travis
- meta/main.yml: CI - Add support for all Fedora images

[1.1.0] - 2020-11-06
--------------------

### New Features

- Add exclude\_users and exclude\_groups support

### Bug Fixes

- none

### Other Changes

- lock ansible-lint version at 4.3.5; suppress role name lint warning
- sync collections related changes from template to tlog role

[1.0.0] - 2020-08-12
--------------------

### Initial Release
