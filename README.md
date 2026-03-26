
# AIM

To connect computers in multiple networks using Open Shortest Path First Routing Protocol and to verify the connectivity between computers.

# EQUIPMENTS REQUIRED
1.Desktop Computer
2.Cisco Packet Tracer 5.0 Software
# IP ASSIGNMENT

<img width="1035" height="639" alt="Screenshot 2026-03-26 110349" src="https://github.com/user-attachments/assets/aa5ee255-6d9a-42b3-afa4-cd9e6364fb61" />

# NETWORK DIAGRAM

<img width="839" height="578" alt="Screenshot 2026-03-26 110401" src="https://github.com/user-attachments/assets/0327b314-74d9-485e-9736-557763db1987" />


# PROCEDURE
STEP 1: Open a Packet Tracer Software.
STEP 2: Drag two 2900 Switches, two Cisco 1800 Routers, four PC Terminals from tool bar and drop it in work area.
STEP 3: Connect all the PC Terminals and Routers through Switches as shown in the network diagram using CAT 6 Patch cables.
STEP 4: Configure IP address and Gateway in all PC Terminals.
STEP 5: Configure Delhi router IP address, save configuration and restart Delhi router. STEP 6: Configure Chennai router IP address, save configuration and restart Chennai router. STEP 7: Check the connectivity between the computers in network.
STEP 8: Configure OSPF in Delhi router, Save configuration and restart Delhi router.
STEP 9: Configure OSPF in Chennai router, Save configuration and restart Chennai router.
STEP 10: Verify the connectivity between PC Terminals in different networks using Ping command.
STEP 11: Check the routing table in Delhi router and Chennai router using show ip route command

# PROGRAM
Router Table 1:
Router0> enable 
Router0# configure terminal 
Router0(config)# interface FastEthernet0/0 
Router0(config-if)# ip address 192.168.1.1 255.255.255.0 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# interface Serial2/0 
Router0(config-if)# ip address 192.168.2.1 255.255.255.0 
Router0(config-if)# clock rate 64000 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# router ospf 1 
Router0(config-router)# router-id 1.1.1.1 
Router0(config-router)# network 192.168.1.0 0.0.0.255 area 0 
Router0(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router0(config-router)# exit 
Router0# write memory

Router Table:
Router1> enable 
Router1# configure terminal 
Router1(config)# interface FastEthernet0/0 
Router1(config-if)# ip address 192.168.3.1 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# interface Serial2/0 
Router1(config-if)# ip address 192.168.2.2 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# router ospf 1 
Router1(config-router)# router-id 2.2.2.2 
Router1(config-router)# network 192.168.3.0 0.0.0.255 area 0 
Router1(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router1(config-router)# exit 
Router1# write memory




# OUTPUT
Router Table 1:

<img width="1278" height="574" alt="Screenshot 2026-03-26 110428" src="https://github.com/user-attachments/assets/06e9052d-b2a7-4a84-9f38-2395cbfb4bfe" />

Router Table 2:

<img width="936" height="429" alt="Screenshot 2026-03-26 110440" src="https://github.com/user-attachments/assets/11496338-0389-43e9-a452-6dc319cf88d1" />




# RESULT
Thus the computers in multiple networks using Open Shortest Path First Routing Protocol is connected and the connectivity between the computers is verified.

