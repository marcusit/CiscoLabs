## Switch 1
```
! Disable routing if using a Layer 3 switch
no ip routing
! Configure the switch ports
int range e0/0 - 2
  switchport mode access
```
## Router 1
```
! Configure the physical interfaces
int fa0/0
  ip address 10.0.0.1 255.255.255.0
  no shutdown
int fa0/1
  ip address 10.99.1.1 255.255.255.252
  no shutdown
! Set static route
ip route 10.22.0.0 255.255.255.0 10.99.1.2
```
## Router 2
```
! Configure the physical interfaces
int fa0/0
  ip address 10.0.0.2 255.255.255.0
  no shutdown
int fa0/1
  ip address 10.99.2.1 255.255.255.252
  no shutdown
! Set static route
ip route 10.22.0.0 255.255.255.0 10.99.2.2
```
## Router 3
```
! Configure the phyisical interfaces
int fa0/0
  ip address 10.99.1.2 255.255.255.252
  no shutdown
int fa0/1
  ip address 10.99.2.2 255.255.255.252
  no shutdown
int fa1/0
  ip address 10.22.0.1 255.255.255.0
  no shutdown
! Set static routes
ip route 10.0.0.0 255.255.255.0 fa0/0
ip route 10.0.0.0 255.255.255.0 fa0/1 5
! Validation commands
show ip route
```
