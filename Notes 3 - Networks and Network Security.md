# Network and Network Security Fundamentals

## Network Basics

- **Network**: A group of connected devices that can communicate with each other
- **Network Architecture**: The basic structure and design of a network
- **Network Security**: Protection of network infrastructure and data from threats
- **Device Identification**: Devices use unique identifiers (IP and MAC addresses)

### Network Types
- **LAN (Local Area Network)**: Spans a small area (office, home)
- **WAN (Wide Area Network)**: Spans a large geographical area
  - The internet is essentially one large WAN

### Network Devices
- **Hub**: Broadcasts information to every device (less secure, less efficient)
- **Switch**: Makes connections between specific devices, maintains MAC address tables
- **Router**: Connects networks together, directs traffic based on IP addresses
- **Modem**: Connects router to the internet, translates between digital and analog signals
- **Firewall**: Monitors traffic, restricts specific incoming/outgoing traffic
- **Wireless Access Point**: Creates wireless networks using Wi-Fi

### Client-Server Model
- **Servers**: Provide information and services
- **Clients**: Devices that connect to servers and request information/services
- **Common server types**: DNS, file, mail servers

## Cloud Computing

- **Cloud Network**: Remote servers hosted on internet instead of local physical devices

### Service Models
- **SaaS (Software as a Service)**: Remote software suites
- **IaaS (Infrastructure as a Service)**: Virtual computer components
- **PaaS (Platform as a Service)**: Tools for designing custom applications

### Advanced Cloud Concepts
- **Software-Defined Networks (SDN)**: Virtual network devices and services
- **Hybrid Cloud**: Organizations using both CSP services and on-premise resources
- **Multi-Cloud**: Using more than one Cloud Service Provider

### Benefits
- **Reliability**: Consistent access with minimal interruption
- **Cost Reduction**: Lower upfront costs, pay-as-you-go model
- **Scalability**: Easy to scale resources as needed

## Network Communication

### Data Transmission
- **Data Packets**: Basic units of information containing:
  - Destination address, source address, protocol number, message body, footer
- **Performance Metrics**:
  - **Bandwidth**: Amount of data received per second
  - **Speed**: Rate at which data packets are received/downloaded
  - Irregular bandwidth/speed can indicate a network attack

### TCP/IP Model
Four-layer model for network communication:

#### 1. Network Access Layer (lowest)
- Deals with creation and transmission of data packets
- Includes physical hardware (hubs, modems, cables)
- Contains Address Resolution Protocol (ARP)
  - Maps IP addresses to MAC addresses

#### 2. Internet Layer
- Ensures delivery to destination hosts
- Attaches IP addresses to data packets
- Key protocols:
  - **Internet Protocol (IP)**: Routes packets to destinations
  - **Internet Control Message Protocol (ICMP)**: Shares error information and status updates

#### 3. Transport Layer
- Controls traffic flow across networks
- Key protocols:
  - **Transmission Control Protocol (TCP)**:
    - Establishes connections, ensures reliable transmission
    - Connection-oriented using three-way handshake (SYN → SYN/ACK → ACK)
  - **User Datagram Protocol (UDP)**:
    - Connectionless protocol prioritizing speed over reliability
    - Used for performance-sensitive applications

#### 4. Application Layer (highest)
- Handles interaction with receiving devices
- Common protocols:
  - HTTP/HTTPS (web browsing)
  - SMTP (email)
  - SSH (secure remote access)
  - FTP (file transfers)
  - DNS (domain name resolution)

### OSI Model Comparison
The OSI model has 7 layers compared to TCP/IP's 4 layers:

1. Physical Layer (cables, hardware)
2. Data Link Layer (switches, network interface cards)
3. Network Layer (routing between networks)
4. Transport Layer (data delivery, TCP/UDP)
5. Session Layer (connection establishment, authentication)
6. Presentation Layer (data translation, encryption)
7. Application Layer (user-facing applications)

TCP/IP combines multiple OSI layers:
- TCP/IP Network Access = OSI Physical + Data Link
- TCP/IP Internet = OSI Network
- TCP/IP Transport = OSI Transport
- TCP/IP Application = OSI Application + Presentation + Session

## Addressing and Packets

### IP Addressing
- **IP Address**: Unique string identifying device location

#### Two versions:
1. **IPv4**
   - Format: Four 1-3 digit numbers separated by periods (e.g., 198.51.100.0)
   - 4 bytes total (32 bits), up to 4.3 billion possible addresses
   - Header size: 20-60 bytes

2. **IPv6**
   - Format: Eight hexadecimal numbers separated by colons
   - 16 bytes total (128 bits), 340 undecillion addresses
   - Developed to address IPv4 exhaustion
   - Simpler header format, more efficient routing

