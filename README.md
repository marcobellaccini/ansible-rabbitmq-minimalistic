ansible-rabbitmq-minimalistic
=============================
[![Build Status](https://travis-ci.org/marcobellaccini/ansible-rabbitmq-minimalistic.svg?branch=master)](https://travis-ci.org/marcobellaccini/ansible-rabbitmq-minimalistic)

Minimalistic, yet powerful and clustering-enabled RabbitMQ Ansible role.

Written for Debian 9 (may work on other versions and distributions too - in case, please let me know).

Role Variables
--------------
Apart from role defaults (for which you can refer to [this file](./defaults/main.yml)), you'll probably want to deploy your custom *rabbitmq.conf* file
to the servers.

You can make the role generate and deploy your *rabbitmq.conf* file by defining the *rabbitmq_conf_template* variable:

    rabbitmq_conf_template: "path/to/rabbitmq.conf.j2"


For other variables, see [Role Defaults](./defaults/main.yml).

Example Playbook
----------------

    - hosts: servers
      roles:
         - ansible-rabbitmq-minimalistic
      vars:
        rabbitmq_conf_template: "my_rabbit_conf/rabbitmq.conf.j2"

License
-------

Apache License 2.0

Author Information
------------------

Marco Bellaccini - marco.bellaccini[at!]gmail.com

[https://github.com/marcobellaccini](https://github.com/marcobellaccini)
