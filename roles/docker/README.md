Docker role
=========

Docker provisioning role OS agnostic.

Requirements
------------

None

Role Variables
--------------

```yml
docker_compose_version: "1.17.0"
docker_compose_path: /usr/local/bin/docker-compose

# Debian
docker_apt_url: 'https://download.docker.com/linux/debian'
docker_repo: edge
```

Dependencies
------------

None

Example Playbook
----------------


License
-------

GPLv3

Author Information
------------------

Daniel Andrei Minca <dminca@protonmail.com>
