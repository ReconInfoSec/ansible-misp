# ansible-misp
Ansible role to deploy MISP and Apache on Ubuntu.

This role is intended to point to an already existing MySQL server. It can be local, or external. RDS, for example.

MISP, MySQL, and Postfix variables can be changed in main.yml.

All other MISP configuration options are in roles/misp/templates/misp.

This role:
* Installs and configures Postfix
* Installs and configures Apache
* Creates a MISP user and MISP database, initializes the database
* Clones all required MISP repositories and deploys MISP
* Installs MISP modules, if desired

Spawned from:
* https://github.com/MISP/ansible
* https://github.com/MISP/MISP/blob/2.4/INSTALL/INSTALL.ubuntu1604.txt
* MISP AWS Community AMI

## Deploy Steps

Sample hosts file:
```
[misp]
172.18.0.10
```

Run playbook:
```
cd ansible-misp
ansible-playbook main.yml
```
