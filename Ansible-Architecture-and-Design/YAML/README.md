# ==== Note 01 ====
#### Note: You can see the YAML file structure here. It is straightforward and similar to the JSON format. *Note the double quote* 
```python
# Every YAML file should start with three dashes
---

name: Suresh
city: "BLR"
address: 'BLR, India'
 
# Every YAML file should end with three dots
...
```

# ==== Note 02 ====
#### Note: you can see the multiline comment, each line will be provided in the next line, like if you have multiple commands for Cisco, you can keep them all like this. *Note the | and next line* 
```python
# Every YAML file should start with three dashes
---

module: |
  show runn
  show vlan
  show 
 
# Every YAML file should end with three dots
...
```
AND
#### Note: if you see the value, it will look like a single line separated with a space, and at the end it will give you the next line; *Note the > and next line*
```python
# Every YAML file should start with three dashes
---

module: >
  single line part1 
  single line part2
  single line part3
 
# Every YAML file should end with three dots
...
```
AND
#### Note: if you see the value, it will result in a single line separated with a space; *>*
```python
# Every YAML file should start with three dashes
---

module: >-
  single line part1 
  single line part2
  single line part3
 
# Every YAML file should end with three dots
...
```
# ==== Note 03 ====
```Python
# Every YAML file should start with three dashes
---

example_integer: 1   # ---> this is integer 
example_integer: "1"  # ---> this is string
 
# Every YAML file should end with three dots
...
```
# ==== Note 04 ====
```Python
---
# Every YAML file should start with three dashes

- item 1
- item 2
- item 3
- item 4
- item 5

# Every YAML file should end with three dots
...
```
![List](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_10h48_18.png "List")

```python
---
# Every YAML file should start with three dashes

key_1: value_1
key_2: value_2

# Every YAML file should end with three dots
...
```
![Dictionary](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_10h56_48.png "Dictionary")

```python
---
# Every YAML file should start with three dashes

{example_key_1: example_value_1, example_key_2: example_value_2}

# Every YAML file should end with three dots
...
```
![Dictionary](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_10h59_14.png "Dictionary")

```python
---
# Every YAML file should start with three dashes

[example_list_entry_1, example_list_entry_2]

# Every YAML file should end with three dots
...
```

![List](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h01_13.png "List")

```python
---
# Every YAML file should start with three dashes

example_key_1:
  sub_example_key1: sub_example_value1

example_key_2:
  sub_example_key2: sub_example_value2

# Every YAML file should end with three dots
...
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h14_05.png)

```python
---
# Every YAML file should start with three dashes

example_1: 
  - item_1
  - item_2
  - item_3

example_2: 
  - item_4
  - item_5
  - item_6

# Every YAML file should end with three dots
...
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h16_56.png)


```python
---
# Every YAML file should start with three dashes

example_dictionary_1:
  - example_dictionary_2:
    - 1
    - 2
    - 3
  - example_dictionary_3:
    - 4
    - 5
    - 6
  - example_dictionary_4:
    - 7
    - 8
    - 9

# Every YAML file should end with three dots
...
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h19_21.png)


```python
---
# Every YAML file should start with three dashes
- name: this is the playbook
  host: localhost
  connection: local
  vars:
    key: value
  tasks:
    - name: this is first task
      module:
        copy:
          src: value
          dst: dist_value
    - name: this is second task
      test:
        test1: testvalue
# Every YAML file should end with three dots
...    
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h24_52.png)

# ==== Note 05 ====

```python
---
# Every YAML file should start with three dashes

key_1: value_1
- list1

# Every YAML file should end with three dots
...
 
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h41_59.png)

# ==== Note 06 ====

```python
---
# Every YAML file should start with three dashes

{key_1: value_1}
[list1]

# Every YAML file should end with three dots
...
```
![](https://github.com/suresh950/Ansible-Notes/blob/main/Ansible-Architecture-and-Design/YAML/image/2025-11-09_11h37_28.png)
