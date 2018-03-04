# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [v5.0.0] - 2018-03-04
### Added
- [CHANGELOG](CHANGELOG.md) for keeping track of changes better
- 3x distros on Vagrantfile for testing playbook: Archlinux, Debian, Fedora
- more templates in the packages role that were missing (ie. i3 config..)
- task to install i3 window manager dependencies ( #91 )

### Changed
- remove bloated information from [README.md](README.md)
- each tasks are separated by distribution
  - Archlinux
  - Fedora
  - Ubuntu
- separate Window Manager tasks:
  - LXDE
  - i3

### Removed
- obsolete variables from packages role for Openbox
- obsolete Openbox presence check
- roles from playbook that aren't integrated yet on master branch

[Unreleased]: https://github.com/olivierlacan/keep-a-changelog/compare/v5.0.0...HEAD
[5.0.0]: https://github.com/olivierlacan/keep-a-changelog/compare/4.2.0...v5.0.0