#### Public vs Private IP Addresses:
- **Public**: Assigned by ISP, connected to geographic location
- **Private**: Only visible to devices on same local network

### MAC Addresses
- Unique alphanumeric identifier assigned to each physical device
- Used by switches to direct data packets

### IPv4 Packet Structure
- **Header (20-60 bytes)**: Contains version, length, type of service, TTL, protocol, etc.
- **Data Section**: Contains the actual message

## Network Protocols

### Protocol Categories

#### Communication Protocols - Govern data exchange
- **TCP (Transmission Control Protocol)** - Reliable connections with handshaking
- **UDP (User Datagram Protocol)** - Connectionless, prioritizes speed
- **HTTP (Hypertext Transfer Protocol)** - Web page transfer, port 80
- **DNS (Domain Name System)** - Translates domain names to IP addresses, port 53

#### Management Protocols - Monitor and manage networks
- **SNMP (Simple Network Management Protocol)** - Device monitoring and management
- **ICMP (Internet Control Message Protocol)** - Reports errors, used by "ping"
- **DHCP (Dynamic Host Configuration Protocol)** - Assigns IP addresses, ports 67/68
- **ARP (Address Resolution Protocol)** - Maps IP addresses to MAC addresses

#### Security Protocols - Ensure secure data transmission
- **HTTPS (HTTP Secure)** - Secures HTTP using SSL/TLS, port 443
- **SFTP (Secure File Transfer Protocol)** - Secures file transfers using SSH
- **SSH (Secure Shell)** - Secure remote connections, port 22

#### Email Protocols
- **POP3 (Post Office Protocol)** - Retrieves email, ports 110/995
- **IMAP (Internet Message Access Protocol)** - Downloads email headers, ports 143/993
- **SMTP (Simple Mail Transfer Protocol)** - Transmits email, ports 25/587

### Ports
- Software-based locations that organize data transmission by service type
- Common port numbers:
  - 25: Email (SMTP)
  - 80: HTTP
  - 443: HTTPS
  - 22: SSH
  - 20/21: FTP

## Network Security

### Firewalls
- **Definition**: Device that monitors traffic, allowing or blocking based on security rules

#### Types:
- **Hardware firewalls**: Physical devices inspecting packets
- **Software firewalls**: Programs installed on devices
- **Cloud-based firewalls (FaaS)**: Hosted by cloud providers

#### Operation Modes:
- **Stateless**: Uses predefined rules, doesn't track packet information
- **Stateful**: Tracks information, proactively filters threats
- **Next Generation Firewall (NGFW)**: Advanced security with deep packet inspection

### Virtual Private Networks (VPNs)
- **Purpose**: Preserves privacy on public networks

#### Functions:
- Changes public IP address, hides virtual location
- Encrypts data in transit
- Uses encapsulation for data protection
- Creates encrypted tunnels between devices and servers

#### Types:
- **Remote access VPNs**: Connect individual users to networks
- **Site-to-site VPNs**: Connect entire networks together

#### Protocols:
- **WireGuard**: Newer, faster, open-source
- **IPSec**: Well-established, widely adopted

### Security Zones
- **Definition**: Network segments protecting internal networks through segmentation

#### Zone Types:
- **Uncontrolled zone**: Networks outside organizational control (internet)
- **Controlled zone**: Subnet protecting internal network
- **Demilitarized Zone (DMZ)**: Contains public-facing services
- **Internal network**: Contains private servers and sensitive data
- **Restricted zone**: Protects highly confidential information

### Subnetting and CIDR
- **Subnetting**: Subdividing a network into logical groups
- **CIDR (Classless Inter-Domain Routing)**:
  - Method for assigning subnet masks to IP addresses
  - Format: IP address followed by "/" and a prefix (e.g., 198.51.100.0/24)

### Proxy Servers
- **Definition**: Servers that fulfill client requests by forwarding them to other servers

#### Types:
- **Forward proxy**: Regulates user internet access, hides IP
- **Reverse proxy**: Regulates internet access to internal servers
- **Email proxy**: Filters spam by verifying sender addresses

### Wireless Security Protocols (from least to most secure)
- **WEP (Wired Equivalent Privacy)**: First standard (1999), now high-risk
- **WPA (Wi-Fi Protected Access)**: Replaced WEP (2003), uses TKIP
- **WPA2**: Standard since 2004, uses AES and CCMP
- **WPA3**: Latest protocol with Simultaneous Authentication of Equals (SAE)

#### WPA2/WPA3 Modes:
- **Personal**: Best for home networks, uses global passphrase
- **Enterprise**: For businesses, provides individualized control

