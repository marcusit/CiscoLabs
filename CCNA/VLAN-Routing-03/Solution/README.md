## Switch 1
```
! Commands to enable L3 routing if needed
sdm prefer lanbase-routing
reload
ip routing
! Configure the switch ports
int e0/0
  switchport mode access
  switchport access vlan 30
int e0/1
  switchport mode access
  switchport access vlan 50
! Routing configuration
int vlan 30
  ip address 172.16.30.1 255.255.255.0
  no shutdown
int vlan 50
  ip address 172.16.50.1 255.255.255.0
! Validation commands
show ip int brief
show vlan brief
show ip route
```
