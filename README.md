# What is this?
This is a collection of all ansible playbooks and scripts I have accumulated over the ~~years~~ past few months

here you will find:
* Bookstack installer
* Matomo installer
* Cachet installer
* Jellyfin installer
* Nginx installer
	 * php7.2
* Zabbix server installer
* Mysql
They can be found in the `roles` folder - It will ever be growing.

You are able to run anything by creating a new file at the top level called `<what it does>.yml` with the file containing (at a minimum):
```
---
- name: <Give it a nme>
  hosts: <pick hosts or all>
  become: yes

  roles:
    - list
    - the
    - roles
    - here
```
then you can run it either via [tower](https://tower.bread) or via the command line
```
ansible-playbook -i hosts -l <pick a node if you want> -u <user to run as> <playbook>.yml
```

---
This repo will hopefully start to grow a lot more as I expand on my ansible journey.