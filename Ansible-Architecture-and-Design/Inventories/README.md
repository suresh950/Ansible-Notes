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
## -------------------- Note 03 -----------------------

#### File name: hosts

*Note: you can create multiple group like mentioned below* 
```python
[SRV1]
192.168.1.1
192.168.1.2

[SRV2]
192.168.2.1
webserver.com
server1
```
*So here we have two groups SRV1 and SRV2*

## -------------------- Note 04 -----------------------

#### File name: hosts

*Note: For providing the username only you can use*  (__ansible_user=admin__) *this keyword* *and for providing the custom port you can use* (__ansible_port=1234__)
*and for the password (__ansible_password: Cisco123__)* *keep in mind that we are doing all in hosts file but there are alternate way to pass the username password and custom port*
*using using group_vars directory*  
```python
[SRV1]
192.168.1.1 ansible_user=admin ansible_port=1234
192.168.1.2 ansible_user=cisco ansible_password: Cisco123

[SRV2]
192.168.2.1
webserver.com
server1
```
## -------------------- Note 05 -----------------------

#### File name: hosts

*Note: if you want to keep all the details related to host in different section you can keep it like below*  
```python
[SRV1]
192.168.1.1 
192.168.1.2 

[SRV2]
192.168.2.1
webserver.com
server1

[SRV:vars] # Note this will be applicable for all the host present in same way you can do it for 
ansible_user=admin 
ansible_port=1234
ansible_password: Cisco123
```
