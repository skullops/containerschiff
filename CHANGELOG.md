# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [v5.2.0] - 2018-03-18
### Added
- tagged window manager reload task for applying just that configuration
  instead of running the whole playbook
- install packages for ArchLinux and RedHat:
  - tcpdump
  - mtr
  - chromium
- install packages on ArchLinux:
  - gimp
  - unzip
  - nmap
  - evince (needed a pdf reader)
- list of packages to be installed on Notebook only
- touchpad toggle (on/off) on notebook only for easily disabling it when mouse
  is pluged in or when typing
- limit text width to 80 characters in the [CHANGELOG](CHANGELOG.md) and
  [README](README.md)

### Changed
- Ansible roles path in [ansible.cfg](ansible.cfg); just clone the role in the
  project dir where all roles are stored so it's easier to version it
- `vim-ansible-role` name changed to its actual repository name for easily
  switching to it in vim and finding it properly

### Fixed
- RPM Fusion repository provisioning for RedHat distribution; missing jinja2
  escape statement (double quotes and surrounded by double braces)
- sound issues on ArchLinux; installed missing packages (`alsa-utils` and
  `pulseaudio-alsa`)

### Deprecated
- disable autostart processes on i3wm system boot; wasn't functioning very well

### Removed
- duplicate text from [CHANGELOG](CHANGELOG.md)
- xautolock package; it wasn't locking screen after inactivity anyway
- `ansible` vim filetype; was screwing up indentation, `yaml` filetype
  indentation works better out of the box and it's native

## [v5.1.0] - 2018-03-04
### Added
- `xautolock` on ArchLinux for auto-locking screen
- useful Jinja2 URL resource in [README](README.md)
- LibreOffice package to `bootstrap` role for installing on Debian
- Powerline font for `vim-airline`
- weekly cron on ArchLinux for updating mirrorlist

### Changed
- Ansible default Python interpreter to Python3
- `packages` rolename to `bootstrap`
- merged into `master` the following docker roles:
  - `archlinux` branch
  - `fedora` branch
  - [WizDevOps.debian-docker-toolbox](https://github.com/WizDevOps/debian-docker-toolbox)

### Fixed
- typos and URLs in [CHANGELOG](CHANGELOG.md)
- subdirectory creation for project root dir (`~/Repos `)
- Sublime Text installer
- dynamic imports based on `ansible_os_family`

### Deprecated
- Sublime Text role from main playbook

### Removed
- LibreOffice debian role
- `WizDevOps.debian-docker-toolbox` role

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

[Unreleased]: https://github.com/WizDevOps/containerschiff/compare/v5.2.0...HEAD
[v5.2.0]: https://github.com/WizDevOps/containerschiff/compare/v5.1.0...v5.2.0
[v5.1.0]: https://github.com/WizDevOps/containerschiff/compare/v5.0.0...v5.1.0
[v5.0.0]: https://github.com/WizDevOps/containerschiff/compare/4.2.0...v5.0.0

<!--
vim: tw=80
-->
