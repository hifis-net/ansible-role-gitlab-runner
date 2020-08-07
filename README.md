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

### GitLab-Runner variables
```yaml
gitlab_runner_version: 13.2.2
```
The version of GitLab-Runner to install.

```yaml
gitlab_runner_apt_repo: "deb https://packages.gitlab.com/runner/gitlab-runner/{{ ansible_distribution | lower }}/ {{ ansible_distribution_release }} main"
```
The repository URL where to install the packages from.

### Docker-machine variables
```yaml
docker_machine_binary_url: "https://github.com/tobiashuste/machine/releases/download/v0.16.2-gitlab.4.fork.1/docker-machine-Linux-x86_64"
```
The URL where to download the docker-machine binary file from.

```yaml
docker_machine_binary_checksum: "sha256:f83d54161a4b50fdde9916fbeeb57f429e536d8f0a64feec05ac08f2177ab748"
```
The checksum of the downloaded docker-machine binary. This must correspond to the file download via the
`docker_machine_binary_url` variable.

Dependencies
------------

GitLab-Runner for Openstack depends on `docker-machine` requiring docker to be available on the system.

- Docker - [geerlingguy.docker](https://galaxy.ansible.com/geerlingguy/docker)

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
