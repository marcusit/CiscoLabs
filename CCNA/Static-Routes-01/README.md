# Equipment

* 1 Switch
* 3 Routers
* 2 Hosts

# Objective
1. Refer to the diagram for port connectivity. For Router 2, if access to more than two interfaces is not possible then create an internal interface on the router with Host B's IP address, and use this interface in place of Host B.
2. Configure each device and interface referenced in the diagram with their respective IP addresses.
3. On Router 1 and Router 2 create a static route to the 10.22.0.10/24 network. On Router 3 create a static route two static routes to the 10.0.0.0/24 network, via Router 1.
4. Using administrative distances, adjust the static routes on Router 1, Router 2 and Router3 so that traffic will always flow over the path labeled "Fast" and utilize the "Slow" path only if the "Fast" path becomes unavailable.
5. Ping Host B from Host A. Validate on Router 1 that in inbound/outbound traffic counters are incrementing. Validate the opposite on Router 2, no traffic is expected over this path.
6. Disconnect port 1 and 2 on Router 1, or simply turn Router 1 off. Change the default gateway on Host A to 10.0.0.2 and validate that it can still ping Host B. Port 1 on Router 3 may need to be manually shut down in a lab environment if it remains in a up/up state after Router 1 is disconnected.
** Note: Outside of this lab we would configure redundant gateways so that Router 1 and Router 2 would share the same IP, to avoid having to make changes to end points. **

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/Static-Routes-01/Diagram01.png)
