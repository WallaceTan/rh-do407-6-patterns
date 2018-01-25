# rh-do407-6-patterns

```
[student@workstation patterns]$ ansible db1.example.com -i inventory --list-hosts
  hosts (1):
    db1.example.com
```

```
[student@workstation patterns]$ ansible 172.25.252.44 -i inventory --list-hosts
  hosts (1):
    172.25.252.44
```

```
[student@workstation patterns]$ ansible all -i inventory --list-hosts
  hosts (17):
    srv1.example.com
    srv2.example.com
    s1.lab.example.com
    s2.lab.example.com
    jupiter.lab.example.com
    saturn.example.com
    db1.example.com
    db2.example.com
    db3.example.com
    lb1.lab.example.com
    lb2.lab.example.com
    file1.lab.example.com
    web1.lab.example.com
    file2.example.com
    172.25.252.23
    172.25.252.44
    172.25.252.32
```

```
[student@workstation patterns]$ ansible london -i inventory --list-host
  hosts (4):
    db2.example.com
    db3.example.com
    file1.lab.example.com
    lb1.lab.example.com
```

```
[student@workstation patterns]$ ansible environments -i inventory --list-hosts
  hosts (10):
    web1.lab.example.com
    db3.example.com
    file2.example.com
    db2.example.com
    lb2.lab.example.com
    db1.example.com
    jupiter.lab.example.com
    172.25.252.23
    172.25.252.44
    172.25.252.32
```

```
[student@workstation patterns]$ ansible ungrouped -i inventory --list-hosts
  hosts (4):
    srv1.example.com
    srv2.example.com
    s1.lab.example.com
    s2.lab.example.com
```

```
[student@workstation patterns]$ ansible '*.example.com' -i inventory --list-hosts
  hosts (14):
    jupiter.lab.example.com
    saturn.example.com
    db1.example.com
    db2.example.com
    db3.example.com
    lb1.lab.example.com
    lb2.lab.example.com
    file1.lab.example.com
    web1.lab.example.com
    file2.example.com
    srv1.example.com
    srv2.example.com
    s1.lab.example.com
    s2.lab.example.com
```

```
[student@workstation patterns]$ ansible '*.example.com, !*.lab.example.com' -i inventory --list-hosts
  hosts (7):
    saturn.example.com
    db1.example.com
    db2.example.com
    db3.example.com
    file2.example.com
    srv1.example.com
    srv2.example.com
```

```
[student@workstation patterns]$ ansible lb1.lab.example.com,s1.lab.example.com,db1.example.com -i inventory --list-hosts
  hosts (3):
    lb1.lab.example.com
    s1.lab.example.com
    db1.example.com
```

```
[student@workstation patterns]$ ansible '172.25.*' -i inventory --list-hosts
  hosts (3):
    172.25.252.23
    172.25.252.44
    172.25.252.32
```

```
[student@workstation patterns]$ ansible 's*' -i inventory --list-hosts
  hosts (7):
    saturn.example.com
    srv1.example.com
    srv2.example.com
    s1.lab.example.com
    s2.lab.example.com
    file2.example.com
    db2.example.com
```

```
[student@workstation patterns]$ ansible 'prod,172*,*lab*' -i inventory --list-hosts
  hosts (11):
    lb2.lab.example.com
    db1.example.com
    jupiter.lab.example.com
    172.25.252.23
    172.25.252.44
    172.25.252.32
    lb1.lab.example.com
    file1.lab.example.com
    web1.lab.example.com
    s1.lab.example.com
    s2.lab.example.com
```

```
[student@workstation patterns]$ ansible 'db,&london' -i inventory --list-hosts
  hosts (2):
    db2.example.com
    db3.example.com
```
