# CouchDB Role

Ansible Role for CouchDB

Restrictions: Does not yet create an admin user.

Requirements
------------

- Ubuntu Server
- "qafoo.base" role

Resource
--------

The CouchDB role provides a service at `app.couchdb.service.consul` domain to
applications that register to it and exposes an environment variable to web,
cron and worker processes:

    export COUCHDB_URL=http://app.couchdb.service.consul:5984
    export COUCHDB_URL=http://foo:bar@app.couchdb.service.consul:5984

Make sure both URLs work for your applications for forward compatbility with
secured databases.

And provide this as Consul Konfiguration:

    $ curl http://localhost:8500/v1/kv/apps/foo/couchdb/url

Role Variables
--------------

    ---
    couchdb_port: 5984
    couchdb_listen: "{{ ansible_all_ipv4_addresses|ipaddr('private')|first|default('127.0.0.1') }}"
    couchdb_apps: []

Example Playbook
----------------

Minimal example:

    - hosts: couchdb
      roles:
        - role: "qafoo.couchdb"
          couchdb_apps: ['foo', 'bar']

License
-------

Licensed under the MIT License. See the LICENSE file for details.

Author Information
------------------

Benjamin Eberlei <benjamin@qafoo.com>
https://github.com/QafooGalaxy
