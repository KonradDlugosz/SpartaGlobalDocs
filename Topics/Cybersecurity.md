<div id="top"></div>
<div align="center">
    <h1 align= "center">Cyber Security</h1>
</div>
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#1. Introduction-to-Cyber-Security">Introduction to Cyber Security</a></li>
      <li><a href="#2. Virtualization">Virtualization</a></li>
      <li><a href="#3. Containerization ">Containerization </a></li>
      <li><a href="#4. Cryptography ">Cryptography</a></li>
      <li><a href="#5. Networking">Networking</a></li>
  </ol>
</details>





### 1. Introduction to Cyber Security

##### **What is cybersecurity ?** 

Cyber security's core function is to protect the **devices** we all use (smartphones, laptops, tablets and computers), and the **services** we access - both online and at work - from theft or damage.

It's also about preventing unauthorized access to the vast amounts of **personal information** we store on these devices, and online.

##### **Cybersecurity Cube (McCumber Cube)**

1. Desired goals : (CIA Triad)

   * Confidentiality : Unauthorized access is prevented 

   * Integrity : Data should not be modified
   * availability : Access should not be unavailable

2. Data states : 

   * Storage : Data At Rest (DAR) Data is in storage
   * Transmission : Data In Transit (DIT) Transferring data between systems
   * Processing : performing operations on data in order to achieve desired objective. 

3. Safeguards: 

   * Policy and practices : administrative controls/operations
   * Human factors: personnel 
   * Technology : software and hardware based solutions 

##### **Cybersecurity colors** 

1. Blue Team (The Defenders) : responsible for defense of security, damage control and incident response. 
2. Red Team (The Breakers/Attackers) : commissioned to perform "ethical hacking" on an organization.
3. White Team (The Admins) : responsible for refereeing an engagement between a Red Team and mock attackers and Blu Team of actual defenders of their enterprise's use on information systems.  
4. Yellow Team (The Builders) : responsible for developing the security system of an organization. 
5. Many more .... Depends on context and organization. 

##### **Hackers**

1. Black Hat Hackers - Attackers 
2. White Hat Hackers - Ethical hackers, hacking with permission.
3. Grey Hat Hackers - violate laws or typical ethical standards, but no malicious intent. 

##### **Testing**

1. White box testing : All information on the system.
2. Black box testing : No information on the system. 
3. Grey box testing : Some information. eg network design. 

##### **Essential Terms**

1. Asset: An asset is what we trying to protect.
2. Vulnerability : A vulnerability is a weakness or gap in our protection efforts.
3. Exploit : The way how hackers leverage vulnerabilities. 
4. Threat : A threat is what we are trying to protect against.
5. Risk : the intersection of assets, threats and vulnerabilities. 

##### **Causes of Vulnerabilities**

1. Design and development errors 
2. Poor system configuration 
3. Human errors
4. Connectivity : unsecure network like working for a café.
5. Complexity : too many entry points in large and complex system. 
6. Passwords : not strong passwords.
7. User input : invalidated input can cause vulnerability, SQL injection
8. Management : incorrect management could miss some important aspects of the systems. Delay to manage security can cause vulnerability,
9. Lack of training to staff 
10. Communication : Mobile users need to use secure network. For example VPN to connect to organization network.

##### **Cyber Attacks**

1. Un-targeted cyber attacks : phishing attacks which can be targeted for millions of people. 
2. Targeted cyber attacks : Specific attack for a company or individual. Spear phishing 

##### **Threat Actors**

​	*CYBER THREAT ACTOR > MOTIVATION* 

1. National-states > Geo political 
2. Cybercriminals > Profits 
3. Hacktivists > Ideological 
4. Terrorist groups > ideological violence 
5. Thrill-seekers > satisfaction/ attention 
6. Insider threats > discontent

##### **Cyber Threats** 

1. Malware : malicious software 
2. Spyware : form of malware that hides on devices providing real-time information. 
3. Phishing attack : lure individuals to gain information 
4. DDoS : aims to disrupt a computer network. Overload system. 
5. Ransomware : from of malware that denies access to a computer system or data until a ransom is paid. 
6. Zero day exploit : flaw that is unknow until it happens. 
7. Advanced persistent threats : unauthorized user gains access to a system or network and remain there for some time. 
8. Trojan : a backdoor to your system 
9. Wiper attacks : form of malware to wipe hard drive
10. Intellectual property theft 
11. Theft of money : access to bank account 
12. Data manipulation : aims to change data 
13. Data destruction : attempts to delete data 
14. Main in the middle attack : alters communication between two parties who believe they are communication with each other.
15. Rogue software : malware disguised as real software 
16. Unpatched software 
17. Natural disaster
18. Water holing : fake website 
19. Spear- phishing : sending emails to targeted individual that could contain an attachment with malicious software
20. Deploying a botnet : to deliver DDoS attack
21. Subverting the supply chain : to attack equipment or software being delivered to the organization. 

