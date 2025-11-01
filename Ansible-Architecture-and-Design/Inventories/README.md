# Basic Inventories configuration

#### File Structure
```python
project-folder/
├── ansible.cfg
├── hosts
└── playbook.yml

```
#### ansible.cfg
```python
[defaults]
inventory = hosts
```
#### hosts

```python
[all]
192.168.1.1
192.168.1.2
192.168.2.1
webserver.com
server1
```
