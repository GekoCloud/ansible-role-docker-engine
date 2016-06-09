docker-engine
=============

This role installs and configures [docker-engine](https://www.docker.com/products/docker-engine) on an Ubuntu Server following [Official Documentation](https://docs.docker.com/engine/installation/linux/ubuntulinux/).

Requirements
------------

Only Ubuntu 14.04 (trusty), 15.10 (wily) and 16.04 (xenial) are supported

Example Playbook
----------------

    - hosts: servers
      roles:
        - { 
          role: 'docker-engine'
        }

License
-------

MIT

