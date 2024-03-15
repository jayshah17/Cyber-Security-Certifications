# Network Security

## Module 1: Understand Computer Networking

-  The purpose of all communications is to exchange information and ideas between people and organizations so that they can get work done.

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/60c42d2d-51b5-4b90-a62a-b0615f3e017a)

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/d7bcf706-bc93-42be-8830-18d4de1cf093)

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/7c753bbb-cb19-4801-8b1b-89f26a712ef4)

IPv4 is divided into 2 parts: Private IP Address and Public IP Address

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/db77e71e-a560-4409-baae-7d77e2164710)

 The loopback address is used to provide a mechanism for self-diagnosis and troubleshooting at the machine level. This mechanism allows a network administrator to treat a local machine as if it were a remote machine and ping the network interface to establish whether it is operational.
 - ::1 is the local loopback address, used the same as 127.0.0.1 in IPv4.

### What is WiFi?
Wireless networking is a popular method of connecting corporate and home systems because of the ease of deployment and relatively low cost. It has made networking more versatile than ever before. Workstations and portable systems are no longer tied to a cable but can roam freely within the signal range of the deployed wireless access points. 

- TCP/IP (as well as most protocols) is also subject to passive attacks via monitoring or sniffing. Network monitoring, or sniffing, is the act of monitoring traffic patterns to obtain information about a network.

Ports and Protocol 

 A logical port (also called a socket) is little more than an address number that both ends of the communication link agree to use when transferring data. 

- Well-known ports (0–1023): These ports are related to the common protocols that are at the core of the Transport Control Protocol/Internet Protocol (TCP/IP) model, Domain Name Service (DNS), Simple Mail Transfer Protocol (SMTP), etc.
- Registered ports (1024–49151): These ports are often associated with proprietary applications from vendors and developers. While they are officially approved by the Internet Assigned Numbers Authority (IANA), in practice many vendors simply implement a port of their choosing. Examples include Remote Authentication Dial-In User Service (RADIUS) authentication (1812), Microsoft SQL Server (1433/1434) and the Docker REST API (2375/2376).
- Dynamic or private ports (49152–65535): Whenever a service is requested that is associated with well-known or registered ports, those services will respond with a dynamic port that is used for that session and then released.

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/0b71e32b-fb10-4cb1-8183-2aeecd1f81cf)

### Module 2 Network Cyber Threat Attack

- Spoofing: An attack with the goal of gaining access to a target system through the use of a falsified identity. Spoofing can be used against IP addresses, MAC address, usernames, system names, wireless network SSIDs, email addresses, and many other types of logical identification.
- Phishing: An attack that attempts to misdirect legitimate users to malicious websites through the abuse of URLs or hyperlinks in emails could be considered phishing.
- Denial of Service: A denial-of-service (DoS) attack is a network resource consumption attack that has the primary goal of preventing legitimate activity on a victimized system. Attacks involving numerous unsuspecting secondary victim systems are known as distributed denial-of-service (DDoS) attacks.
- Virus:  A virus is a self-replicating piece of code that spreads without the consent of a user, but frequently with their assistanc
- Worms: Worms pose a significant risk to network security. They contain the same destructive potential as other malicious code objects with an added twist—they propagate themselves without requiring any human intervention.
- Trojan Horse: , ransomware often uses a Trojan to infect a target machine and then uses encryption technology to encrypt documents, spreadsheets and other files stored on the system with a key known only to the malware creator.
- On path attack: In an on-path attack, attackers place themselves between two devices, often between a web browser and a web server, to intercept or modify information that is intended for one or both of the endpoints. On-path attacks are also known as man-in-the-middle (MITM) attacks.
- Side Channel Attack: A side-channel attack is a passive, noninvasive attack to observe the operation of a device. Methods include power monitoring, timing and fault analysis attacks.
- Advanced Persitant threat: Advanced persistent threat (APT) refers to threats that demonstrate an unusually high level of technical and operational sophistication spanning months or even years. APT attacks are often conducted by highly organized groups of attackers.
- Insider Threat:  A trusted user who falls victim to a scam could be an unwilling insider threat.
- Ransomware: Malware used for the purpose of facilitating a ransom attack. Ransomware attacks often use cryptography to “lock” the files on an affected computer and require the payment of a ransom fee in return for the “unlock” code.


Identify threats and tools used to prevent it
![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/023d10b2-0723-42f1-9d34-49ddadc21584)

### Module 3: Understand Network Security Infrastructure



### Redundancy

- The concept of redundancy is to design systems with duplicate components so that if a failure were to occur, there would be a backup. This can apply to the data center as well. Risk assessments pertaining to the data center should identify when multiple separate utility service entrances are necessary for redundant communication channels and/or mechanisms.  

### Cloud
Cloud computing is usually associated with an internet-based set of computing resources, and typically sold as a service, provided by a cloud service provider (CSP). 
```
what is cloud : a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (such as networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.
```
- Types of cloud computing service models include Software as a Service (SaaS) , Platform as a Service (PaaS) and Infrastructure as a Service (IaaS).

Managed Service Provider(MSP)
A managed service provider (MSP) is a company that manages information technology assets for another company. 


Service-Level Agreement (SLA)
- The cloud computing service-level agreement (cloud SLA) is an agreement between a cloud service provider and a cloud service customer based on a taxonomy of cloud computing– specific terms to set the quality of the cloud services delivered. It characterizes quality of the cloud services delivered in terms of a set of measurable properties specific to cloud computing (business and technical) and a given set of cloud computing roles

### Network Design
- The objective of network design is to satisfy data communication requirements and result in efficient overall performance.

1. Network segmentation involves controlling traffic among networked devices. Complete or physical network segmentation occurs when a network is isolated from all outside communications, so transactions can only occur between devices within the segmented network.
2. A Demilitarized Network (DMZ) is a network area that is designed to be accessed by outside visitors but is still isolated from the private network of the organization. The DMZ is often the host of public web, email, file and other resource servers.
3. VLANs are created by switches to logically segment a network without altering its physical topology
4. A virtual private network (VPN) is a communication tunnel that provides point-to-point transmission of both authentication and data traffic over an untrusted network.
5. Defense in depth uses multiple types of access controls in literal or theoretical layers to help an organization avoid a monolithic security stance.
6. Network access control (NAC) is a concept of controlling access to an environment through strict adherence to and implementation of security policy.


### Defense in Depth

![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/e6f4ca8e-59dd-4cad-b5d7-c39a0958bc1a)

### Zero Trust

- Zero trust is an evolving design approach which recognizes that even the most robust access control systems have their weaknesses. It adds defenses at the user, asset and data level, rather than relying on perimeter defense. In the extreme, it insists that every process or action a user attempts to take must be authenticated and authorized; the window of trust becomes vanishingly small.

- ![image](https://github.com/jayshah17/Cyber-Security-Certifications/assets/76842630/c7ba1b93-152b-441a-b9c1-865e6a59478a)


### Network Access Control (NAC)

### Network Segmentation (Demilitarized Zone (DMZ))

- Network segmentation is also an effective way to achieve defense in depth for distributed or multi-tiered applications. The use of a demilitarized zone (DMZ), for example, is a common practice in security architecture.
- With a DMZ, host systems that are accessible through the firewall are physically separated from the internal network by means of secured switches or by using an additional firewall to control traffic between the web server and the internal network. 
