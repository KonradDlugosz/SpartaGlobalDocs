<div id="top"></div>
<div align="center">
    <h1 align= "center">Cyber Security</h1>
</div>
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Introduction-to-Cyber-Security">Introduction to Cyber Security</a></li>
      <li><a href="#virtualization">Virtualization</a></li>
      <li><a href="#Containerization ">Containerization </a></li>
  </ol>
</details>


### Introduction to Cyber Security:

1. **What is cybersecurity ?** 

   Cyber security's core function is to protect the **devices** we all use (smartphones, laptops, tablets and computers), and the **services** we access - both online and at work - from theft or damage.

   It's also about preventing unauthorized access to the vast amounts of **personal information** we store on these devices, and online.

2. **Cybersecurity Cube (McCumber Cube)**

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

3. **Cybersecurity colors** 
   
   1. Blue Team (The Defenders) : responsible for defense of security, damage control and incident response. 
   2. Red Team (The Breakers/Attackers) : commissioned to perform "ethical hacking" on an organization.
   3. White Team (The Admins) : responsible for refereeing an engagement between a Red Team and mock attackers and Blu Team of actual defenders of their enterprise's use on information systems.  
   4. Yellow Team (The Builders) : responsible for developing the security system of an organization. 
   5. Many more .... Depends on context and organization. 
   
4. **Hackers**
   1. Black Hat Hackers - Attackers 
   2. White Hat Hackers - Ethical hackers, hacking with permission.
   3. Grey Hat Hackers - violate laws or typical ethical standards, but no malicious intent. 

5. **Testing**
   1. White box testing : All information on the system.
   2. Black box testing : No information on the system. 
   3. Grey box testing : Some information. eg network design. 
   
6. **Essential Terms**
   1. Asset: An asset is what we trying to protect.
   2. Vulnerability : A vulnerability is a weakness or gap in our protection efforts.
   3. Exploit : The way how hackers leverage vulnerabilities. 
   4. Threat : A threat is what we are trying to protect against.
   5. Risk : the intersection of assets, threats and vulnerabilities. 
   
7. **Causes of Vulnerabilities**
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

8. **Cyber Attacks**

   1. Un-targeted cyber attacks : phishing attacks which can be targeted for millions of people. 
   2. Targeted cyber attacks : Specific attack for a company or individual. 

9. **Threat Actors**

   ​	*CYBER THREAT ACTOR > MOTIVATION* 

   1. National-states > Geo political 
   2. Cybercriminals > Profits 
   3. Hacktivists > Ideological 
   4. Terrorist groups > ideological violence 
   5. Thrill-seekers > satisfaction/ attention 
   6. Insider threats > discontent

10. **Cyber Threats** 

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
    
11. **Cyber Threat Surface** 

    The attack surface of a software environment is the sum of the different points where an unauthorized user can try to enter data to or extract data from an environment. Keeping the attack surface as small as possible is a basic security measure.

12. **Cyber Kill Chain**

    1. Reconnaissance : finding all information about the target
    2. Weaponization : Write malware to leverage the vulnerability 
    3. Delivery : deliver malware via web, email, USB etc.
    4. Exploitation : exploiting vulnerability to execute code
    5. Installation : installing the malware on the asset
    6. Command and control (C2) : command channel for remote manipulation 
    7. Actions on objectives : with access, accomplish your goal

13. **Securing during development**

    Moving to the left in cybersecurity means that you should apply cybersecurity from beginning of product development. 

<p align="right">(<a href="#top">back to top</a>)</p>

### Virtualization

1. **Why use virtualization?** 

   * Variation between the development and production environment. 
   * Development environment is where application is developed. 
   * Production environment is where service is set it up. 
   * Each might have diffrenet OS, updates etc.
   * Solutions:
     *  Virtualization: Vagrant (used in development environment)
     * Containerization: Docker (used in production environment)

2. **What is virtualization ?**

   * Is the process of separating a software from the hardware. 
   * A virtual server means that server exists in virtual form physical.
   * Hypervisor (Virtual machine monitor VMM) works as interface between the VMs and the host. eg. VirtualBox , vmware 

3. **Hypervisor types**

   1. Type 1 Native/bare-metal : hardware > Hypervisors >> OS | APP 
   2. Type 2 Hosted : hardware > operating system > Hypervisors >> OS | APP

4. **Why use vagrant ?** 

   Configure virtual machine so that is exactly same across multiple devices so that all developers in a company have the same VM containing all apps and configuration. 

   * A tool for building a managing virtual machine environments in single workflow.
   * it lowers development setup time
   * can mirror production environments on the developer machine 
   * vagrant will create a virtual environment for each production environment. 
   * vagrant is not hypervisor, its an automation tool that can be combined with hypervisor
   * vagrant calls the hypervisor as a provider

<p align="right">(<a href="#top">back to top</a>)</p>

### Containerization 

1. **What is container ?** 
   * Containerization creates abstraction at an OS level that allows individual, modular and distinct functionality of the app to run independently 
   * Several isolated workloads - the containers - can co-exist on a machine
   * A unit of software that is lightweight but still bundles the code, its dependencies and the configuration altogether into a single image 
   * Where can run ? 
     * On bare metal servers 
     * On top hypervisors 
     * In cloud infrastructure
2. **Benefits** 
   * Useful in developing, deploying and testing modern distributed apps and microservices that can operate in isolated execution environments on same host machines.
   * Developers don't need to write application code into different VMs operating different app components to retrieve compute, storage and networking resources.  Containers are not heavy on resources as VM. 
   * A complete application component can be executed in its entirety within its isolated environment without affecting other app components or software. 
   * no conflicts with libraries during execution. 
3. **Security** 
   * Less secure than VM as they share kernel with host OS.
   * Container share the same kernel with other containers 
4. **Docker**
   * An open platform for developing, shipping and running applications.
   * Enables separation of an applications from the infrastructure. 