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
#### Note: if you see the value, it will look like a single line separated with a space; *Note the > and next line*
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
#### Note: if you see the value, it will look like a single line separated with a space, and at theend  it will give you the new line like this \n; *Note the > and next line*
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
# ==== Note 02 ====
```Python
# Every YAML file should start with three dashes
---

example_integer: 1   # ---> this is integer 
example_integer: "1"  # ---> this is string
 
# Every YAML file should end with three dots
...
```
