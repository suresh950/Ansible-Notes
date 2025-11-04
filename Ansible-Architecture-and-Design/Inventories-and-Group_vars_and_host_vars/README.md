# Basic Inventories with Group_vars host_vars configuration 

## File Structure
```python
project-folder/
├── ansible.cfg
├── group_vars/
    ├── groupname
├── host_vars/
    ├── hostname
├── hosts
└── playbook.yml
```
## -------------------- Note 01 ------------------------
#### You need to have dir directory named group_vars, and you can have a group name inside as a file, like you can see in the Structure above 

```python
---
ansible_network_os: nxos
ansible_user: abc
ansible_password: xyz
...

```
## -------------------- Note 02 ------------------------
#### You need to have dir directory named host_vars, and you can have a host inside as a file, like you can see in the Structure above 

```python
---
ansible_network_os: nxos
ansible_user: abc
ansible_password: xyz
...

```
