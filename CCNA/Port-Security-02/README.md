# Equipment

* 1 Switch
* 4 Hosts

# Objective
1. Configure port security on the first switch port, with sticky MAC learning and a maximum of 2 MAC addresses retained. Ping Host B from Host A.
2. Disconnect Host A and connect Host C to the first switch port. Try to ping Host B again, which should succeed.
3. Validate that the switch port learned the two MAC addresses from Host A and Host C.
4. Disconnect Host C and connect Host D to the first switch port. Try to ping Host B again, which should fail.
5. Re-connect Host A to the first swich port and make sure that Host A can ping Host B again.
6. Re-configure the first switch port to block traffic from unknown MAC addresses, but not shut down the interface, as well as count the number of violations.
7. Disconnect Host A and connect Host D to the first switch port. Try to ping Host B again, and validate that the switchport remains up/up, and that the port security violation counter is incrementing.
8. Make sure that learned MAC addresses are retained after a switch reboot. Restart the switch to validate.

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/Port-Security-02/Diagram01.png)
