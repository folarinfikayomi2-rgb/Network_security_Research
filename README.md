Network Security Threats Research Report

* Network security refers to the policies, technologies, processes and practices used to protect computer networks, connected devices and transmitted data from unauthorised access, misuse, modification and cyberattacks.

Modern organisations depend heavily on computer networks to communicate, store information and provide services. However, these networks face several security threats that can compromise sensitive information, disrupt operations and cause financial losses.

Understanding common network security threats is essential for identifying vulnerabilities, reducing risks and implementing effective security measures.

* The objectives of this summary are to:

* Identify and explain common network security threats.
* Understand how attackers exploit network vulnerabilities.
* Examine the potential impact of different network attacks.
* Explore methods used to detect, prevent and mitigate these attacks.
* Understand the importance of implementing effective network security controls.

The CIA Triad

The CIA Triad is a fundamental information security model consisting of three principles:

* Confidentiality: Ensures that sensitive information is accessible only to authorised individuals and systems.

* Integrity: Ensures that information remains accurate, complete and protected against unauthorised modification.

* Availability: Ensures that systems, networks and information remain accessible to authorised users when required.

These three principles provide a foundation for understanding the impact of network security attacks.


Section 2
Denial of Service (DoS) and Distributed Denial of Service (DDoS)

* What is a DoS attack?
  A Denial of Service (DoS) attack is a cyberattack designed to make a network, server or online service unavailable to legitimate users.
  An attacker achieves this by overwhelming the target with excessive traffic or requests, or by exploiting a vulnerability that causes the service to stop
  responding.

Example:
Imagine a bank's website can handle 5,000 requests per minute. An attacker sends an unusually large number of requests, consuming the server's resources. Legitimate customers may then be unable to access their accounts.

* What is a DDoS attack?
  A Distributed Denial of Service (DDoS) attack has the same objective as a DoS attack, but the malicious traffic   originates from multiple devices or sources.
  Attackers often use a network of compromised devices called a botnet.
  
* A botnet may consist of infected computers, routers, servers and Internet of Things (IoT) devices controlled remotely by an attacker.

  
* Difference between DoS and DDoS
  DoS is is often from a single source and the traffic is always from a single source also which makes the mitigation process less simpler and its often easier to trace. It can also disrupt services also. Meanwhine DDoS is from multiple sources and the traffic is from multiple sources and this makes the mitigation process more harder than DoS and harder to identify sources, Its impact can cause widespread disruption

* Common Types of DoS/DDoS attacks;
1. SYN Flood: This happens when an attacker sends multiple syn requests to a server without completeing the Three way handshake. This leaves the server with many half-open connection, consuming resources

2. UDP Flood: An Attacker sends large volumes of UDP packets to random or targeted ports, forcing the receiving system to process traffic and potentially generate responses

3. ICMP Flood: An attacker overwhelms a target with excessive ICMP packets, such as ping requests

4. HTTP Flood: An Attacker overwhelms a target with excessive HTTP requests to a web-server, consuming application and sserver responses

Detection And Prevention:
Organisations can reduce the impact of these attacks through:
* Rate Limiting
* Firewalls and Intrusion Prevention System(IPS)
* Traffic Monitoring
* DDoS protection services
* Traffic filtering

To Conclude;
DoS and DDoS attacks threaten the availability of network resources and online services. While DoS attacks typically originate from a single source, DDoS attacks uses multiple distributed sources, making them difficult to mitigate.

Organisations shoull implement appropriate network monitoring, traffic filtering and intrusion prevention systems mechanisms to maintain service availability


Section 2,
MITM(Man-In-The-Middle) attacks
A Man-in-the-middle) attack occurs when an attacker secretly positions themselves between two communicating parties and intercepts, monitors or modifies the information being exchanged

Two parties may beleive they are communicating directly, meanwhile an attacker sits between them and sees what both parties are communicating

* How a MITM attack works
An MITM attack typically follows this pattern;
1. Interception: the attacker positions themselves between two communicating devices.
2. Monitoring: The attacker captures information being exchanged.
3. Manipulation: The attacker Modifies messages or redirect communications.
4. exploitation: The attacker may steal credentials, sensitive information or session data.

For example, imagine someone connects to an unsecured network public wifi network to access their email. An attacker on the same network may attempt to intercept their communications and obtain sensitive information

