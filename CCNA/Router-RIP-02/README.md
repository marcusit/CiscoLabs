# Equipment

* 4 Routers
* 2 Hosts

# Objective
1. Connect the routers and hosts according to the diagram.
2. Configure each device with the the IP addresses listed in the diagram. Each host needs a default gateway, set this to the IP address of the connected router.
3. Setup RIP v2 on Router 1, 2 and 3. Be sure to disable auto summarization. For security reasons we do not want to send out RIP updates on the Host networks, so be sure to disable updates on those interfaces.
4. On Router 3, create a default route that points to 1.1.1.2. Configure Router 3 to re-destribute its default route using RIP to Router 1 and Router 2.
5. On Router 4 create a static route to 10.0.0.0/8 via 1.1.1.1.
6. Validate functionality by pinging Host B from Host A, as well as pinging Router 4 from Host A.
7. Validate that Router 1 and Router 2 learned a default route from Router 3.

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/Router-RIP-02/Diagram01.png)