##### **Cyber Threat Surface** 

The attack surface of a software environment is the sum of the different points where an unauthorized user can try to enter data to or extract data from an environment. Keeping the attack surface as small as possible is a basic security measure.

##### **Cyber Kill Chain**

1. Reconnaissance : finding all information about the target
2. Weaponization : Write malware to leverage the vulnerability 
3. Delivery : deliver malware via web, email, USB etc.
4. Exploitation : exploiting vulnerability to execute code
5. Installation : installing the malware on the asset
6. Command and control (C2) : command channel for remote manipulation 
7. Actions on objectives : with access, accomplish your goal

##### **Securing during development**

Moving to the left in cybersecurity means that you should apply cybersecurity from beginning of product development. 

<p align="right">(<a href="#top">back to top</a>)</p>

### 2. Virtualization

##### **Why use virtualization?** 

* Variation between the development and production environment. 
* Development environment is where application is developed. 
* Production environment is where service is set it up. 
* Each might have different OS, updates etc.
* Solutions:
  *  Virtualization: Vagrant (used in development environment)
  * Containerization: Docker (used in production environment)

##### **What is virtualization ?**

* Is the process of separating a software from the hardware. 
* A virtual server means that server exists in virtual form physical.
* Hypervisor (Virtual machine monitor VMM) works as interface between the VMs and the host. eg. VirtualBox , vmware 

##### **Hypervisor types**

1. Type 1 Native/bare-metal : hardware > Hypervisors >> OS | APP 
2. Type 2 Hosted : hardware > operating system > Hypervisors >> OS | APP

##### **Why use vagrant ?** 

Configure virtual machine so that is exactly same across multiple devices so that all developers in a company have the same VM containing all apps and configuration. 

* A tool for building a managing virtual machine environments in single workflow.
* it lowers development setup time
* can mirror production environments on the developer machine 
* vagrant will create a virtual environment for each production environment. 
* vagrant is not hypervisor, its an automation tool that can be combined with hypervisor
* vagrant calls the hypervisor as a provider

<p align="right">(<a href="#top">back to top</a>)</p>

### 3. Containerization 

##### **What is container ?** 

* Containerization creates abstraction at an OS level that allows individual, modular and distinct functionality of the app to run independently 
* Several isolated workloads - the containers - can co-exist on a machine
* A unit of software that is lightweight but still bundles the code, its dependencies and the configuration altogether into a single image 
* Where can run ? 
  * On bare metal servers 
  * On top hypervisors 
  * In cloud infrastructure

##### **Benefits** 

* Useful in developing, deploying and testing modern distributed apps and microservices that can operate in isolated execution environments on same host machines.
* Developers don't need to write application code into different VMs operating different app components to retrieve compute, storage and networking resources.  Containers are not heavy on resources as VM. 
* A complete application component can be executed in its entirety within its isolated environment without affecting other app components or software. 
* no conflicts with libraries during execution. 

##### **Security** 

* Less secure than VM as they share kernel with host OS.
* Container share the same **kernel** with other containers 

##### **What is container engine ?** 

A container engine is a piece of software that accepts user requests, including command line options, pulls images, and from the end user's perspective runs the container. There are many container engines, including docker, RKT, CRI-O, and LXD.

##### **Docker**

* An open platform for developing, shipping and running applications.
* Enables separation of an applications from the infrastructure. 
* Components:

  * Server : Docker Server >
  * REST API >
  * Client : Docker command line interface 
* Container: 

  * Running instance of image
  * A **Docker container** is a virtualized run-time environment where users can isolate applications from the underlying system. These containers are compact, portable units in which you can start up an application quickly and easily.
* Image: 

  * In java case: Class with source code
  * A **Docker image** is an immutable (unchangeable) file that contains the source code, libraries, dependencies, tools, and other files needed for an application to run.
* Create image: 

  * Put all files of app into app folder
  * create Dockerfile 
    * FROM
    * COPY
    * RUN mvn clean package : run when image creating
    * ENTRYPOINT [Array of commands eg: `"mvn", "spring-boot:run"`] : run when container created
  
* To create image with different operating system have to create image using multi arch architecture 

<p align="right">(<a href="#top">back to top</a>)</p>

### 4. Cryptography 

##### **Introduction**

1. Encryption: transform original data into unrecognizable form
2. Decryption: transform from unrecognizable to readable format.

