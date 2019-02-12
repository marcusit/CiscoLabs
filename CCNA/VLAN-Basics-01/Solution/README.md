## Switch 1
```
! Create VLANs and assign switchports to the approriate VLAN
vlan 100
  name Sales
vlan 200
  name Marketing
int e0/0
  switchport mode access
  switchport access vlan 100
int e0/1
  switchport mode access
  switchport access vlan 200
int e0/2
  switchport mode access
  switchport access vlan 100
! Validate switchport VLAN assignment
show vlan
show vlan brief
! Create the NULL VLAN
vlan 500
  name NULL
int range e0/3 - 48
  switchport access vlan 500
```
