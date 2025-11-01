# Basic Inventories configuration

## -------------------- Note 01 ------------------------
#### File Structure
```python
project-folder/
├── ansible.cfg
├── hosts
└── playbook.yml

```
#### file name: ansible.cfg
```python
[defaults]
inventory = hosts
```
#### file name: hosts

```python
[all]
192.168.1.1
192.168.1.2
192.168.2.1
webserver.com
server1
```
## -------------------- Note 02 -----------------------
#### File Structure
```python
project-folder/
├── ansible.cfg
├── hosts
└── playbook.yml

```
#### file name: ansible.cfg
```python
[defaults]
inventory = hosts
host_key_checking = False
```
#### file name: hosts

```python
[all]
192.168.1.1
192.168.1.2
192.168.2.1
webserver.com
server1
```
