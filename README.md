# Dyamnic_Rounting_Using_BGP

Dynamic routing between autonomous systems can be achieved using Border Gateway Protocol (BGP).

Dynamic routing, also called adaptive routing, is a process where a router can forward data via a different route or given destination based on the current conditions of the communication circuits within a system. 
Border Gateway Protocol (BGP) is a standardized exterior gateway protocol designed to exchange routing and reachability information among autonomous systems (AS) on the Internet. The protocol is classified as a path vector protocol. The Border Gateway Protocol makes routing decisions based on paths, network policies, or rule-sets configured by a network administrator and is involved in making core routing decisions.

Steps followed to build and execute the project :
1.Select five PC’s
2.Connect the PC’s to the routers via cables
3.Set up autonomous systems comprising of PC’s and routers
4.Connect the routers via cables
5.Assign network ID for each connection
6.Configure the PC’s with IP address and gateway address
7.Configure the Routers with FastEthernet port IP address and Serial port IP address 
8.Configure the Routers with BGP protocol by giving in all the necessary commands via Command Line Interface (CLI).
Router commands for configuring Router 0 :
Router>en
Router#conf t
Router(config)#router bgp 100
Router(config-router)#network 192.168.1.0
Router(config-router)#network 192.168.2.0
Router(config-router)#network 192.168.3.0
Router(config-router)#network 192.168.4.0
Router(config-router)#neighbor 192.168.2.2 remote-as 200
Router(config-router)#neighbor 192.168.5.1 remote-as 200
Router(config-router)#neighbor 192.168.4.2 remote-as 400
Router(config-router)#neighbor 192.168.6.1 remote-as 400
Router(config-router)#neighbor 192.168.3.2 remote-as 500
Router(config-router)#neighbor 192.168.8.2 remote-as 300
Router(config-router)#neighbor 192.168.10.1 remote-as 300

Similarly, remaining routers are configured
9.Wait till every link turns to green, which is the confirmation of the successful connection of links
10.Transfer the message packets within an autonomous system and also across the autonomous systems and check for the status. We observe that the transfer of data in the form of message packets initially fails, but is successful at later stages
