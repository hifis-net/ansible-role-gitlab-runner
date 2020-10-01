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
gitlab_runner_docker_machine_binary_url: "https://github.com/tobiashuste/machine/releases/download/v0.16.2-gitlab.4.fork.1/docker-machine-Linux-x86_64"
```
The URL where to download the docker-machine binary file from.

```yaml
gitlab_runner_docker_machine_binary_checksum: "sha256:f83d54161a4b50fdde9916fbeeb57f429e536d8f0a64feec05ac08f2177ab748"
```
The checksum of the downloaded docker-machine binary. This must correspond to the file downloaded via the
`gitlab_runner_docker_machine_binary_url` variable.

### Flatcar Linux configuration
```yaml
gitlab_runner_transpiler_binary_url: https://github.com/coreos/container-linux-config-transpiler/releases/download/v0.9.0/ct-v0.9.0-x86_64-unknown-linux-gnu
```
The URL to the configuration transpiler binary that shall be used.

```yaml
gitlab_runner_transpiler_binary_checksum: "sha256:31f4c3bd2219ba82b743bcbb4afab34a3e11e8a6512cefef407d9b6da0192adb"
```
The checksum of the download transpiler binary. This must correspond to the file
downloaded via the `gitlab_runner_transpiler_binary_url` variable.

```yaml
gitlab_runner_namerservers:
    - 9.9.9.9
    - 149.112.112.112
```
The DNS nameservers to be used by the Openstack Flatcar virtual machine.

```yaml
gitlab_runner_mtu: 1450
```
Configure the MTU (Maximum Transmission Unit) for the docker daemon in Flatcar
linux running in Openstack. The default of 1450 is proven to work for default
Openstack configurations. If you have a different setup, feel free to update
this value.  
**Please note:** This value can cause strange network issues if not configured
properly.

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
