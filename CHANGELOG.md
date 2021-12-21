<!--
SPDX-FileCopyrightText: 2021 Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: 2021 Helmholtz-Zentrum Dresden-Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Group your changes into these categories:

`Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`.

## Unreleased

[List of commits](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/compare/v0.2.2...main)

### Added

* Add support for docker `tls_verify` parameter
  ([!46](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/46)
  by [Normo](https://gitlab.com/Normo)).

### Changed

* Bump geerlingguy.docker to version 4.1.1
  ([!48](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/48)
  by [Normo](https://gitlab.com/Normo)).
* Bump container linux config transpiler to v0.9.2
  ([!47](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/47)
  by [Normo](https://gitlab.com/Normo)).

### Fixed

* Fix debian docker issue in GitLab CI and bump runner version in tests
  ([!49](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/49)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.2](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/releases/v0.2.2) - 2021-07-30

[List of commits](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/compare/v0.2.1...v0.2.2)

### Fixed

* Fix failing binfmt-init.service for multiarch support
  ([!44](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/44)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.1](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/releases/v0.2.1) - 2021-07-30

[List of commits](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/compare/v0.2.0...v0.2.1)

### Fixed

* Correctly configure MTU and registry mirror for Docker-in-Docker
  ([!43](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/43)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Fix bug when `cache_type` is undefined
  ([!42](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/42)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.0](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/releases/v0.2.0) - 2021-07-28

[List of commits](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/compare/v0.1.0...v0.2.0)

### Added
* Allow to configure autoscaling parameters
  ([!36](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/36)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Create a test machine via docker-machine once
  ([!39](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/39)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Changed
* Reference latest version of gitlab-runner throughout the role
  ([!38](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/38)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Skip ignition check tasks if flatcar config is unchanged
  ([!37](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/37)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Fixed
* Document the `limit` parameter
  ([!40](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/40)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.1.0](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/releases/v0.1.0) - 2021-07-20

[List of commits](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/compare/359ac4d5e6371452d5488fcf7daa3a43d935ddc1...v0.1.0)

### Added
Initial release of the Ansible GitLab-Runner Role.
