[![Build
Status](https://travis-ci.com/nkakouros-original/ansible-role-kibana.svg?branch=master)](https://travis-ci.com/nkakouros-original/ansible-role-kibana)
[![Galaxy](https://img.shields.io/badge/galaxy-nkakouros.elasticsearch-blue.svg)](https://galaxy.ansible.com/nkakouros/kibana/)

ansible-role-kibana
===================

Installs and configures Kibana.

Description
-----------

This role will:

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

```yaml

```

License
-------

GPLv3

Author Information
------------------

Nikolaos Kakouros (nkak@kth.se)