##### **Ciphers** 

Algorithm that consists of series of well defined step that can be followed as procedure when encrypting and decrypting: 

* Substitution cipher: Change characters with other characters. Shift alphabet by number of 3 or n.
  * Can be decrypted by using frequency analysis  
  * or simply guessed by generating all the keys 
* Transposition cipher 
  * letters are simply rearranged
  * key is number of lines you are using

##### **Asymmetric Encryption**

Different key to encrypt and decrypt data: 

1. **Private key :** should be kept secret

2. **Public key :** can be shared to others

Both keys can be use to encrypt and decrypt information but it gives other functionalities: 

* Encrypt using public key :  only decrypt by private key :  used for confidentiality

* Encrypt using private key :  only decrypt by public key : used for authentication and non-repudiation

Common algorithms: 

* Diffie-Hellman(DH) - 512, 1024 ,2048, 3072 or 4096
* Digital Signature Standard (DSS) - 512 to 1024
* RSA encryption algorithms - 512 to 2048
* EIGamal - 512 to 1024
* Elliptical curve techniques - smaller keys

##### **Symmetric Encryption**

Same key to encrypt and decrypt data. 

Types of algorithms: 

* Block ciphers: send in blocks of 64 bits or 128 bits ..
* Stream ciphers: send bit by bit

Common algorithms: 

* Data Encryption Standard 
* Triple Data Encryption Standard
* Advanced Encryption Standard (AES)
* Software-Optimized Encryption Algorithm (SEAL)

##### **Hashing** 

one way function - not encryption

* Used to verify and ensure **data integrity** 
* can also be used to verify authentication
* output is fixed size
* Hash message authentication code (HMAC) - used secret key with data to hash function
* Hashing password in shadow file : 
  * $ID $SALT $HASHED_PASSWORD
    ID 1 : MD5 
    ID 5 : SHA256
    ID 6 : SHA512 
    SALT : Random value
    HASHED_VALUE = hash(algorithm, SALT, PASSWORD)

##### **Password Salting** 

* Salt is a unique value that can be added to the end of the password to create a different hash value.

##### **Integrity**

Asymmetric Algorithms and Hashing:

* plain text + bob's Public key > Encryption Algorithm > Encrypted text : 

  *no integrity as anyone has bob's public key*

* hashed message + Alice's Private key > Encryption Algorithm > Encrypted hash: 

  *anyone can decrypt the message and check if the hash is the same as in the message*

##### **Public key Infrastructure**

Digital signatures are a mathematical technique used to provide authenticity, integrity and non-repudiation. 

* *Properties* : 

  * Authentic : provides proof that signer and no one else signed the document. 
  * Unalterable : after is signed, it cannot be altered. 
  * Not Reusable : the signature cannot be transferred between documents. 
  * Non-repudiated : the signed document is considered to be the same as a physical document. 

* *Standards* : 

  * Digital signature algorithm (DSA)
  * Rivest-Shamir Adleman Algorithm (RSA)
  * Elliptic curve digital signature algorithms (ECDSA)

* *Code signing* : 

  * Commonly used to provide assurance of the authenticity and integrity and software code. 
  * Provides assurance about the code :
    * Authentic
    * Not modified 
    * Non-repudiation of the act of publishing.

* *Digital Certificate* : 

  Its proof of ones identity, like an electronic passport that enables to securely exchange information over internet. It contains **public key**.

  * PKI Certificate < PKI Certificate Authority < Certificate Database
  * Digital certificate is used to publish public key and it's verified. 
  * Receiver should verify the certificate with the authority.
  * Certificate authority hierarchical. 

* *Certificate Revocation* : 

  * Certificate must be revoke sometimes, if private key has been compromised.
  * Methods: 
    * Certificate revocation list
    * Online Certification 

* *X.509 and Application* :

  * SSL/TLS : secure web servers use x.509v3 for website 
  * Web browsers : use x.509v3 to implment HTTPS cilent certificates 
  * S/MIME : User mail agents that support mail
  * EAP-TLS : Cisco switches can use certificate to authenticates end devices connecting to LAN 
  * IPSec 

<p align="right">(<a href="#top">back to top</a>)</p>

### 5. Networking

##### **OSI Model (Standard Model)**

1. **Physical Layer** : Media, signal, and binary transmission, related to hardware 

2. **Data link Layer** : physical addressing, protocol that work with physical layer, only recognized on local network inside your own network.

3. **Network Layer** : Path determination (routing decides to take the best path across a physical network) and logical addressing, connected on wider network like internet

