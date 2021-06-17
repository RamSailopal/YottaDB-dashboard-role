Role Name
=========

This role automates the process of installing the necessary YottaDB-dashboard service to allow integration with Prometheus/Grafana.

Requirements
------------

It is assumed that Yottadb is aready installed on the server as well as Prometheus and Grafana. If log analytics are required, it is assumed that Promtail and Loki are also set up with relevant datasources set up within Grafana.

Role Variables
--------------

instdir - The directory in which YottaDB-dashboard is to be installed

[ Default - /usr/local/YottaDB-dashboard ]

yotroutdir - The directory in which Yottadb routines are held

[ Default - /root/.yottadb/r1.30_x86_64/r ]

mgateway - Whether M Gateway service logs need to be interogated

[ Default - no ]

yotta_env - Environmental variables when running service process

[ Defaults - 
       YOTTA_PROM_PORT: '8001'
       yotta_dir: '/root/.yottadb/r1.30_x86_64' ]


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      role: YottaDB-dashboard
      instdir: /opt/YottaDB-dashboard
      ...

Further Information
-------------------

The git repo referenced in the role to install the dashboard:

https://github.com/RamSailopal/YottaDB-dashboard

License
-------

BSD

Author Information
------------------

Raman Sailopal
