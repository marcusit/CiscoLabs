# Equipment

* 1 Switch
* 1 Router
* 2 Hosts

# Objective
1. Connect Host A to Switch 1 port 1. Connect Host B to Switch 1 port 2. Connect Router 1 to Switch 1 port 3.
2. Configure Host A with IP 10.22.0.2/25 and Host B with IP 10.33.0.2/25. Set the default gateway on both hosts to the first IP address in the subnet.
3. Create VLANs 22 and 33 on the switch. Assign port 1 to VLAN 22 and port 2 to VLAN 33.
4. Configure switch port 3 as a trunk port. Allow VLAN 22 and 33 on the trunk.
5. Setup Router 1 so that it can route packets between Host A and Host B's subnets.
6. Validate a working config by pinging Host B from Host A.

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/VLAN-Routing-01/Diagram01.png)
