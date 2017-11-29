docker-engine
=============

This role installs and configures [docker-engine](https://www.docker.com/products/docker-engine) on an Ubuntu Server following [Official Documentation](https://docs.docker.com/engine/installation/linux/ubuntulinux/).

Requirements
------------

Only Ubuntu 14.04 (trusty), 15.10 (wily) and 16.04 (xenial) are supported

Role Variables
--------------

- `docker_engine_init_system`: OS init system. (default 'upstart')
- `docker_engine_is_prod`: Is a production environment or not (default: True)
- `docker_engine_state`: Desired daemon state after role execution (default: 'started')
- `docker_engine_enabled`: Enable docker at boot or not (default: 'yes')
- `docker_engine_opts`: To modify the daemon startup options (Ex: '-H tcp://127.0.0.1:2375')
- `docker_engine_http_proxy`: If you need Docker to use an HTTP proxy (Ex: 'http://127.0.0.1:3128/')
- `docker_engine_tmpdir`: Docker's temporary files dir (Ex: '/mnt/bigdrive/docker-tmp')
- `docker_engine_daemon_config`: Dict used to set /etc/docker/daemon.json config file (default: empty dict)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { 
          role: 'docker-engine',
          docker_engine_opts: '-H tcp://127.0.0.1:2375'
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/dpujadas/ansible-role-docker-engine.svg?branch=master)](https://travis-ci.org/dpujadas/ansible-role-docker-engine)