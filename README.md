memcached_docker
=========

Ansible role for install and run memcached in docker.

Requirements
------------

* Docker must be installed on the remote machine. You can use role `cesnet.docker`.
* Required module: `community.docker.docker_compose`
  * Install it by command: `ansible-galaxy collection install community.docker`


Role Variables
--------------

* memcached_path
  * Directory (There will be stored docker-compose file)
  * Default value: "/opt/memcached"
* memcached_docker_image
  * Specify the docker image to use
  * Default value: "memcached:latest"
* memcached_docker_compose_template
  * Path to the template which will be load as docker-compose file. Without `.j2`
  * Default value: "default-docker-compose.yml"

Dependencies
------------

- 


Example Playbook
----------------

    - hosts: all
      roles:
         - { role: cesnet.memcached }


