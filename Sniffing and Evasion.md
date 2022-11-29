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
