## Switch 1 and Switch 2
```
! Create the VLAN and make the appropriate port configs
vlan 100
  name IT Dept
int e0/0
  switchport mode access
  switchport access vlan 100
int e0/1
  switchport trunk encapsulation dot1q
  switchport mode trunk
  switchport nonegotiate
  switchport trunk allowed vlan 100
! Validation commands
show vlan brief
show interface e0/1 switchport
```