4. **Transport Layer ** : End to end connections and reliability, 

   * TCP(connection-oriented) slower but more reliable
     * FTP 
     * Web browsing
     * Email
   * UDP (connectionless) faster but less reliable
     * Live streaming
     * Online games
     * VoIP
   * SSL not used, TLS commonly used

5. **Session** : Interhost communication, Session establishment in TCP 

6. **Presentation** : Data representation and encryption 

7. **Application Layer** : Network process to application, most of the time this layer contains session and presentation layer. 

   Application protocols: 

   * HTTP for web server (HTTPS = HTTP + SSL, TLS)
   * SMTP, IMAP for emails
   * FTP for file transferring 
   * DNS convert name to IP address 
   * SSH for remote machine

##### **TCP/IP Protocol Suite vs OSI model** 

This model is used more commonly in real life. 

* Application Layer : Application, Presentation, session
* Transport Layer : Transport
* Internet Layer : Network
* Network Access Layer : Data link, physical

##### **Encapsulation** 

* Passing down the stack. 
* Data > Segment > Packet > Frame > Bits
* Each step adds more information, encapsulates. 
* Once on destination, decapsulation at each step. 

##### **Transport Layer TCP vs UDP** 

* FTP : TCP , used across networks
* TFTP : UDP, used on same network with no authentication
* **When to use what ?** 
  * UDP : VoIP and DNS 
    * Fast 
    * Low overhead 
    * Does not require acknowledgements 
    * Does not resend lost data 
    * Delivers data as it arrives
  * TCP : SMTP/ IMAP and HTTP/HTTPS
    * Reliable 
    * Acknowledges data 
    * Resends lost data 
    * Delivers data in sequenced order

##### **Port numbers**

* Used to manage multiple connections or transitions at the same time.
* Source port number (Client) : port number used on source machine, allows to open multiple connections at the same time. 
* Destination port number (Server) : port number used on destination machine
* Server can offer more than one services at the same time eg. 
  * SSH service on port 22 
  * Web service on port 80
  * FTP on port 21
* Port Number Groups: 
  * Well-knows ports : 0-1023, reserved for common or popular services
  * Registered ports : 1,024 to 49,151
  * Private and/or Dynamic Ports : 49,152 to 65,535, ephemeral ports, temporal port client OS assigns port numbers when connecting to a service.
* Well known port numbers 
  * 20 TCP | FTP 
  * 21 TCP | FTP 
  * 22 TCP | SSH 
  * 23 TCP |Telnet 
  * 25 TCP | SMTP 
  * 53 UDP, TCP | DNS
  * 67 UDP | DHCP - server
  * 68 UDP | DHCP - client
  * 69 UDP | TFTP
  * 80 TCP | HTTP 
  * 110 TCP | POP3
  * 143 TCP | IMAP
  * 161 UDP | SNMP
  * 443 TCP | HTTPS 
  * 3306 TCP | MySQL

##### **Positional Numeral Systems** 

* A positional (numeral) system is the system used to write/express a number. 

* Positional nation means that a digit represents different values depending on the position the digit occupies in the sequence numbers. 

* In networking we use 3 numeral systems: 

  * Decimal numeral System (i.e. base 10 [0-9])

    | ==                 | Thousands | Hundreds | Tens | Ones |
    | ------------------ | --------- | -------- | ---- | ---- |
    | Radix              | 10        | 10       | 10   | 10   |
    | Position in Number | 3         | 2        | 1    | 0    |
    | Calculate          | 10^3      | 10^2     | 10^1 | 10^0 |
    | Position value     | 1000      | 100      | 10   | 1    |
    | Actual value       | 3000      | 200      | 10   | 0    |

  * Binary Numeral System (i.e. base 2 [0,1])

    | Radix              | 2       | 2      | 2      | 2      | 2     | 2     | 2     | 2     |
    | ------------------ | ------- | ------ | ------ | ------ | ----- | ----- | ----- | ----- |
    | Position in Number | 7       | 6      | 5      | 4      | 3     | 2     | 1     | 0     |
    | Calculate          | 2^7     | 2^6    | 2^5    | 2^4    | 2^3   | 2^2   | 2^1   | 2^0   |
    | Position value     | **128** | **64** | **32** | **16** | **8** | **4** | **2** | **1** |
    | 1 =                | 0       | 0      | 0      | 0      | 0     | 0     | 0     | 1     |
    | 2 =                | 0       | 0      | 0      | 0      | 0     | 0     | 1     | 0     |
    | 3 =                | 0       | 0      | 0      | 0      | 0     | 0     | 1     | 1     |
    | 8 =                | 0       | 0      | 0      | 0      | 1     | 0     | 0     | 0     |
    | 17 =               | 0       | 0      | 0      | 1      | 0     | 1     | 0     | 0     |
    | 172 =              | 1       | 0      | 1      | 0      | 1     | 1     | 0     | 0     |
    | 16 =               | 0       | 0      | 0      | 1      | 0     | 0     | 0     | 0     |
    | 254 =              | 1       | 1      | 1      | 1      | 1     | 1     | 1     | 0     |

  * Hexadecimal Number System (i.e base 16 [0-9 A-F]) 

    | Decimal | Binary | Hexadecimal |
    | :-----: | :----: | :---------: |
    |    0    |  0000  |      0      |
    |    1    |  0001  |      1      |
    |    2    |  0010  |      2      |
    |    3    |  0011  |      3      |
    |    4    |  0100  |      4      |
    |    5    |  0101  |      5      |
    |    6    |  0110  |      6      |
    |    7    |  0111  |      7      |
    |    8    |  1000  |      8      |
    |    9    |  1001  |      9      |
    |   10    |  1010  |      A      |
    |   11    |  1011  |      B      |
    |   12    |  1100  |      C      |
    |   13    |  1101  |      D      |
    |   14    |  1110  |      E      |
    |   15    |  1111  |      F      |

