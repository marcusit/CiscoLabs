## Router 1
```
! Configure the physical interfaces
int fa0/0
  ip address 10.0.0.1 255.255.255.0
  no shutdown
int f0/1
  ip address 10.99.1.1 255.255.255.252
  no shutdown
! Setup RIP v2
router rip
  version 2
  no auto-summary
  network 10.0.0.0
```
## Router 2
```
! Configure the physical interfaces
int fa0/0
  ip address 10.22.0.1 255.255.255.0
  no shutdown
int f0/1
  ip address 10.99.1.2 255.255.255.252
  no shutdown
! Setup RIP v2
router rip
  version 2
  no auto-summary
  network 10.0.0.0
```
