```
vlan {id}
name {nombre}

[int f0/2] ----- [int range f0/2, f0/3, f0/4] ----- [int range f0/2 - 4]
switchport mode access
switchport access vlan {id}
```