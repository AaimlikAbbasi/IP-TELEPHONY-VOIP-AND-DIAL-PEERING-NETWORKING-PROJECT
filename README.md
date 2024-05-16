
Requirements:

Department 	Phones	PCs	Printers
Finance	10	10	1
HR	10	10	1
Sales	10	10	1
ICT	10	10	1

PCs are connected to phones instead of switches, the network has four servers in the server area and configured servers are shared between all the users which are 
●	EMAIL
●	DNS
●	DHCP
●	HTTP



 

The IT manager emphasizes scalability and availability and hence you are required to provide a complete network infrastructure design and implementation.Following IP address will be used 
For Data: 192.168.100.0/24
For Voice 172.16.100.0/24
Between Routers: 10.10.10.0/24

 Explanation of each component:
1.	ROUTER :- each department is to have a VOIP enabled router with server-side LAN attached to the ICT department router .note use cisco 2811 router.
2.	SWITCHES:- each department has an access layer switch note cisco 2960 switch.
3.	Connections:-use serial connection between the router and a router than a straight cable between the router to switch ,switch to hosts ,phones to pcs.
4.	SUBNETS:- each department will be accessing two subnetworks ,for example data and voice subnets ,carry out appropriate subnetting.
5.	Basic setting:- configure basic device settings such as host names ,console password enable password and banner messages encrypt all passwords and disable IP domain lookup.
6.	DHCP Server :- for voice (voIP) use the representative router as DHCP server while for the data use the  DHCP server device at the server side site.
7.	VLANS :-Each department will be in two VLANS. One for the data and another for voice. All IP phones in the network should be in VLANS  100.
8.	INTER -VLAN Routing:- use OSPF as routing protocol to advertise routers on the routers.
9.	IP addressing:-  all devices in the network are expected to obtain an ip address dynamically from the respective DHCP servers while the devices in the server room are to be allocated  IP addressing statically.
10.	Routing protocols :- Use OSpf as routing protocol to advertise routes on the routers.
11.	Remote access:- configure SSH in all the routers for remote login.
12.	TELEPHONY SERVICES:- configure VOIP on the routers for remote login and dial numbers in  this format for departments,finance (1..),HR(2..),Sales(3..) and ICT(4.._ where 1.. Can be 101 to 199) and so on.
13.	Routing for VoIp :-configure dial-peering on the routers to allow IP phones from the different routers to communicate 
14.	Finance:-Test communication ,ensure everything configured is as working as expected








Topology:
![image](https://github.com/AaimlikAbbasi/IP-TELEPHONY-VOIP-AND-DIAL-PEERING-NETWORKING-PROJECT/assets/96013254/cd2e07fb-68bc-409c-943a-e9fb6d1e27a3)
Configuration Steps :-
1.	Network design and beautifications.
2.	Basic setting to all the devices plus ssh on the router
3.	VLANS assignment plus all access and truck ports on the switches.
4.	Subnetting and IP addressing
5.	Static IP address to server room devices
6.	DHCP server service devices configuration
7.	Configure DHCP for voice
8.	Inter Vlan routing on routers plus ip dhcp helper addresses
9.	OSPF on the routers
10.	Configure VOIP configuration in all routers 
11.	Dial peering configuration in all router
12.	Verifying and testing configuration

![image](https://github.com/AaimlikAbbasi/IP-TELEPHONY-VOIP-AND-DIAL-PEERING-NETWORKING-PROJECT/assets/96013254/c20703df-bfbb-4218-a5ac-fbc150a309b4)

