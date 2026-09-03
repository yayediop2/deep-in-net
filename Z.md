Certainly! Let's go through the first three exercises and create a README.md file to document the concepts and steps involved.

# Deep-in-Net Project

## Exercise 1: Basic PC Connectivity

### Objectives
- Connect PCs in pairs and ensure communication between them.
- Understand the use of crossover and straight-through cables.

### Network Topology
The network topology for Exercise 1 is as follows:

![Exercise 1 Topology](https://learn.zone01dakar.sn/git/root/public/media/branch/master/subjects/devops/deep-in-net/pictures/ex01.jpg)

### Configuration Steps
1. Add 6 PCs (PC0 through PC5) to the Packet Tracer workspace.
2. Connect the PCs in pairs using crossover cables:
   - PC0 to PC1
   - PC2 to PC3
   - PC4 to PC5
3. Configure the IP addresses for each PC pair:
   - PC0: 92.168.1.3/24
   - PC1: 192.168.1.82/24
   - PC2: 192.168.13.82/20
   - PC3: 192.168.13.83/20
   - PC4: 192.168.13.254/20
   - PC5: 192.168.13.253/20
4. Test the connectivity between the PC pairs by pinging from one PC to the other.

### Knowledge
1. **RJ-45 Cable**: RJ-45 is the standard connector used for Ethernet networking, with 8 pins that carry data between network devices.
2. **Crossover vs. Straight-Through Cables**:
   - Crossover cables are used to connect similar devices (e.g., PC to PC, Switch to Switch) by crossing the transmit and receive pins.
   - Straight-through cables are used to connect different types of devices (e.g., PC to Switch, Router to Switch) by connecting the pins directly.

## Exercise 2: Switches and Hubs

### Objectives
- Connect PCs to a switch and a hub.
- Understand the function and differences between a switch and a hub.

### Network Topology
The network topology for Exercise 2 is as follows:

![Exercise 2 Topology](https://learn.zone01dakar.sn/git/root/public/media/branch/master/subjects/devops/deep-in-net/pictures/ex02.jpg)

### Configuration Steps
1. Add a Switch and a Hub to the Packet Tracer workspace.
2. Connect the PCs to the Switch and Hub as shown in the topology.
3. Observe the communication patterns between the PCs connected to the Switch and the Hub.

### Knowledge
1. **Switch**: A switch is a network device that connects multiple devices and forwards data packets between them based on their destination MAC addresses. Switches operate at the data link layer (Layer 2) of the OSI model.
2. **Hub**: A hub is a network device that connects multiple devices and broadcasts all received data packets to all connected devices. Hubs operate at the physical layer (Layer 1) of the OSI model.
3. **Difference between Switch and Hub**: Switches are more efficient and intelligent than hubs, as they can direct traffic based on MAC addresses, whereas hubs simply broadcast all received data to all connected devices.

## Exercise 3: Servers and Services

### Objectives
- Set up various servers with specific services and configurations.
- Understand the role of servers in a network and the function of different network services.

### Network Topology
The network topology for Exercise 3 consists of multiple servers and clients, as shown in the following image:

![Exercise 3 HTTPS Server](https://learn.zone01dakar.sn/git/root/public/media/branch/master/subjects/devops/deep-in-net/pictures/ex03.jpg)

### Configuration Steps
1. Add the necessary servers (HTTPS Server, FTP Server, DHCP Server, DNS Server) to the Packet Tracer workspace.
2. Configure the servers with the following requirements:
   - HTTPS Server:
     - Display a "Hello" message
     - Disable HTTP
   - FTP Server:
     - Create a user account with the name "deepinnet" and provide RWDNL access
   - DHCP Server:
     - Assign IP addresses to all PCs
   - DNS Server:
     - Map "deep-in-net.local" to IP address 192.168.1.99
     - Map "deep-in-net.com" to "deep-in-net.local"
     - Ensure that "https://deep-in-net.com" redirects to the HTTPS server
3. Test the functionality of each server and its associated services.

### Knowledge
1. **Server**: A server is a computer or software program that provides a specific service or resource to other devices or users on a network.
2. **DHCP**: The Dynamic Host Configuration Protocol (DHCP) is a network service that automatically assigns IP addresses to devices on a network.
3. **DNS**: The Domain Name System (DNS) is a network service that translates human-readable domain names into machine-readable IP addresses, enabling communication on the internet.
4. **HTTP and HTTPS**: HTTP (Hypertext Transfer Protocol) is the standard protocol for web communication. HTTPS (Secure HTTP) is a version of HTTP that adds security by encrypting the communication.
5. **FTP**: The File Transfer Protocol (FTP) is a standard network protocol used for transferring files between computers over a network.
6. **TCP and UDP**: TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two main transport layer protocols used in network communication. TCP is connection-oriented and reliable, while UDP is connectionless and unreliable.
