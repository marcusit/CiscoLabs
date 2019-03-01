## Router 1
```
! Configure the physical interfaces
int fa0/0
  ip address 10.0.0.1 255.255.254.0
  no shutdown
int fa0/1
  ip address 10.99.1.5 255.255.255.252
  no shutdown
! Setup RIP v2
router rip
  version 2
  no auto-summary
  network 10.0.0.0
  passive-interface fa0/0
```
## Router 2
```
! Configure the physical interfaces
int fa0/0
  ip address 10.1.1.1 255.255.255.0
  no shutdown
int fa0/1
  ip address 10.99.1.9 255.255.255.252
  no shutdown
! Setup RIP v2
router rip
  version 2
  no auto-summary
  network 10.0.0.0
  passive-interface fa0/0
```
## Router 3
```
! Configure the physical interfaces
int fa0/0
  ip address 10.99.1.6 255.255.255.252
  no shutdown
int fa0/1
  ip address 10.99.1.10 255.255.255.252
  no shutdown
int fa1/0
  ip address 1.1.1.1 255.255.255.252
  no shutdown
! Create the default route
ip route 0.0.0.0 0.0.0.0 1.1.1.2
! Setup RIP v2
router rip
  version 2
  no auto-summary
  network 10.0.0.0
  default-information originate
```
## Router 4
```
! Configure the physical interfaces
int fa0/0
  ip address 1.1.1.2 255.255.255.252
  no shutdown
! Configure the static route
ip route 10.0.0.0 255.0.0.0 1.1.1.1
! Validation commands
show ip protocols
show ip route rip
show ip rip database
```