##### **Network Addressing**

* IPv4 
  * series of 1s and 0s (binary)
  * IPv4 address consist of 32 bits, divided into 4 sections. Each octet contains 8 bits (1 byte) separated by dot. 
  * eg. 10101100 00010000 11111110 00000001 > 172.16.254.1 IP address
  * 0.0.0.0 : accepting from anyone 
  * 255.255.255.255 : sending broadcast to everyone
  * IPv4 address is made up of :
    * A network portion 
    * A host portion
  * There are two systems to recognize the network portion form host portion: 
    * Legacy Classful addressing 
    * Classless (Subnet-Based System)
  * Private IP address ranges are as follows:
    - Class A Private IP Range: 10.0.0.0 – 10.255.255.255 
    - Class B Private IP Range: 172.16.0.0 – 172.31.255.255
    - Class C Private IP Range: 192.168.0.0 – 192.168.255.25
  
* Subnet Mask
  * Is a series of 1s followed by series of 0s. 
  
  * 1s represent network portion
  
  * 0s represent host portion 
  
  * IP and subnet mask are two separate things
  
  * Class A 
    * Network : 1.0.0.0 - 127.0.0.0 
    
    * Subnet mask: 255.0.0.0
    
    * Network portion is first octet
    
      ```text
      IP Address : 19.159.39.164/8 	Subnet : 255.0.0.0
      ------------------------------------------------------
      Binary IP Addr : 00010011.10011111.00100111.10100100
      Binary Subnet  : 11111111.00000000.00000000.00000000
      				 -----Network-----.-------Host------
      IP Network  : 19.0.0.0	
      First Host  : 19.0.0.1
      Last Host   : 19.255.255.254
      Brodcasat   : 19.255.255.255
      Next Subnet : 20.0.0.0
      
      
      IP Address : 58.21.182.173/13 	Subnet : 255.248.0.0
      ------------------------------------------------------
      Binary IP Addr : 00111010.00010|101.10110110.10101101
      Binary Subnet  : 11111111.11111|000.00000000.00000000
      				 -----Network-----.-------Host------
      IP Network  : 58.16.0.0
      First Host  : 58.16.0.1
      Last Host   : 58.23.255.254
      Brodcasat   : 58.23.255.255
      Next Subnet : 58.24.0.0
      Class A : Public
      ```
    
  * Class B 
    * Network : 128.0.0.0 - 191.255.0.0 
    
    * Subnet mask : 255.255.0.0
    
    * Network portion: 2 octet
    
      ```text
      IP Address : 19.159.39.164/16 	Subnet : 255.255.0.0
      ------------------------------------------------------
      Binary IP Addr : 00010011.10011111.00100111.10100100
      Binary Subnet  : 11111111.11111111.00000000.00000000
      				 -----Network-----.-------Host------
      IP Network  : 19.159.0.0	
      First Host  : 19.159.0.1
      Last Host   : 19.159.255.254
      Brodcasat   : 19.159.255.255
      Next Subnet : 19.160.0.0
      
      
      IP Address : 161.249.146.246/20 
      Subnet : 255.255.240.0
      ------------------------------------------------------
      Binary IP Addr : 10110001.11111001.1001|0010.11110110 
      Binary Subnet  : 11111111.11111111.1111|0000.00000000
      
      IP Network  : 161.249.144.0
      First Host  : 161.249.144.1
      Last Host   : 161.249.159.254
      Broadcast   : 161.249.159.255
      Next Subnet : 161.249.160.0
      Class B: Private
      ```
    
  * Class C 
    * Network : 192.168.0.0 - 223.255.255.0 
    
    * Subnet mask : 255.255.255.0
    
    * Network portion: 3 octet
    
    * ```text
      IP Address : 19.159.39.164/24 	Subnet : 255.255.255.0
      ------------------------------------------------------
      Binary IP Addr : 00010011.10011111.00100111.10100100
      Binary Subnet  : 11111111.11111111.11111111.00000000
      				 ----------Network---------.--Host--				
      IP Network  : 19.159.39.0	
      First Host  : 19.159.39.1
      Last Host   : 19.159.39.254
      Brodcasat   : 19.159.39.255
      Next Subnet : 19.159.40.0
      
      IP Address : 19.159.39.164/28 	Subnet : 255.255.255.240
      ------------------------------------------------------
      Binary IP Addr : 00010011.10011111.00100111.10100100
      Binary Subnet  : 11111111.11111111.11111111.11110000
      				 ----------Network-------------.--Host				
      IP Network  : 19.159.39.160	
      First Host  : 19.159.39.161
      Last Host   : 19.159.39.174
      Brodcasat   : 19.159.39.175
      Next Subnet : 19.159.39.176
      ```
  
