# Equipment

* 2 Switches
* 1 Router
* 1 Host

# Objective
1. Connect Host A to Switch 1 port 1. Connect Router 1 to Switch 1 port 2. Connect Switch 2 port 1 to Switch 1 port 3.
2. If using L3 switches disable routing on Switch 1 and Switch 2.
3. Configure Host A with IP 10.10.10.10/16, default gateway 10.10.0.254. Create a virtual interface (SVI) on Switch 2 and set the IP to 192.168.1.1/24, gateway 192.168.1.254.
4. Configure the link between Switch 1 and Switch 2 as well as Switch 1 port 1 as access ports. Assign Switch 1 port 1 to VLAN 2, leave all other ports with their default VLAN configuration (assumed VLAN 1).
5. Configure Switch 1 port 2 as a trunk port tagging VLAN 2, and set the native VLAN to 1.
6. Setup Router 1 so that i can route packets between Host A and Switch 2's SVI.
7. Validate that Host A can ping Switch 2's SVI IP address.

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/VLAN-Routing-02/Diagram01.png)