### Security Best Practices
- Implement defense in depth with multiple security layers
- Use stateful firewalls over stateless when possible
- Maintain proper network segmentation
- Keep all security devices and software updated
- Apply the principle of least privilege for network access
- Monitor traffic for suspicious activity
- Implement both physical and virtual security measures

## Network Security & Intrusion Tactics

### Introduction to Network Intrusion Tactics

#### Why Secure Networks?
- Networks face constant attack risks from malicious hackers
- Attacks can leak confidential information, damage reputation, impact customer retention, and cost money/time to mitigate
- Case example: Home Depot (2014) - servers infected with malware compromised credit/debit information of 56 million customers

#### Types of Network Intrusion Attacks

##### Network Interception Attacks
- Intercept network traffic to steal information or manipulate transmissions
- **Packet sniffing**: Capturing/inspecting data packets in transit
  - **Passive sniffing**: Reading data packets without altering them
  - **Active sniffing**: Manipulating data packets in transit
- **On-path attacks (meddler-in-the-middle)**: Intercepting communications between trusted devices
  - Can collect credentials or spoof DNS responses to redirect users
  - Protection: Encrypt data in transit (e.g., TLS)

##### Backdoor Attacks
- Weaknesses intentionally left by programmers/administrators that bypass normal access controls
- Originally for troubleshooting but can be exploited for malicious purposes
- Allows attackers to install malware, perform DoS attacks, steal information, or change security settings

#### Impact of Network Attacks
- **Financial**: Service interruption, repair costs, ransomware payments, litigation from affected customers
- **Reputation**: Public trust erosion, customer migration to competitors
- **Public safety**: Critical infrastructure compromise (power grids, water systems, defense communications)

### Denial of Service (DoS) Attacks

#### Basic Concepts
- **DoS attack**: Floods network/server with traffic to disrupt operations
- **DDoS attack**: Uses multiple devices/servers in different locations to amplify the attack

#### Common Network-Level DoS Attacks

##### SYN Flood Attack
- Exploits TCP connection handshake process
- Attacker floods server with SYN packets but never completes handshake
- Consumes all available ports, preventing legitimate connections

##### ICMP-Based Attacks
- ICMP (Internet Control Message Protocol): Used for network status/error reporting
- **ICMP flood**: Repeatedly sends ICMP packets to force responses until bandwidth is consumed
- **Ping of death**: Sends oversized ICMP packets (>64KB) to crash vulnerable systems

##### Smurf Attack
- Combines IP spoofing with DoS techniques
- Attacker spoofs victim's IP address and sends ICMP requests to network broadcast address
- All devices respond to the victim's IP, overwhelming it with traffic

#### Real-World DDoS Example (2016 DNS Attack)
- University students created a botnet targeting gaming servers
- Code was posted online, allowing others to gain control
- Attackers sent tens of millions of DNS requests to major DNS service provider
- Resulted in widespread outages across North America and Europe for websites using the service
- Service was restored after two hours

### Network Attack Tactics and Mitigations

#### IP Spoofing
- Changing source IP of data packets to impersonate authorized systems
- Used to bypass authentication or hide attacker's identity
- Mitigation: Configure firewalls to refuse unauthorized IP packets and suspicious traffic

#### Packet Sniffing Mechanics
- Network Interface Cards (NICs) can be set to "promiscuous mode" to accept all traffic
- Attackers use software like Wireshark to capture and analyze network data
- Can obtain IP/MAC addresses, credentials, or personal information

#### Replay Attacks
- Intercepting valid data transmissions and repeating them later
- Example: Capturing authentication packets and resending them to gain access

#### Protection Against Network Attacks

##### Against Packet Sniffing
- Use VPNs to encrypt data in transit
- Ensure websites use HTTPS (SSL/TLS encryption)
- Avoid unprotected public WiFi networks

##### Against DoS/DDoS
- Implement advanced firewalls that detect network anomalies
- Use traffic filtering to block suspicious patterns
- Distribute resources across dynamically scalable hosts

##### General Security Measures
- Apply encryption for data in transit
- Regularly update and patch systems
- Monitor network for unusual traffic patterns
- Implement defense-in-depth strategy (multiple layers of security)

### Security Analyst Role

#### Defensive Techniques
- Use network protocol analyzers (tcpdump, Wireshark) to monitor traffic patterns
- Analyze packet content for security investigations
- Establish network traffic baselines to identify anomalies
- Review logs for signs of intrusion attempts

#### tcpdump Analysis
- Command-line network protocol analyzer
- Captures and displays packet information:
  - Timestamp
  - Source IP and port
  - Destination IP and port
- Used for troubleshooting and security monitoring

#### Professional Perspective
- Incident response requires:
  - The "3Cs": Command, Control, and Communications
  - Calm under pressure
  - Coordination with team members
  - Clear communication about findings and actions