* Classless Inter-Domain Routing (CIDR) 
  * CIDR can be considered as another method to write subnet masks 
  * CIDR value is the number of 1s in a subnet mask
  * CIRD value is how many bits represent the network portion in an IP
  * For example: 
    * IP: 192.168.1.1 Mask : 255.255.255.0 -> 192.168.1.1/24
    * IP: 172.16.1.1 Mask : 255.255.0.0 -> 172.16.1.1/16
  * Special IPv4 Addresses: 
    * 127.0.0.0 : 255.0.0.0 or /8 : direct traffic to itself
    * 169.254.x.y : 255.255.0.0 or /16 : Failed to get IP address from network, automatic assign. 
    * 172.16.0.0 - 172.31.0.0 : 255.240.0.0 or /12 : cannot be routed on the public network
    * 192.168.0.0 - 192.168.255.0 : 255.255.0.0 or / 16 : they can be used by anyone in any network

##### **Network Layer**

1. Introduction 
   * Router connects networks together, Its a computer.
   * Switch used to connect devices that belong to the same segment of the network. 
   
2. Getaway 
   * Its the router interface that is connected on a network reachable from the host 
   * Its the IP address of the NIC of the router
   * A host uses it in case it wants to send data to another host in a different network. 
   * It should be directly connected on the same network of its hosts
   * A host sends the traffic to the router when destination IP address in not on its own network. 
   
4. Directly Connected Networks 
   * If host not in local network, send traffic to default gateway and router will check in the routing table to see if the interface network is listed. This will mean that it exists on the network and forward the traffic.
   
4. Static Routing vs Dynamic Routing

   Static Routing does not use any routing protocols and algorithms, while dynamic routing uses routing protocols and complex algorithms to calculate routing operations. ... In static routing, routes not react with network changes, while in dynamic routing, routes react with network changes.

##### **Network Security**

1. Access Control List (ACL)
   * Contains rules that grant or deny access to resource (file, server, network, printer, system, etc)
   * ACL tells networking devices which type of traffic can access the network and which activity is allowed.
   * In networks, ACL is usually applied on a specific interface and specific direction. 
   * A networking device would apply and ACL on each packet as follows:
     * Get the destination and source addresses from packet
     * Find a rule in the ACL that matches the source and/or destination address/port
     * If match found, check if to allow packet to pass or deny. 
     * if no match, drop the packet immediately 
2. ACL - Wildcard
   * Wildcards are the opposite of subnet mask (replace 1 with 0, 0 with 1)
   * ACL will use the wildcard to check if the source/destination IP address matches a specific rule 
   * 255.255.255.0 -> 0.0.0.255
   * 255.255.128.0 -> 0.0.127.255
3. Firewall 
   * Firewall is a system that enforces an access control policy between networks. 
   * It monitors incoming and outgoing traffic
   * Firewall prevents the exposure of sensitive hosts, resources and applications to untrusted users. 
   * It sanitizes protocol flow, which prevents the exploitation of protocol flaws. 
   * It blocks malicious data from servers and clients
   * It reduces security management complexity by off-loading most of the network access control to a few firewall in the network 
   * A misconfigured firewall can have serious consequences for the network such as single point of failure
   * Network performance can slow down, as it has capacity of how many clients can be checked at a time. 
   * Unauthorized traffic can be tunneled or hidden so that it appears as legitimate traffic trough the firewall. 