* Common MITM attack techniques
1. ARP Spoofing (ARP Poisoning)
Address Resolution Protocol (ARP) is used to map IP addresses to MAC addresses within a local network.
An attacker sends falsified ARP messages to associate their MAC address with another device's IP address, often the default gateway.
This can redirect network traffic through the attacker's device.

3. DNS Spoofing
An attacker manipulates DNS responses or records to redirect users from legitimate websites to malicious destinations.
For example, a user attempts to visit their bank's website but is redirected to a fraudulent website designed to steal login credentials.

5. Rogue Wi-Fi Access Points
An attacker creates a malicious wireless access point that imitates a legitimate Wi-Fi network.
Users who connect may expose their network traffic to interception.

7. SSL Stripping
An attacker attempts to downgrade a connection from HTTPS to HTTP, potentially exposing information that would otherwise be encrypted.
Modern HTTPS protections, including HSTS, help prevent this technique.

* Impact of MITM attacks
* MITM attacks can result in:
* Theft of usernames and passwords.
* Exposure of sensitive personal information.
* Financial fraud.
* Session hijacking.
* Modification of transmitted information.
* Unauthorised access to systems and accounts.


*  Detection and prevention
* Organisations and individuals can reduce MITM risks through:
* Using HTTPS and valid TLS certificates.
* Avoiding unsecured or suspicious public Wi-Fi networks.
* Implementing strong Wi-Fi encryption such as WPA3.
* Using VPNs on untrusted networks where appropriate.
* Implementing certificate validation.
* Using network monitoring and intrusion detection systems.
* Enabling HSTS on supported websites.
* Implementing Dynamic ARP Inspection on managed networks where appropriate.

* Conclusion
 Man-in-the-Middle attacks compromise the confidentiality and integrity of communications by allowing attackers    to intercept or manipulate information exchanged between two parties.

 * Strong encryption, proper network configurations, certificatte validaation and continous monitoring are essential for reducing the risk of these attacks



**Section 4
* IP Spoofing
  IP spoofing is a cyberattack technique in which an attacker modifies the source IP address in an IP packet to make it appear as though the packet originated froma another device. Normally, when a device sends data across a network, its IP packet contains a source IP address identifying where the packet came from. An attacker can manipulate this address to disguise the true origin of the traffic

* How does IP Spoofing Work:
  1. Selecting a False IP address: The attacker chooses an IP address To Impersonate.
  2. Packet Manipulation: The attacker Modifies the source IP in Outgoing IP packets.
  3. Transmission: The packets are transmitted with a forged source address.
  4. Deception: The recieving System sees the falsified source address, which may make identifying the main sender difficult

  * IP spoofing changes the source address, but it does not give the attacker acess to the device's address being impersonated
 
  * Common Types of IP spoofing
  1. Blind spoofing: The attacker sends packets using a forges source IP address without being able toobserve The responses from the target
  2. Non-Blind Spoofing: The attacker can observe network traffic and potentially use that information to make spoofed communication more convincing
  3. IP Spoofing in DDoS Attacks: Attackers may forge fake source IP addresses to disguise the origin of malicious traffic or make it harder to filter network traffic

  * Impact of IP spoofing;
  1. Conceals the actual source of the network Traffic
  2. Makes Network investigations more difficult
  3. can be used in reflection and amplifications attacks
  4. can facilitate certain forms of unauthorized access where other weaknesses exist
  5. can undermine trust in IP-based access control
 
  * Detection and Prevention;
  1. Ingress Filtering: Checking incoming traffic to prevent packets with invalid or unexpected source addresses
  2. Egress filtering: Checking Outgoing traffics from leaving a network with forged source addresses
  3. Access control Lists: Filtering traffic according to network security policies
  4. Network Monitoring: Identifying unusual source addresses and taffic patterns
  5. Unicast Reverse Path Fowarding (uRPF): Checking whether the routing table provides a valid return path for a packet's source address
  6. Firewalls: Applying appropriate source-address filtering rules
  
  To Conclude; IP spoofing involves falsifying the source IP of network packets to disguise their origin. It if frequently associated with DDoS attacks and other network-based attacks.
  Implementing ingress and egress filtering,network Monitoring and appropriate firewall policies helps organisations reduce the risks associated with IP spoofing.
  
  
