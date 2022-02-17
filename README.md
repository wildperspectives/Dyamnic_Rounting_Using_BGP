# Dyamnic_Rounting_Using_BGP

Dynamic routing between autonomous systems can be achieved using Border Gateway Protocol (BGP).

Dynamic routing, also called adaptive routing, is a process where a router can forward data via a different route or given destination based on the current conditions of the communication circuits within a system. 

Border Gateway Protocol (BGP) is a standardized exterior gateway protocol designed to exchange routing and reachability information among autonomous systems (AS) on the Internet. The protocol is classified as a path vector protocol. The Border Gateway Protocol makes routing decisions based on paths, network policies, or rule-sets configured by a network administrator and is involved in making core routing decisions.

Steps to build and execute the project :
Select five PC’s
Connect the PC’s to the routers via cables
Set up autonomous systems comprising of PC’s and routers
Connect the routers via cables
Assign network ID for each connection
Configure the PC’s with IP address and gateway address
Configure the Routers with FastEthernet port IP address and Serial port IP address 
Configure the Routers with BGP protocol by giving in all the necessary commands via Command Line Interface (CLI).
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

Wait till every link turns to green, which is the confirmation of the successful connection of links
Transfer the message packets within an autonomous system and also across the autonomous systems and check for the status. We observe that the transfer of data in the form of message packets initially fails, but is successful at later stages