4. Firewall IP table traffic: 
   * Input: traffic target is firewall 
   * Output : traffic generated by firewall its self
   * Forward : traffic passing by firewall and 
5. Firewall Policies
   * Allow List (White List) : Drop all packets except for the once on the list.
   * Deny List (Black List) : Allow all packets to pass except for the once on the list. 
6. Firewall types 
   * Packet filtering firewall : works on Layer 3 (Network) and 4 (Transport) 
   * Stateful firewall : works on Layer 3, 4, 5 and 7 
     * Stateful packet inspection, analyzing packet header, inspecting packet state.
7. Firewall delivery method
   1. Network based firewall 
   2. Host based firewall 
8. Firewall zones 
   1. Inside : Private network that should not be access by anyone unauthorized. 
   2. Outside : Public accessing your services. 
   3. Demilitarized : Servers separated from private network, prevents attacker from accessing all the network if one server has been breached. 

##### Network Address Translation (NAT)

Problem : 

* Not enough public IPv4 address to assign a unique address to each device connected to the internet. 
* Private address are used within an organization or site to allow devices to communicate locally 
* Private IPv4 cannot be route on internet

Solution : NAT

* Allow private IPv4 address to access an resource that is outside local network.
* NAT provides the translation of private address to public address.
* Private IPv4 address (Internal Network) < NAT Translation > Public IPv4 Address (Internet)
* NAT should be done on router or firewall. 

Types of NAT : 

* Static NAT : It uses a one to one mapping of local and global addresses. Isolating internal network from outside. 
* Dynamic NAT : It uses a pool of public address and assigns them on a first-come, first-served basic. 
* Port Address Translation (PAT) : also known as NAT overload, maps multiple private IPv4 address to a single public IPv4 address or few addresses.  This is used at home routers, one public IP address used by multiple devices. 

##### Proxy & Load Balancer

Forward Proxy 

* Server to pass the request from the clients on a private/isolated network to the internet (and the responses back to the clients)
* Caching 
* For example: Squid for HTTP/s
* Proxy is for protocol like HTTP, FTP, Socks, SSH etc. 

Reverse Proxy 

* A server to pass the HTTP/s requests from the clients on the internet to a server/multiple servers on a private/isolated network (and the responses back to the clients)
* For example: Nginx 
* Caching 
* Compression
* SSL/TLS Termination

Load Balancer

* A server that balances the received requests to a group of servers that do the same job (and the responses back to the client)
* A generic concept that can be used with any protocol 
* Can be used together with reverse proxy (for HTTP/s)
* For example: Nginx for HTTP/s
* Certificate used between client and proxy, as well as between proxy and server. 

<p align="right">(<a href="#top">back to top</a>)</p>

### 6. Cloud

##### What is Cloud Computing ? 

Cloud computing is the on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user. Large clouds often have functions distributed over multiple locations, each location being a data center.

* It covers all resources of computing; storage, network etc.
* Less responsibility of resources as its not on premises. 

##### **Benefits** 

* Flexibility : deployed and access anywhere, resources can be extended or reduced, when relocating business easier to move as no resources on site. 
* Efficiency : available in different locations. 
* Cost : no need to buy new hardware, if need more servers can be extended for some time when needed. 

##### Risks

* **Security** 

  Data lives on internet,  security still needs to be considered in order to keep data secure. 

* **Data Portability** 

  Being lock with provider, if you decided to change provider, your data might not be portable between services as they might be different 

* **Cloud Provider Transparency**  

  Can't be sure where your data is stored, it might be in different country than you live and it might have different law regarding data protection. For example in some countries government can access your data. 



##### Deployment Types

* **Private cloud** 

  Having your own private cloud also lets you control how data is shared and stored. This is often the best option if cloud security is a concern, since you can manage data governance, ensure compliance with any regulations, and protect valuable intellectual property.

* **Public cloud** 

  Since public cloud services are set up as pay-per-use, there’s minimal investment to get started. They’re also easy to scale, since you can simply buy more capacity as it’s needed. Public cloud services are especially useful for workloads that may run for a short period of time—for example, a start-up that can’t afford to wait months to prove its viability can get just the right amount of compute it needs, for just as long as it needs it. Plus, your IT team won’t need to maintain the hardware. The largest cloud service providers today include Amazon Web Services, Microsoft Azure, Alibaba Cloud, Google Cloud, and IBM

* **Hybrid**  

  A hybrid cloud combines public cloud and private cloud environments by allowing data and applications to be shared between them. This helps businesses seamlessly scale services back and forth between their own infrastructure and the public cloud. 