## Security Hardening: Networks and Network Security

### Security Hardening Fundamentals
Security hardening is the process of strengthening a system to reduce its vulnerability and attack surface. The attack surface comprises all potential vulnerabilities that could be exploited.

Key aspects:
- Can be implemented on devices, networks, applications, and cloud infrastructure
- Includes regular maintenance procedures to keep systems functioning securely
- Physical security is also a component (security cameras, guards, etc.)

### OS Hardening Practices
Operating systems serve as intermediaries between hardware and users/software applications. Security is critical as one compromised OS can lead to network-wide vulnerabilities.

#### Regular Interval Tasks:
- **Patch Updates**: Software/OS updates addressing security vulnerabilities
  - Critical to install promptly after release to prevent exploitation
- **Baseline Configuration**: Documented specifications used as reference for builds and updates
  - Allows comparison of current configuration against the baseline
- **Hardware/Software Disposal**: Properly wiping hardware and removing unused software applications

#### Security Measures:
- **Strong Password Policies**: Rules requiring specific character types, length, etc.
- **Multi-Factor Authentication (MFA)**: Verification using multiple methods (something you know, have, or are)

### Brute Force Attacks
Types of brute force attacks:
- **Simple Brute Force**: Manually trying combinations of credentials
- **Dictionary Attacks**: Using lists of commonly used passwords or leaked credentials

#### Prevention Measures:
- **Salting and Hashing**: One-way conversion of information with added random characters
- **MFA/2FA**: Requiring multiple forms of verification
- **CAPTCHA/reCAPTCHA**: Tests distinguishing humans from automated programs
- **Password Policies**: Guidelines for password complexity, updates, and reuse

#### Testing Environments:
- **Virtual Machines (VMs)**: Software versions of physical computers providing isolation
- **Sandbox Environments**: Testing environments separate from the main network

### Network Hardening Practices

#### Regular Tasks:
- **Firewall Rules Maintenance**: Keeping rules updated and relevant
- **Network Log Analysis**: Examining logs to identify events of interest using log analyzers or SIEM tools
- **Patch Updates**: Network device firmware and software updates
- **Server Backups**: Regular data backup procedures

#### One-Time Tasks (with updates as needed):
- **Port Filtering**: Blocking/allowing specific ports to limit communication
- **Network Access Privileges**: Restricting access based on user roles
- **Network Segmentation**: Creating isolated subnets for different departments
- **Encryption**: Implementing current encryption standards for all communications

### Network Security Applications: Defense in Depth
Defense in depth refers to adding multiple layers of security to a network:

#### Security Layers:
- **Firewalls**: Allow/block traffic based on rules examining packet headers
- **Intrusion Detection System (IDS)**: Monitors system activity and alerts on possible intrusions
  - Located behind firewall to reduce false positives
  - Limitation: Only detects known attacks/anomalies and doesn't stop traffic
- **Intrusion Prevention System (IPS)**: Monitors and actively stops intrusive activity
  - Sits behind firewall, blocks suspicious traffic before reaching sensitive areas
  - Limitation: If it breaks, network connection may be disrupted
- **Full Packet Capture Devices**: Record and analyze all network data
- **Security Information and Event Management (SIEM)**: Collects and analyzes log data
  - Creates centralized dashboard ("single pane of glass")
  - Helps prioritize security events but only reports issues without taking action

### Cloud Security
Cloud networks are collections of servers storing resources and data in remote data centers, accessed via the internet.

#### Key Considerations:
- **Identity Access Management (IAM)**: Manages digital identities and access to cloud resources
- **Configuration**: Precise setup of each cloud service to maintain security
- **Attack Surface**: More services can mean more entry points without proper design
- **Zero-Day Attacks**: CSPs typically detect these faster than traditional IT organizations
- **Visibility and Tracking**: Organizations have less direct visibility into CSP infrastructure
- **Rapid Changes**: Cloud services frequently update, requiring organizational adaptations

#### Hardening Techniques:
- **Hypervisors**: Abstract hardware from the operating environment (Type 1 run on hardware, Type 2 on software)
- **Baselining**: Establishing reference points for cloud environment configuration
- **Cryptography**: Encrypting data processed and stored in cloud environments
- **Cryptographic Erasure**: Destroying encryption keys to make data unreadable

#### Key Management:
- **Trusted Platform Module (TPM)**: Computer chip for secure credential storage
- **Cloud Hardware Security Module (CloudHSM)**: Device for cryptographic key storage and operations

#### Shared Responsibility Model:
- **CSP Responsibility**: Cloud infrastructure, physical data centers, hypervisors, host operating systems
- **Organization Responsibility**: Assets and processes stored or operated in the cloud, proper configuration
