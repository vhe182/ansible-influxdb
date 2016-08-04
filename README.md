Role Name
=========

This role installs InfluxDB and its dependencies.  To do so, it retrieves a key from the influxdb site and adds it to apt then pulls influxdb from the appropriate repo.

Requirements
------------

This role will escalate to administrator priviledges (sudo) for many of the required executions.  Also, Influxdb uses TCP port 8083 for the Admin GUI and TCP port 8086 for client-server communication using InfluxDB's HTTP API.  This role leaves the ports to the default settings.

Role Variables
--------------

Variable names used in this role that can be changed as per the user's wishes are the following:

The influx database key for pulling the latest build from influxdb repo.
`influx_db_url_key`

This role is configured to install InfluxDB on an Ubuntu OS.
`distro_id: "ubuntu"`

Currently, this role defaults to installing dependencies for Ubuntu 14.04, trust tahr
distro_codename: "trusty"

Dependencies
------------

This role does not have any role dependencies to perform correctly.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: vhe182.influxdb }

License
-------

BSD

Author Information
------------------

Author: Victor Estrada, Performance Team, Rackspace
Date: August 2016
