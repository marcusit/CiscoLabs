## Switch 1
```
! Disable routing if using a L3 switch
no ip routing
! Create the VLAN and make the appropriate port configs
vlan 22
vlan 33
int e0/0
  switchport mode access
  switchport access vlan 22
int e0/1
  switchport mode access
  switchport access vlan 33
int e0/2
  switchport trunk encapsulation dot1q
  switchport mode trunk
  switchport nonegotiate
  switchport trunk allowed vlan 22,33
! Validation commands
show vlan brief
show int e0/2 switchport
show int trunk
```
## Router 1
```
! Configure the physical interface
int fa0/0
  no shutdown
  no ip address
! Create and configure the sub interfaces
int fa0/0.22
  encapsulation dot1Q 22
  ip address 10.22.0.1 255.255.255.128
int fa0/0.33
  encapsulation dot1Q 33
  ip address 10.33.0.1 255.255.255.128
! Validation commands
show vlans
show ip route
```
