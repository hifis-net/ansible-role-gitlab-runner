## [0.5.1](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.5.1) - 2022-03-17

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.5.0...v0.5.1)

### Fixed

* Fix install from deb file if version is older than installed
  ([!55](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/55)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.5.0](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.5.0) - 2022-03-16

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.4.0...v0.5.0)

### Added

* Add support for optionally installing gitlab-runner via a `.deb` file
  ([!53](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/53)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.4.0](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.4.0) - 2022-03-03

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.3.0...v0.4.0)

### Changed

* Allow to update the installed GPG keys
  ([!52](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/52)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.3.0](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.3.0) - 2022-01-11

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.2.2...v0.3.0)

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
* Bump Python dependencies to the latest version
  ([!50](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/50)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Fixed

* Fix debian docker issue in GitLab CI and bump runner version in tests
  ([!49](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/49)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.2](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.2.2) - 2021-07-30

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.2.1...v0.2.2)

### Fixed

* Fix failing binfmt-init.service for multiarch support
  ([!44](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/44)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.1](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.2.1) - 2021-07-30

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.2.0...v0.2.1)

### Fixed

* Correctly configure MTU and registry mirror for Docker-in-Docker
  ([!43](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/43)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Fix bug when `cache_type` is undefined
  ([!42](https://gitlab.com/hifis/ansible/gitlab-ci-openstack/-/merge_requests/42)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [0.2.0](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.2.0) - 2021-07-28

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.1.0...v0.2.0)

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

## [0.1.0](https://github.com/hifis-net/ansible-role-gitlab-runner/releases/v0.1.0) - 2021-07-20

[List of commits](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/359ac4d5e6371452d5488fcf7daa3a43d935ddc1...v0.1.0)

### Added
Initial release of the Ansible GitLab-Runner Role.
