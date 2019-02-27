# Equipment

* 2 Routers
* 2 Hosts

# Objective
1. Connect Host A to Router 1 port 1. Connect Router 1 port 2 to Router 2 port 2. Finally, connect Router 2 port 1 to Host B.
2. Configure each device with the the IP addresses listed in the diagram. Each host needs a default gateway, set this to the IP address of the connected router.
3. Setup RIP v2 on both routers. Be sure to disable auto summarization. Router 1 should learn Host B's network and Router 2 should learn Host A's network.
4. Validate functionality by pinging Host B from Host A.

![alt text](https://github.com/marcusit/CiscoLabs/raw/master/CCNA/Router-RIP-01/Diagram01.png)