##### Cloud Services 

Shared responsibility model

* **On-premises**

  Your responsibly of everything 

* **IaaS (Infrastructure as a service)** 

  Provides only hardware, your responsibility to maintain and configure. Provider only maintenance physical hardware. 

* **PaaS (Platform as a service)**

  Provider takes care of network controls, access and authorization, OS, identity. The client is responsibility of deployment, usage, access policies and content. 

* **SaaS (Software as a service)**

  Provider takes care most of the responsibilities but client still needs to take responsibility for access policies and data governance rights management content. 

*There is no model that will provide no responsibility , client ALWAYS will have some responsibility.*



##### Virtualization vs Cloud Computing 

Virtualization is a technology that allows you to create multiple simulated environments or dedicated resources from a single, physical hardware system, and clouds are IT environments that abstract, pool, and share scalable resources across a network. To put it simply, virtualization is a technology, where cloud is an environment.

* Virtualization and Cloud computing are the two key buzz words 
* The concept of Virtualization forms a base for Cloud computing
* 

[Virtualization vs Cloud computing Reference](https://www.redhat.com/en/topics/cloud-computing/cloud-vs-virtualization)



##### Responsibility Model

1. Responsibilities that are always the provider's 

2. Responsibilities that are always the customer's 

3. Responsibilities that vary depending on the services

   

##### Cloud Security Challenges 

1. **Increased Attack Surface** 

   Adding more factors that can be attacked which are not under your control. For example, PaaS vulnerability of OS should be patched by provider but if they don't you will be vulnerable 

2. **Lack of Visibility and Tracking** 

   IaaS the provider they have full control of the infrastructure of hardware, you cant control what's happening at hardware level.

   SaaS has less viability of whats happping there, 

3. **Ever-Changing Workloads** 

   Keep changing resources all the time

4. **DevOps, DevSecOps and Automation** 

5. **Granular Privilege and Key Management**

   Cloud gives more privilege to user as its easier but gives more vulnerability 

6. **Complex Environments**

   Specially for hybrid type its hard to manage therefore it will give more security risks 

7. **Cloud Compliance and Governance**

   Need to make sure cloud provider compile with domain data laws. 

   

##### Zero trust security framework 

“never trust, always verify.”

1. Zero trust in cloud security is not to automatically trust anyone or anything within or outside of the network - verify
2. This approach helps secure access from users, end-user devices, APIs, IoT, microservices, containers, and more.

2. It protects an organization’s workforce, workloads, and the workplace. 
3. Assume zero trust any time someone or something requests access to assets.
4. It promotes a least privilege governance strategy
5. Users are only given access to the resources they need to perform their duties
6. Developers to ensure that web-facing applications are properly secured, check all inputs from the users.
7. Zero trust networks utilize micro-segmentation to make cloud network security far more granular

##### AAA Protocol 

1. Authentication : prove identity 
2. Authorization : determinate what user can do
3. Accounting : records what user does

<p align="right">(<a href="#top">back to top</a>)</p>

#### Amazon Web Services AWS

##### Best Practices

* Naming Convention

  `groupID_projectName_username_resourceName`

  For example: 

  `cyber10x_calculator_konrad_server`

* Always stop the instances (servers) when not in use

* Delete resources when no longer needed 

##### Regions & Zones

* Region has multiple zones, collection of availability zones 
* Availability zone is one or more discrete data centers with redundant power,networking and connectivity in an AWS region. 



##### Elastic Compute Cloud (EC2)

* EC2 provides scalable computing capacity in the AWS
* EC2 can be used to launch as many or as few virtual servers as needed, configure security and networking and mange storage. 
* EC2 enables you to scale up or down to handle changes in the requirements or spikes in popularity reducing your need to forecast traffic

##### EC2 Components 

1. **Amazon Machine Image (AMI)**

   Template that contains a software, its used to create instance

2. **Instance** 

   Virtual server in the cloud

3. **Key Pairs**

   * A key pair, consisting of a private key and a public key
   * is a set of security credential that you use to prove your identity when connecting to an instance 
   * Amazon keeps public key and private key is used to access instance. 

   

##### Simple Storage Service (S3)

Interface that you can use to store and retrieve any amount of data at any time and from anywhere

##### S3 Components

* **Bucket** 

  A bucket is a container for objects stored in S3. Every object is contained in a bucket

* **Object**

  Object are the fundamental entitles stored in S3. Object consist of object data and metadata. An object is uniquely identified within a bucket by a key (name) and version ID

* **Keys**

  A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key. 

<p align="right">(<a href="#top">back to top</a>)</p>
