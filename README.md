# Amtega sqlserver_jdbc_connector role

This is an [Ansible](http://www.ansible.com) role to deploy SqlServer JDBC connector.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

The role setups the following facts:

- sqlserver_jdbc_connector_latest_version: latest version of the connector available on the web. This fact is only available if you are downloading from the official SqlServer site.
- sqlserver_jdbc_connector_jar_path: full path to the deployed jar with the connector.


## Example Playbook

This is an example playbook:

``` yaml
---
- name: msyql_jdpc_connector role sample
  hosts: localhost
  roles:  
    - amtega.sqlserver_jdbc_connector
  vars:
    sqlserver_jdbc_connector_state: present
    sqlserver_jdbc_connector_version: 7.4.1.0_esn
    sqlserver_jdbc_connector_dir: /root/software    
    sqlserver_jdbc_connector_remove_artifact: no
```

## Testing

Tests are based on docker containers. You can setup docker engine quickly using the playbook `files/setup.yml` available in the role [amtega.docker_engine](https://galaxy.ansible.com/amtega/docker_engine).

Once you have docker, you can run the tests with the following commands:

```shell
$ cd amtega.sqlserver_jdbc_connector/tests
$ ansible-playbook main.yml
```

## License

Copyright (C) 2019 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Daniel Sánchez Fábregas.
