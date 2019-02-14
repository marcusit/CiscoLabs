## Switch 1
```
! Disable routing if using a L3 switch
no ip routing
! Configure the switch ports
int e0/0
  switchport mode access
  switchport access vlan 2
int e0/1
  switchport trunk encapsulation dot1q
  switchport mode trunk
  switchport nonegotiate
  switchport trunk allowed vlan 1-2
  switchport trunk native vlan 1
int e0/2
  switchport mode access
! Validation commands
show vlan brief
show int e0/1 switchport
show int trunk
```
## Switch 2
```
! Disable routing if using a L3 switch
no ip routing
! Create the virtual interface
int vlan 1
  ip address 192.168.1.1 255.255.255.0
  no shutdown
! Configure the switch port
int e0/0
  switchport mode access
! Set the default gateway
ip default-gateway 192.168.1.254
```
## Router 1
```
! Configure the physical interface
int fa0/0
  no shutdown
  no ip address
! Create and configure the sub interfaces
int fa0/0.1
  encapsulation dot1Q 1 native
  ip address 192.168.1.254 255.255.255.0
int fa0/0.2
  encapsulation dot1Q 2
  ip address 10.10.0.254 255.255.0.0
! Validation commands
show vlans
show ip route
```
