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

```yaml
gitlab_runner_concurrent: 1
```

Limits how many jobs can run concurrently. The maximum number is all defined runners.
`0` does not mean unlimited.

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

### GitLab-Runner registration

In order to register a runner with the GitLab instance of your choice, you need
to edit the `gitlab_runner_list` variable and add a list entry.
Each list entry corresponds to one registered GitLab-Runner.

Below table lists and describes all available configuration options you can
specify for registering your GitLab-Runner with this Ansible role.

| Key                  | Example                    | Description                                                                                       |
|----------------------|----------------------------|---------------------------------------------------------------------------------------------------|
| `name`               | `"my-docker-runner"`       | The name of the registered runner.                                                                |
| `url`                | `"https://gitlab.com"`     | The URL of the GitLab instance you want to register the runner with.                              |
| `description`        | `"My first Docker runner"` | Description of the runner.                                                                        |
| `registration_token` | `"MY_SECURE_TOKEN"`        | The registration token required to register the runner.                                           |
| `tags`               | `["docker", "hifis"]`      | List of runner tags.                                                                              |
| `executor`           | `docker`                   | Specify, the runner [executor](https://docs.gitlab.com/runner/executors/#selecting-the-executor). |
| `docker_image`       | `"python:3.8"`             | Specify the default docker image to be used. Required for `docker` and `docker+machine` executor. |
| `run_untagged`       | `False`                    | Specify, if the runner can run jobs without tags.                                                 |
| `locked`             | `True`                     | Specify, whether the runner is locked to the current project.                                     |
| `machine_driver`     | `"openstack"`              | The driver to use when creating the machine via `docker-machine`.                                 |
| `machine_name`       | `"auto-scale-%s"`          | The machine name template. (You need to include `%s`).                                            |
| `machine_options`    | See the machine example.   | Additional machine creation options.                                                              |

#### Docker Example

```yaml
gitlab_runner_list:
    - name: "my-docker-runner"
      url: "https://gitlab.com"
      description: "My first Docker runner via Ansible."
      registration_token: ${REGISTRATION_TOKEN}
      tags: ["docker", "hifis"]
      executor: "docker"
      docker_image: "python:3.8"
      run_untagged: False
      locked: True
```

For registering a runner using the Docker backend, a sample configuration is
given above.
Therefore, you need to obtain a registration token.
This can be either done on an instance, a group or a project level.
Visit the [GitLab documentation](https://docs.gitlab.com/runner/register/#requirements)
for further information.
In a production setup, please make sure to encrypt the token using
[Ansible Vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html).

### Docker-machine Example

```yaml
gitlab_runner_list:
    - name: "test01"
      url: "https://gitlab.com"
      description: "Molecule test runner"
      registration_token: "REGISTRATION_TOKEN"
      executor: "docker+machine"
      docker_image: "python:3.8"
      tags: ["docker", "hifis"]
      run_untagged: False
      locked: True
      machine_driver: "openstack"
      machine_name: "auto-scale-%s"
      machine_options:
        - "openstack-auth-url=https://openstack.example:5000/v3"
        - "openstack-image-id=73f07dd3-fa8b-468f-b6bc-b0cd4510f5d0"
        - "openstack-flavor-name=m1.small"
        - "openstack-net-id=7834deeb-8bd5-4fc7-b35b-24035d8f47a7"
        - "openstack-username=gitlab-runner"
        - "openstack-password=secret"
        - "openstack-tenant-id=123456"
        - "openstack-domain-name=default"
        - "openstack-ssh-user=core"
        - "openstack-sec-groups=Internal"
        - "openstack-keypair-name=runners-internal"
        - "openstack-private-key-file=/etc/gitlab-runner/gitlab_runner_key"
        - "openstack-user-data-file=/etc/gitlab-runner/flatcar-linux-config.yml"
        - "openstack-active-timeout=300"
        - "engine-registry-mirror=https://registry-mirror.example"
```

The most important changes compared to the docker runner registration is the
configuration of docker-machine.
Therefore, a suitable configuration for the
[driver](https://docs.docker.com/machine/drivers/) of your choice needs to be
created.
This project focuses on providing the best integration with Openstack but is
probably not limited to that.
The Openstack driver lists all possible configuration options that can be
specified via `machine_options`: https://docs.docker.com/machine/drivers/openstack/

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
