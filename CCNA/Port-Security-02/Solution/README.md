## Switch 1
```
! Configure the first switch port
int e0/0
  switchport mode access
  switchport port-security
  switchport port-security mac-address sticky
  switchport port-security maximum 2
! Validate learned MAC addresses
show run int e0/0
show port-security
show port-security int e0/0
! Re-enable the first switch port after Host D triggers port security
int e0/0
  shutdown
  no shutdown
! Change port-security mode to not disable the port
int e0/0
  switchport port-security violation restrict
! Validate that the port was not disabled
show int e0/0
show port-security
show port-security int e0/0
! Save learned MAC addresses and reboot the switch
copy run start
reload
! Validate that previously learned MAC addresses are still present
show run int e0/0
```
