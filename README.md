Zabbix-agent Role for Zabbix 4.0
=================

Supported OSes
--------------
- Debian 7 8 9 (for Debian 9 install zabbix-agent 3.4)
- Ubuntu 14, 16 and 18
- RHEL / CentOS 6 and 7
- Amazon Linux 1 and 2

for windows, please visit: https://www.zabbix.com/documentation/4.0/manual/appendix/install/windows_agent  

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	# Zabbix server to connect to
	zabbix_agent_server: localhost
	# Zabbix port in the server to connect to
	zabbix_agent_server_port: 10051
	# HostMetadata value in the agent config
	zabbix_agent_metadata: system.uname
	# Prefix to be added to the Hostname value in the agent config
	zabbix_agent_hostname_prefix: ""

How to Install
--------------

```
cd /etc/ansible/roles
git clone git@gt42.itmagic.pro:sysadmins/ansible-zabbix-agent.git zabbix-agent 
```

Example Playbook
----------------

```
---
- hosts: zabbix-clients
  roles:
       - zabbix-agent
```

How to run
----------

``` 
ansible-playbook zabbix-agent.yml --limit zabbix-clients 
```
