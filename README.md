# Deep In Net Project with Cisco Packet Tracer

## Table of Contents

1. [Overview](#overview)  
2. [Objectives](#objectives)  
3. [Prerequisites](#prerequisites)  
4. [Exercise 1: Basic PC Communication](#exercise-1-basic-pc-communication)  
5. [Exercise 2: Switches and Hubs](#exercise-2-switches-and-hubs)  
6. [Exercise 3: Static and Dynamic Networking with Servers](#exercise-3-static-and-dynamic-networking-with-servers)   
8. [Exercise 5: Communication Across Subnets with a Switch and Router](#exercise-5-communication-across-subnets-with-a-switch-and-router)  
9. [Exercise 6: Routing Between Subnets](#exercise-6-routing-between-subnets)  
10. [Exercise 7: Expanded Network Communication](#exercise-7-expanded-network-communication)  
11. [Exercise 8: Multi-Subnet Communication](#exercise-8-multi-subnet-communication)

---

## Overview

This project comprises eight exercises designed to introduce you to the Cisco Packet Tracer and teach fundamental networking concepts. As a cloud and DevOps student, this project will strengthen your understanding of networking devices, protocols, and troubleshooting methods.

[Back to Top](#table-of-contents)

---

## Objectives

- Understand networking devices and their configurations.
- Use essential services and protocols.
- Learn the OSI model and its role in network communication.
- Master important Linux networking commands.
- Build and troubleshoot networks using Cisco Packet Tracer.

[Back to Top](#table-of-contents)

---

## Prerequisites

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) on your system.
2. Familiarize yourself with the CLI interface for device configuration.
3. Avoid using subnet calculators for manual practice.
4. Be ready to debug connectivity issues via CLI commands.

[Back to Top](#table-of-contents)

---

## Exo 1: Basic PC Communication

[View Exercise 1 Details](#exercise-1-basic-pc-communication)

---

## Exo 2: Switches and Hubs

[View Exercise 2 Details](#exercise-2-switches-and-hubs)

---

## Exo: Static and Dynamic Networking with Servers

[View Exercise 3 Details](#exercise-3-static-and-dynamic-networking-with-servers)

---

## Exo 4: PC Communication Through a Router

[View Exercise 4 Details](#exercise-4-pc-communication-through-a-router)

---

## Exo 5: Communication Across Subnets with a Switch and Router

[View Exercise 5 Details](#exercise-5-communication-across-subnets-with-a-switch-and-router)

---

## Exo 6: Routing Between Subnets

[View Exercise 6 Details](#exercise-6-routing-between-subnets)

---

## Exo 7: Expanded Network Communication

[View Exercise 7 Details](#exercise-7-expanded-network-communication)

---

## Exo 8: Multi-Subnet Communication

[View Exercise 8 Details](#exercise-8-multi-subnet-communication)

[Back to Top](#table-of-contents)

--- 

The links can be navigated directly when rendered in Markdown-supported platforms like GitHub, GitLab, or a Markdown viewer.
---

## Exercise 1: Basic PC Communication

### **Scenario**
Create a network where:
- **PC0** can communicate with **PC1**.
- **PC2** can communicate with **PC3**.
- **PC4** can communicate with **PC5**.

### **Steps**

1. **Set Up the Network**:
   - Drag and drop six PCs into the workspace.
   - Connect each pair with a **straight-through RJ-45 cable** using **FastEthernet** ports.

2. **Configure IP Addresses**:
   - Assign static IP addresses as follows:
     - **PC0**: 192.168.1.3/24 
       **PC1**: 192.168.1.4/24
     - **PC2**: 192.168.13.84/29 
       **PC3**: 192.168.13.82/29
     - **PC4**: 192.168.13.254/29 
       **PC5**: 192.168.13.250/29

3. **Verify Connectivity**:
   - Use the `ping` command in the CLI to test connectivity between each pair.

### **Knowledge Questions**  
1. **What is an RJ-45 cable?**  
   An RJ-45 cable is a type of Ethernet cable with 8 pins used to connect network devices.

2. **Difference Between Straight-Through and Crossover RJ-45 Cables**:  
   - **Straight-through** cables connect different devices, like a PC to a switch.  
   - **Crossover** cables connect similar devices, like PC-to-PC or switch-to-switch. [Back to Top](#table-of-contents)
---

## Exercise 2: Switches and Hubs

### **Scenario**
Set up a network where:
- All computers connected to the **Switch** communicate.
- All computers connected to the **Hub** communicate.

### **Steps**

1. **Set Up the Devices**:
   - Drag and drop 10 PCs, one switch, and one hub.
   - Connect 5 PCs to the **Switch** and the other 5 PCs to the **Hub** using **straight-through RJ-45 cables**.

2. **Configure IP Addresses**:
   - Assign static IPs:
     - **Switch-connected PCs**:
       - S-PC1: 192.168.1.1/24  
       - S-PC5: 192.168.1.5/24
     - **Hub-connected PCs**:
       - H-PC1: 192.168.1.193/27  
       - H-PC5: 192.168.1.201/27

3. **Test Connectivity**:
   - Use the `ping` command to test communication within the same device group.

### **Knowledge Questions**
1. **Function of a Switch**:  
A switch connects devices within the same network and forwards packets to the intended recipient based on MAC addresses.

   - Operates at Layer 2 (Data Link Layer) of OSI model
   - Intelligently forwards packets to specific destinations
   - Uses MAC address table for efficient data routing
Reduces network congestion by targeted packet forwarding
   - Provides better performance and security

2. **Function of a Hub**:  
   A hub broadcasts data to all connected devices without distinguishing recipients.

   - Operates at Layer 1 (Physical Layer) of OSI model
   - Broadcasts all incoming data to every connected device
   - No intelligence in packet routing
   - Creates more network noise
   - Less efficient and less secure

3. **OSI Model Layers**:  
   - **Switch**: Layer 2 (Data Link Layer).  
   - **Hub**: Layer 1 (Physical Layer).
 [Back to Top](#table-of-contents)
---

## Exercise 3: Static and Dynamic Networking with Servers

### **Scenario**
Set up a network with the following requirements:
1. All servers must have **static IPs**.
2. **DHCP Server** assigns IPs to all PCs.
3. **HTTPS Server** must display a "hello" message, and **HTTP** must be disabled.
4. **DNS Server** maps domain names:
   - `deep-in-net.local` → `192.168.1.99`
   - `deep-in-net.com` → `deep-in-net.local`
5. Configure an **FTP server**:
   - Create a user: `deepinnet` with **RWDNL** access.

### **Steps**

1. **Set Up the Network**:
   - Drag and drop:
     - 6 PCs  
     - 4 Servers (name them HTTPS, DNS, FTP, DHCP).  
   - Connect all devices to a **Switch** using **straight-through cables**.

2. **Configure Static IPs for Servers**:
   - HTTPS Server: 192.168.1.99/24
   - FTP Server: 192.168.1.100/24  
   - DNS Server: 192.168.1.101/24  
   - DHCP Server: 192.168.1.102/24  
   default gateway: 192.168.1.1

3. **Configure HTTPS Server**:
   - Disable HTTP.
   - Enable HTTPS 
   - Modify index.html and set the homepage to display "hello."

4. **Configure FTP Server**:
   - Set the service FTP on.
   - Create user: `deepinnet` with RWDNL permissions.

5. **Configure DNS Server**:
   - Set the service DNS on.
   - Map `deep-in-net.local` to `192.168.1.99`.
   - Create a CNAME record for `deep-in-net.com` pointing to `deep-in-net.local`.

6. **Configure DHCP Server**:
   - Set the service DHCP on.
   - Assign a DHCP pool:
     - Network: 192.168.1.10  
     - Subnet Mask: 255.255.255.0  
     - Gateway: 192.168.1.1  
   
   - Go to the pcs and set DHCP instead of static on ip configuration

7. **Verify Configurations**:
   - Use a web browser to visit `https://deep-in-net.com`.
   - Test FTP connectivity with user credentials.

### **Knowledge Questions**
1. **Server in Networking**:  
   A server provides services like file storage, web hosting, and DHCP to clients in a network.

   **Analogy: Imagine a server as a specialized computer that's like a dedicated service provider in a digital city. Just as a restaurant prepares and serves food to customers, a server provides specific services to other computers (clients) on a network.**


2. **DHCP**:  
   Automatically assigns IP addresses and network settings to devices(gateway, subnet info).


   Port: 67/68 (server/client) 


   Layer: 4 - Transport

   **Analogy: It's like a hotel's check-in desk automatically assigning room numbers and providing Wi-Fi credentials to new guests.**

3. **DNS**:  
   Translates domain names to IP addresses for easier access.


   Port: 53


   Layer: 4 - Transport

   **Analogy: DNS is like the internet's global phonebook. It translates human-readable domain names (like www.example.com) into computer-readable IP addresses (like 192.0.2.1).**

4. **HTTP vs HTTPS**:  HTTP is a communication protocol for transmitting data between web browsers and web servers. It defines how messages are formatted and transmitted. (OSI Model Layer 7 (Application Layer))
   - **HTTP**: Unsecured, plain-text communication. 



   Port: 80 
   - **HTTPS**: Encrypted communication for secure data transfer.



   Port: 443 


   Layer: 7 - Application

   **Analogy: HTTP is like sending a postcard - anyone can read its contents during transmission. If HTTP is a postcard, HTTPS is a sealed, tamper-proof envelope with a unique seal.**

5. **FTP**:  
   FTP is a standard network protocol used for transferring files between a client and a server. Basically, a protocol for transferring files between devices.



   Port: 21 (Control? auth) & 20 (Data)


   Layer: 4 - Transport

6. **TCP vs UDP**:  
   - **TCP (Transmission Control Protocol)**: Reliable, connection-oriented protocol.  
   - **UDP (User Datagram Protocol)**: Faster, connectionless protocol.

   ### **Comparison of TCP and UDP**
| **Feature**         | **TCP**                        | **UDP**                     |
|----------------------|--------------------------------|-----------------------------|
| **Connection**       | Connection-oriented  | Connectionless     |
| **Reliability**      | Reliable  | Unreliable  |
| **Speed**            | Slower (due to overhead)      | Faster  |
| **Use Cases**        | Web, email, file transfers    | Streaming, gaming, DNS      |
| **Error Handling**   | Built-in  | None  |
| **OSI Model Layer**  | Transport Layer (Layer 4)   | Transport Layer (Layer 4)  |

---

   **Analogy: UDP is like sending a quick postcard - fast, but no guarantee it will arrive intact. TCP is like a registered mail service that confirms each part of your package arrives correctly.**

7. **Ports and OSI Model Layers**:  
   A **port** is a logical endpoint in a network communication system that enables devices to identify specific processes or services running on a host. It works in conjunction with IP addresses to facilitate communication between devices.
 
 ---

### **Key Points About Ports**
1. **OSI Layer**: Ports operate at the **Transport Layer (Layer 4)** of the OSI model.
   - **TCP** and **UDP** protocols use ports to distinguish different services.

2. **Purpose**:
   - Allow multiple services to run on a single device without conflict.
   - Help route network traffic to the correct application or process.

3. **Range of Port Numbers**:
   - **Well-Known Ports (0–1023)**: Reserved for common protocols and services (e.g., HTTP, FTP).
   - **Registered Ports (1024–49151)**: Assigned to user applications and specific services.
   - **Dynamic or Private Ports (49152–65535)**: Used temporarily by client-side applications for communication.

---

### **Common Ports**
| **Port Number** | **Protocol** | **Service**                    |
|------------------|--------------|---------------------------------|
| 20, 21           | TCP          | FTP (File Transfer Protocol)   |
| 22               | TCP          | SSH (Secure Shell)             |
| 23               | TCP          | Telnet                         |
| 25               | TCP          | SMTP (Email Sending)           |
| 53               | TCP/UDP      | DNS (Domain Name System)       |
| 80               | TCP          | HTTP (Web Browsing)            |
| 443              | TCP          | HTTPS (Secure Web Browsing)    |
| 67, 68           | UDP          | DHCP (Dynamic Host Configuration Protocol) |
| 110              | TCP          | POP3 (Email Retrieval)         |
| 143              | TCP          | IMAP (Email Retrieval)         |
| 161, 162         | UDP          | SNMP (Network Management)      |

---

### **Analogy**:
Think of a port as a door to a house (the device). 
- The **IP address** is like the address of the house, identifying the location.
- The **port number** is like the specific room in the house where a task is being performed (e.g., the kitchen for cooking, the study for working).

---

### **How Ports Work in Network Communication**
1. A client sends a request to a server at a specific IP address and port number.
2. The server listens on that port for incoming requests.
3. The server processes the request and sends a response back to the client using the same port.


8. **DNS Records**:  
   
- **A Record**: Maps domain to IPv4 address
- **AAAA Record**: Maps domain to IPv6 address
- **CNAME Record**: Creates an alias for another domain
- **MX Record**: Specifies mail servers
- **TXT Record**: Stores text information
- **NS Record**: Specifies authoritative name servers
 [Back to Top](#table-of-contents)
---

## Exercise 4-5: PC Communication Through a Router

### **Scenario**
Create a network where:
- Two PCs can communicate with each other through a router.

### **Steps**

1. **Set Up the Network**:
   - Drag and drop 2 PCs and 1 router.
   - Connect each PC to the router using **Cross over RJ-45 cables** and their respective **FastEthernet** ports.

2. **Configure IP Addresses**:
   - Assign IP addresses as follows:
     - **PC0**: 192.168.1.2/30, Gateway: 192.168.1.1  
     - **PC1**: 192.168.2.2/30, Gateway: 192.168.2.1  
   - On the router, configure the following:
     - Interface **FastEthernet0/0**: 192.168.1.1/30  
     - Interface **FastEthernet0/1**: 192.168.2.1/30

3. **Enable Router Interfaces**:
   - In the CLI, run:
     ```plaintext
     Router> enable
     Router# configure terminal
     Router(config)# interface FastEthernet 0/0
     Router(config-if)# ip address 192.168.1.1 255.255.255.252
     Router(config-if)# no shutdown
     Router(config)# interface FastEthernet 0/1
     Router(config-if)# ip address 192.168.2.1 255.255.255.252
     Router(config-if)# no shutdown
     ```

4. **Test Connectivity**:
   - Use the `ping` command to test connectivity between **PC0** and **PC1**.

### **Knowledge Questions**
1. **What is a Router and Its Role?**  
   A router connects different networks and directs data packets between them using IP addresses(Layer 3 (Network Layer)).

2. **Switch vs Router**:  
   - **Switch**: Operates within the same network using MAC addresses.  
   - **Router**: Connects multiple networks using IP addresses.

3. **Default Gateway**:  
   A default gateway is a device (usually a router) that routes traffic from a local network to other networks.
 [Back to Top](#table-of-contents)
---

## Exercise 6-7: Routing Between Subnets

### **Scenario**
- PCs in **Subnet 1** and **Subnet 2** can communicate.

### **Steps**

1. **Set Up the Network**:
   - Same as **Exercise 5** setup.

2. **Configure Routing Table (Static Routing)**:
   - If additional routers are involved, configure static routes:
     ```plaintext
     Router0(config)# ip route 192.168.2.0 255.255.255.0 10.10.0.2  
     Router1(config)# ip route 192.168.1.0 255.255.255.0 10.10.0.1 
     ```

3. **Test Connectivity**:
   - Confirm with `ping`.

### **Knowledge Questions**
1. **Routing Table**:  
   A routing table is a data set in routers that contains paths, including IP ranges and gateways, used to direct network traffic.
 [Back to Top](#table-of-contents)
---

## Exercise 8: Multi-Subnet Communication

### **Scenario**
- Communication across **Subnet 1**, **Subnet 2**, and **Subnet 3**.

### **Steps**

1. **Set Up the Network**:
   - Drag and drop PCs, three switches, and a router.

2. **Configure Subnets**:
   - **Subnet 1**: 192.168.1.192/26 
   - **Subnet 2**: 192.168.2.0/24  
   - **Subnet 3**: 192.168.3.160/28 
   - Assign appropriate IPs and gateways.

3. **Configure dynamic Routing**:
   ```plaintext
   Router(config)#router rip 
   Router(config-router)#version 2
   Router(config-router)# network 10.10.0.0
   Router(config-router)#network 192.168.1.192
   ```

4. **Test Connectivity**:
   - Use `ping` to confirm connectivity across all subnets.
 [Back to Top](#table-of-contents)
---
