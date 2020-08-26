# This repository is being archived and moved to [A new repository](https://github.com/breadnet-uk/ansible)
---
# breadnet-infra (Note form)

Ansible playbooks to stand up infrastructure for breadNET.co.uk

---
**infrastructure required:**
Server count: 4
Server type: 3x starter, 1x beefy boi

---
| rev-1| App-1 | app-2 | app-3 |
| --|--|--| --|
| SSL termination| Analytics  | Bookstack | Zabbix	|
|Nginx or HA proxy| Website | Firefly | jellyfin |
|| Kanboard | passbolt | Minecraft|
|| Status page | Nextcloud | |
|| Month | Unifi | |
|| Sql | Sql  | |
---
**things that need to be setup across all servers**
* SSH keys
* Naming according to previous table
* Correct user (stannardb)
* Zerotier
* IP ranges (Contact support about vrack or vlan (depending on what they call it on openstack))
* Nginx 
* Mysql 
	* Correct root account password 

---
OOO (Order of operations)

**rev-1**

 1. Add SSH keys
 2. Rename server
 3. Setup user account
 4. Install NGINX
 5. Install Mariadb

**app-1**
 

 1. Install Matomo
 2. Install ghost
 3. Install kanboard
 4. install Status page
 5. Install Month server
 6. Install redirect 

**app-2**

 1. Install Bookstack
 2. Install Firefly
 3. Install Passbolt
 4. Install Nextcloud
 5. Install Unifi (may need to dockerize it)

**app-3**

 1. Install Jellyfin
 2. Install Zabbix
 3. Install Grafana

Obviously there will be alot of virtual host files and symlinks as well as juju I'mma need to pull for dns records on CF

