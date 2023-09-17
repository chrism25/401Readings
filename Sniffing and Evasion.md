# <p align="center"> How to defend from Sniffing
Initially sniffing was created to analyze and monitor traffic in order to resolve issues, but actors use it for their own gain to steal important information. 

### Types of Sniffing
There are 2 types of sniffing, active and passive. In one the actor has some interaction to get the data and in the other the actor just hides while the data is being collected by itself.

* Passive Sniffing: In this case the attacker places a device into a hub and is able to monitor all traffic. The hub simply receives and redirects all the information disregarding to whom it is intended.
* Active Sniffing: By using a switch the passive sniffing is avoided. However, an actor can flood the CAM table that the switch uses to know where to direct the traffic, with bogus requests. Once the table is full the switch can’t register the destinations and start acting like a hub, redirecting traffic to all ports. That’s how an actor can intercept the data as if it was with a hub. 

### Attack Implementations
* MAC flooding: Flooding the switch with MAC addresses so that the CAM table is overflowed and sniffing can be done
* DNS cache poisoning: Altering the DNS cache records so that it redirects the request to a malicious website where the attacker can capture all the traffic.
* Evil twin attack: The attacker sets up a DNS with the same  information of the victim’s and proceeds to change the victim’s DNS. The attacker DNS will now respond to all the requests  rerouting to any desired direction and the traffic can be easily sniffed.
* MAC spoofing: The actor sets up a device with the same MAC address from the ones acquired from the switch. Then all communication to that MAC address gets intercepted by the device set up with the sniffer.

### How to render sniffed information useless
There are anti-sniffer softwares that can detect sniffers, but depending on the complexity of the attack the sniffer might be able to evade them. These sniffers can be a hardware device, installed software, they can be at a DNS level or network nodes, etc. 
* HTTPS: All traffic will be encrypted as soon as it leaves its layer, this will render the information useless. HTTP shouldn;t be used since it is just plain text.
* TELNET: This is a protocol that a lot of people use but it doesn’t encrypt the traffic. SSH should be used instead which provides basically the same features but with encryption. 
* FTP: For the same reason mentioned above this service should be secured with the use of TLS or it can be replaced by using SFTP, which utilizes SSH. 
* POP3: Some users still use POP, which is also in plain text making it vulnerable, almost always new versions should be used because they are normally more secured.
* SNMP: Just as before this version is outdated, it is highly recommended to use more secure versions like SNMPV3.

### Sniffing Tools:
* Wireshark: Open source packet capturer and analyzer, with different tools to filter them and dissect them.
* dSniff:  This collection of tools is able to analyze and sniff passwords from various protocols like FTP, Telnet, POP, rLogin, SMB and many more.
* Microsoft Network Monitor: It monitors the network and can group more than 300 protocols. Some of its features are reassembly of fragmented messages and wireless monitor mode.
* Debookee: Paid tool that analyzes and monitors the network, it also catches traffic on subnets and in any IoT device. It has some useful modules like:
	* An SSL/TLS decryption module that specialized on secure protocols.
	* A network analysis module that scans connected devices, intercept traffic in a subnet, TCP port scanner, VoIP calls analyzer, Network analysis and monitoring of HTTP, DNS, TCP, DHCP protocols, among others.
	* A Wifi monitoring module that details access points in radio range, wireless client details and wifi statistics among others.

### Precaution Measures
* Trusted Networks: Actors take advantage of free public wifi, avoid these connections since they might be sniffed. What makes it worse is that an attacker can create its own network with an innocent or identical name in order to gain people’s trust.
* Encryption: All traffic leaving the device should be encrypted, this way if an actor gets a hold of it, the chances of the actor getting useful information out of it is minimal.
* Network Scanning and Monitoring: Administrators should constantly scan the network to detect any possible intrusion. Bandwidth monitoring is a technique that audits devices that are set to promiscuous mode.
