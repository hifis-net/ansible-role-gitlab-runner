<!--
SPDX-FileCopyrightText: 2020 Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: 2020 Helmholtz-Zentrum Dresden - Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

GitLab CI Openstack
===================

This Ansible role provides a setup for GitLab CI in Openstack.

Requirements
------------

None.

Role Variables
--------------

```yaml
gitlab_runner_version: 13.2.2
```
The version of GitLab-Runner to install.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

[Apache-2.0](LICENSES/Apache-2.0.txt)

Author Information
------------------

This role was created by [HIFIS Software Services](https://software.hifis.net/).
