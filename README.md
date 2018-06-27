# ansible-misp
Ansible role to deploy MISP and Apache on Ubuntu.

This role was intended to point to an already existing MySQL server.

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
