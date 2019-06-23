[![Build
Status](https://travis-ci.com/nkakouros-original/ansible-role-kibana.svg?branch=master)](https://travis-ci.com/nkakouros-original/ansible-role-kibana)
[![Galaxy](https://img.shields.io/badge/galaxy-nkakouros.elasticsearch-blue.svg)](https://galaxy.ansible.com/nkakouros/kibana/)

ansible-role-kibana
===================

Installs and configures Kibana.

Description
-----------

This role will in a configurable manner:

- install Kibana
- configure Kibana
- enable TLS for communication with elasticsearch

Requirements
------------

None, other than a working elasticsearch node with which Kibana will be
configured to talk to.

Role Variables
--------------

Look at the [defaults/main.yml](defaults/main.yml) file for this roles variables
and their documentation.

The role uses an ansible dict (`kibana_config`) to configure Kibana making it
extremely easy to override any defaults used by the role.

Dependencies
------------

You could use
[nkakouros.elasticsearch](https://galaxy.ansible.com/nkakouros/elasticsearch/)
to install elasticsearch.

Example Playbook
----------------

This is a minimal playbook to have kibana installed as soon as possible, with no
certificates, for development purposes.

```yaml
- hosts: kibana-server
  roles:
    - nkakouros.kibana
```

For a full example on how to configure and install a full ELK installation (from
where you can pick what is relevant for your use case) see the
[molecule/default/](molecule/default/) folder. In there, the
[prepare.yml](molecule/default/prepare.yml) file contains a playbook that will
install dependencies that this role will need. The
[playbook.yml](molecule/default/playbook.yml) file will contain a full and
complex example of how to use this role specifically.

License
-------

GPLv3

Author Information
------------------

Nikolaos Kakouros (nkak@kth.se)
