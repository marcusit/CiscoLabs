# Switch 1 config
```
! Find MAC address of Host A
show mac address-table
! Configure the first switch port
int e0/0
  switchport mode access
  switchport port-security
  switchport port-security mac-address aaaa.bbbb.cccc
! Re-enable the first switch port after host C triggers port security
int e0/0
  shutdown
  no shutdown
```
