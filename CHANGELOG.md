# Changelog

## [v0.6.0](https://github.com/hifis-net/ansible-role-gitlab-runner/tree/v0.6.0) (2022-06-17)

[Full Changelog](https://github.com/hifis-net/ansible-role-gitlab-runner/compare/v0.5.1...v0.6.0)

**Implemented enhancements:**

- Link issue\_tracker URL to GitHub [\#31](https://github.com/hifis-net/ansible-role-gitlab-runner/issues/31)
- Add badges to README [\#11](https://github.com/hifis-net/ansible-role-gitlab-runner/issues/11)
- Implement a daily scheduled run of the CI pipeline [\#6](https://github.com/hifis-net/ansible-role-gitlab-runner/issues/6)
- Update dependencies via Dependabot [\#5](https://github.com/hifis-net/ansible-role-gitlab-runner/issues/5)
- Migrate changelog to github-changelog-generator [\#21](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/21) ([tobiashuste](https://github.com/tobiashuste))
- Skip runner registration in molecule test run [\#14](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/14) ([tobiashuste](https://github.com/tobiashuste))
- Add badges to README [\#12](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/12) ([tobiashuste](https://github.com/tobiashuste))
- Use caching feature of setup-python action [\#10](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/10) ([tobiashuste](https://github.com/tobiashuste))

**Fixed bugs:**

- CI pipeline in forks fails [\#9](https://github.com/hifis-net/ansible-role-gitlab-runner/issues/9)

**Merged pull requests:**

- Bump ansible from 5.8.0 to 5.9.0 [\#34](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/34) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump molecule from 3.6.1 to 4.0.0 [\#33](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/33) ([dependabot[bot]](https://github.com/apps/dependabot))
- Update issue tracker link in the Galaxy meta information [\#32](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/32) ([tobiashuste](https://github.com/tobiashuste))
- Bump ansible-lint from 6.2.1 to 6.3.0 [\#29](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/29) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump robertdebock/galaxy-action from 1.2.0 to 1.2.1 [\#27](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/27) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump reuse from 0.14.0 to 1.0.0 [\#26](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/26) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible from 5.7.1 to 5.8.0 [\#25](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/25) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible-lint from 6.0.2 to 6.2.1 [\#24](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/24) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible from 5.7.0 to 5.7.1 [\#19](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/19) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible from 5.6.0 to 5.7.0 [\#18](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/18) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump molecule from 3.5.2 to 3.6.1 [\#17](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/17) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible-lint from 5.3.1 to 6.0.2 [\#16](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/16) ([dependabot[bot]](https://github.com/apps/dependabot))
- Bump ansible from 5.1.0 to 5.6.0 [\#15](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/15) ([dependabot[bot]](https://github.com/apps/dependabot))
- fixes\(\#5\): added dependabot.yml [\#8](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/8) ([tharun634](https://github.com/tharun634))
- fixes\(\#6\): CI daily run [\#7](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/7) ([tharun634](https://github.com/tharun634))
- Implement full lint and test workflow via GitHub Actions [\#1](https://github.com/hifis-net/ansible-role-gitlab-runner/pull/1) ([tobiashuste](https://github.com/tobiashuste))

<!--
SPDX-FileCopyrightText: 2021 Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: 2021 Helmholtz-Zentrum Dresden-Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

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


\* *This Changelog was automatically generated by [github_changelog_generator](https://github.com/github-changelog-generator/github-changelog-generator)*
