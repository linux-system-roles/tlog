Changelog
=========

[1.4.3] - 2025-08-08
--------------------

### Other Changes

- test: default wrapper should use local connection if local (#176)

[1.4.2] - 2025-07-09
--------------------

### Other Changes

- refactor: fix ansible lint unique name issue (#174)

[1.4.1] - 2025-06-16
--------------------

### Bug Fixes

- fix: Set __is_system_running in check mode (#172)

### Other Changes

- ci: Add support for bootc end-to-end validation tests (#169)
- tests: bootc end-to-end validation; fix ownership of sssd-session-recording.conf (#170)
- ci: Use ansible 2.19 for fedora 42 testing; support python 3.13 (#171)

[1.4.0] - 2025-05-21
--------------------

### New Features

- feat: Support this role in container builds (#164)

### Bug Fixes

- fix: Consider "degraded" systemd state as booted (#166)

### Other Changes

- ci: ansible-plugin-scan is disabled for now (#151)
- ci: bump ansible-lint to v25; provide collection requirements for ansible-lint (#154)
- ci: Check spelling with codespell (#155)
- ci: Add test plan that runs CI tests and customize it for each role (#156)
- ci: In test plans, prefix all relate variables with SR_ (#157)
- ci: Create inventory for wrapper test with inventory_hostname (#158)
- ci: Fix bug with ARTIFACTS_URL after prefixing with SR_ (#159)
- ci: several changes related to new qemu test, ansible-lint, python versions, ubuntu versions (#160)
- ci: use tox-lsr 3.6.0; improve qemu test logging (#161)
- ci: skip storage scsi, nvme tests in github qemu ci (#162)
- ci: Bump sclorg/testing-farm-as-github-action from 3 to 4 (#163)
- ci: bump tox-lsr to 3.8.0; rename qemu/kvm tests (#165)
- ci: Add Fedora 42; use tox-lsr 3.9.0; use lsr-report-errors for qemu tests (#167)

[1.3.8] - 2025-01-09
--------------------

### Other Changes

- ci: Use Fedora 41, drop Fedora 39 (#148)
- ci: Use Fedora 41, drop Fedora 39 - part two (#149)

[1.3.7] - 2024-10-30
--------------------

### Other Changes

- ci: Add tft plan and workflow (#135)
- ci: Update fmf plan to add a separate job to prepare managed nodes (#137)
- ci: Bump sclorg/testing-farm-as-github-action from 2 to 3 (#138)
- ci: Add workflow for ci_test bad, use remote fmf plan (#139)
- ci: Fix missing slash in ARTIFACTS_URL (#140)
- ci: Add tags to TF workflow, allow more [citest bad] formats (#142)
- ci: ansible-test action now requires ansible-core version (#143)
- ci: add YAML header to github action workflow files (#144)
- refactor: Use vars/RedHat_N.yml symlink for CentOS, Rocky, Alma wherever possible (#146)

[1.3.6] - 2024-07-02
--------------------

### Bug Fixes

- fix: add support for EL10 (#133)

### Other Changes

- ci: ansible-lint action now requires absolute directory (#132)

[1.3.5] - 2024-06-11
--------------------

### Other Changes

- ci: use tox-lsr 3.3.0 which uses ansible-test 2.17 (#126)
- ci: tox-lsr 3.4.0 - fix py27 tests; move other checks to py310 (#128)
- ci: Add supported_ansible_also to .ansible-lint (#129)

[1.3.4] - 2024-04-04
--------------------

### Other Changes

- ci: fix python unit test - copy pytest config to tests/unit (#122)
- ci: Bump ansible/ansible-lint from 6 to 24 (#123)
- ci: Bump mathieudutour/github-tag-action from 6.1 to 6.2 (#124)

[1.3.3] - 2024-01-31
--------------------

### Other Changes

- refactor: Support with-tlog authselect feature (#120)

[1.3.2] - 2024-01-16
--------------------

### Other Changes

- ci: support ansible-lint and ansible-test 2.16 (#117)
- ci: Use supported ansible-lint action; run ansible-lint against the collection (#118)

[1.3.1] - 2023-12-08
--------------------

### Other Changes

- ci: Bump actions/github-script from 6 to 7 (#114)
- refactor: get_ostree_data.sh use env shebang - remove from .sanity* (#115)

[1.3.0] - 2023-11-29
--------------------

### New Features

- feat: support for ostree systems (#111)

### Other Changes

- Bump actions/checkout from 3 to 4 (#103)
- ci: ensure dependabot git commit message conforms to commitlint (#106)

[1.2.17] - 2023-09-07
--------------------

### Other Changes

- ci: Add markdownlint, test_converting_readme, and build_docs workflows (#99)

  - markdownlint runs against README.md to avoid any issues with
    converting it to HTML
  - test_converting_readme converts README.md > HTML and uploads this test
    artifact to ensure that conversion works fine
  - build_docs converts README.md > HTML and pushes the result to the
    docs branch to publish dosc to GitHub pages site.
  - Fix markdown issues in README.md
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- docs: Make badges consistent, run markdownlint on all .md files (#100)

  - Consistently generate badges for GH workflows in README RHELPLAN-146921
  - Run markdownlint on all .md files
  - Add custom-woke-action if not used already
  - Rename woke action to Woke for a pretty badge
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- ci: Remove badges from README.md prior to converting to HTML (#101)

  - Remove thematic break after badges
  - Remove badges from README.md prior to converting to HTML
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

[1.2.16] - 2023-07-19
--------------------

### Bug Fixes

- fix: facts being gathered unnecessarily (#97)

### Other Changes

- ci: Add pull request template and run commitlint on PR title only (#94)
- ci: Rename commitlint to PR title Lint, echo PR titles from env var (#95)
- ci: ansible-lint - ignore var-naming[no-role-prefix] (#96)

[1.2.15] - 2023-05-23
--------------------

### Bug Fixes

- fix: Switch SSSD files provider to Proxy Provider

### Other Changes

- docs: Consistent contributing.md for all roles - allow role specific contributing.md section
- docs: remove unused Dependencies section in README

[1.2.14] - 2023-04-27
--------------------

### Other Changes

- test: check generated files for ansible_managed, fingerprint
- ci: Add commitlint GitHub action to ensure conventional commits with feedback

[1.2.13] - 2023-04-13
--------------------

### Other Changes

- ansible-lint - use changed_when for conditional tasks; fix indentation (#83)

[1.2.12] - 2023-04-06
--------------------

### Other Changes

- Add README-ansible.md to refer Ansible intro page on linux-system-roles.github.io (#80)
- Fingerprint RHEL System Role managed config files (#81)

[1.2.11] - 2023-01-20
--------------------

### New Features

- none

### Bug Fixes

- ansible-lint 6.x fixes (#71)

### Other Changes

- Add check for non-inclusive language (#69)
- cleanup non-inclusive words.

[1.2.10] - 2022-12-13
--------------------

### New Features

- none

### Bug Fixes

- Unconditionally enable the files provider. (#67)

The implicitly files provider is now disabled in RHEL 8.8+, RHEL9+,
and Fedora.

### Other Changes

- none

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
- update to tox-lsr 2.4.0 - add support for ansible-test with docker
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
