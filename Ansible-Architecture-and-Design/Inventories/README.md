# Basic Inventories configuration

## -------------------- Note 01 ------------------------
#### File Structure
```python
project-folder/
├── ansible.cfg
├── hosts
└── playbook.yml

```
#### File name: ansible.cfg
```python
[defaults]
inventory = hosts
```
#### File name: hosts

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
#### File name: ansible.cfg
```python
[defaults]
inventory = hosts
host_key_checking = False 
```
Note: Setting in *ansible.cfg* - *host_key_checking = False* disables this safety check. It means Don’t verify or prompt for SSH host keys — just connect directly.

#### File name: hosts

```python
[all]
192.168.1.1
192.168.1.2
192.168.2.1
webserver.com
server1
```
