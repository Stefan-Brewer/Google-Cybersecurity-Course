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

1. **Hub**: Broadcasts information to every device (less secure, less efficient)
2. **Switch**: Makes connections between specific devices, maintains MAC address tables
3. **Router**: Connects networks together, directs traffic based on IP addresses
4. **Modem**: Connects router to the internet, translates between digital and analog signals
5. **Firewall**: Monitors traffic, restricts specific incoming/outgoing traffic
6. **Wireless Access Point**: Creates wireless networks using Wi-Fi

### Client-Server Model
- **Servers**: Provide information and services
- **Clients**: Devices that connect to servers and request information/services
- Common server types: DNS, file, mail servers

### Cloud Computing

- **Cloud Network**: Remote servers hosted on internet instead of local physical devices
- **Service Models**:
  - **SaaS (Software as a Service)**: Remote software suites
  - **IaaS (Infrastructure as a Service)**: Virtual computer components
  - **PaaS (Platform as a Service)**: Tools for designing custom applications

- **Advanced Cloud Concepts**:
  - **Software-Defined Networks (SDN)**: Virtual network devices and services
  - **Hybrid Cloud**: Organizations using both CSP services and on-premise resources
  - **Multi-Cloud**: Using more than one Cloud Service Provider

- **Benefits**:
  - Reliability: Consistent access with minimal interruption
  - Cost Reduction: Lower upfront costs, pay-as-you-go model
  - Scalability: Easy to scale resources as needed

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

1. **Physical Layer** (cables, hardware)
2. **Data Link Layer** (switches, network interface cards)
3. **Network Layer** (routing between networks)
4. **Transport Layer** (data delivery, TCP/UDP)
5. **Session Layer** (connection establishment, authentication)
6. **Presentation Layer** (data translation, encryption)
7. **Application Layer** (user-facing applications)

TCP/IP combines multiple OSI layers:
- TCP/IP Network Access = OSI Physical + Data Link
- TCP/IP Internet = OSI Network
- TCP/IP Transport = OSI Transport
- TCP/IP Application = OSI Application + Presentation + Session

## Addressing and Packets

### IP Addressing
- **IP Address**: Unique string identifying device location
- Two versions:
  
  #### IPv4
  - Format: Four 1-3 digit numbers separated by periods (e.g., 198.51.100.0)
  - 4 bytes total (32 bits), up to 4.3 billion possible addresses
  - Header size: 20-60 bytes
  
  #### IPv6
  - Format: Eight hexadecimal numbers separated by colons
  - 16 bytes total (128 bits), 340 undecillion addresses
  - Developed to address IPv4 exhaustion
  - Simpler header format, more efficient routing

- **Public vs Private IP Addresses**:
  - **Public**: Assigned by ISP, connected to geographic location
  - **Private**: Only visible to devices on same local network

### MAC Addresses
- Unique alphanumeric identifier assigned to each physical device
- Used by switches to direct data packets

### IPv4 Packet Structure
- **Header** (20-60 bytes): Contains version, length, type of service, TTL, protocol, etc.
- **Data Section**: Contains the actual message

## Network Protocols

### Protocol Categories

1. **Communication Protocols** - Govern data exchange
   - **TCP (Transmission Control Protocol)** - Reliable connections with handshaking
   - **UDP (User Datagram Protocol)** - Connectionless, prioritizes speed
   - **HTTP (Hypertext Transfer Protocol)** - Web page transfer, port 80
   - **DNS (Domain Name System)** - Translates domain names to IP addresses, port 53

2. **Management Protocols** - Monitor and manage networks
   - **SNMP (Simple Network Management Protocol)** - Device monitoring and management
   - **ICMP (Internet Control Message Protocol)** - Reports errors, used by "ping"
   - **DHCP (Dynamic Host Configuration Protocol)** - Assigns IP addresses, ports 67/68
   - **ARP (Address Resolution Protocol)** - Maps IP addresses to MAC addresses

3. **Security Protocols** - Ensure secure data transmission
   - **HTTPS (HTTP Secure)** - Secures HTTP using SSL/TLS, port 443
   - **SFTP (Secure File Transfer Protocol)** - Secures file transfers using SSH
   - **SSH (Secure Shell)** - Secure remote connections, port 22

### Email Protocols
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
- **Types**:
  - **Hardware firewalls**: Physical devices inspecting packets
  - **Software firewalls**: Programs installed on devices
  - **Cloud-based firewalls (FaaS)**: Hosted by cloud providers

- **Operation Modes**:
  - **Stateless**: Uses predefined rules, doesn't track packet information
  - **Stateful**: Tracks information, proactively filters threats
  - **Next Generation Firewall (NGFW)**: Advanced security with deep packet inspection

### Virtual Private Networks (VPNs)
- **Purpose**: Preserves privacy on public networks
- **Functions**:
  - Changes public IP address, hides virtual location
  - Encrypts data in transit
  - Uses encapsulation for data protection
  - Creates encrypted tunnels between devices and servers

- **Types**:
  - **Remote access VPNs**: Connect individual users to networks
  - **Site-to-site VPNs**: Connect entire networks together

- **Protocols**:
  - **WireGuard**: Newer, faster, open-source
  - **IPSec**: Well-established, widely adopted

### Security Zones
- **Definition**: Network segments protecting internal networks through segmentation
- **Zone Types**:
  1. **Uncontrolled zone**: Networks outside organizational control (internet)
  2. **Controlled zone**: Subnet protecting internal network
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
- **Types**:
  - **Forward proxy**: Regulates user internet access, hides IP
  - **Reverse proxy**: Regulates internet access to internal servers
  - **Email proxy**: Filters spam by verifying sender addresses

### Wireless Security Protocols (from least to most secure)
- **WEP (Wired Equivalent Privacy)**: First standard (1999), now high-risk
- **WPA (Wi-Fi Protected Access)**: Replaced WEP (2003), uses TKIP
- **WPA2**: Standard since 2004, uses AES and CCMP
- **WPA3**: Latest protocol with Simultaneous Authentication of Equals (SAE)

- **WPA2/WPA3 Modes**:
  - **Personal**: Best for home networks, uses global passphrase
  - **Enterprise**: For businesses, provides individualized control

## Security Best Practices
- Implement defense in depth with multiple security layers
- Use stateful firewalls over stateless when possible
- Maintain proper network segmentation
- Keep all security devices and software updated
- Apply the principle of least privilege for network access
- Monitor traffic for suspicious activity
- Implement both physical and virtual security measures


# Network Security & Intrusion Tactics

## 1. Introduction to Network Intrusion Tactics

### Why Secure Networks?
- Networks face constant attack risks from malicious hackers
- Attacks can leak confidential information, damage reputation, impact customer retention, and cost money/time to mitigate
- Case example: Home Depot (2014) - servers infected with malware compromised credit/debit information of 56 million customers

### Types of Network Intrusion Attacks

#### Network Interception Attacks
- Intercept network traffic to steal information or manipulate transmissions
- **Packet sniffing**: Capturing/inspecting data packets in transit
  - **Passive sniffing**: Reading data packets without altering them
  - **Active sniffing**: Manipulating data packets in transit
- **On-path attacks** (meddler-in-the-middle): Intercepting communications between trusted devices
  - Can collect credentials or spoof DNS responses to redirect users
  - Protection: Encrypt data in transit (e.g., TLS)

#### Backdoor Attacks
- Weaknesses intentionally left by programmers/administrators that bypass normal access controls
- Originally for troubleshooting but can be exploited for malicious purposes
- Allows attackers to install malware, perform DoS attacks, steal information, or change security settings

### Impact of Network Attacks
- **Financial**: Service interruption, repair costs, ransomware payments, litigation from affected customers
- **Reputation**: Public trust erosion, customer migration to competitors
- **Public safety**: Critical infrastructure compromise (power grids, water systems, defense communications)

## 2. Denial of Service (DoS) Attacks

### Basic Concepts
- **DoS attack**: Floods network/server with traffic to disrupt operations
- **DDoS attack**: Uses multiple devices/servers in different locations to amplify the attack

### Common Network-Level DoS Attacks

#### SYN Flood Attack
- Exploits TCP connection handshake process
- Attacker floods server with SYN packets but never completes handshake
- Consumes all available ports, preventing legitimate connections

#### ICMP-Based Attacks
- **ICMP (Internet Control Message Protocol)**: Used for network status/error reporting
- **ICMP flood**: Repeatedly sends ICMP packets to force responses until bandwidth is consumed
- **Ping of death**: Sends oversized ICMP packets (>64KB) to crash vulnerable systems

#### Smurf Attack
- Combines IP spoofing with DoS techniques
- Attacker spoofs victim's IP address and sends ICMP requests to network broadcast address
- All devices respond to the victim's IP, overwhelming it with traffic

### Real-World DDoS Example (2016 DNS Attack)
- University students created a botnet targeting gaming servers
- Code was posted online, allowing others to gain control
- Attackers sent tens of millions of DNS requests to major DNS service provider
- Resulted in widespread outages across North America and Europe for websites using the service
- Service was restored after two hours

## 3. Network Attack Tactics and Mitigations

### IP Spoofing
- Changing source IP of data packets to impersonate authorized systems
- Used to bypass authentication or hide attacker's identity
- Mitigation: Configure firewalls to refuse unauthorized IP packets and suspicious traffic

### Packet Sniffing Mechanics
- Network Interface Cards (NICs) can be set to "promiscuous mode" to accept all traffic
- Attackers use software like Wireshark to capture and analyze network data
- Can obtain IP/MAC addresses, credentials, or personal information

### Replay Attacks
- Intercepting valid data transmissions and repeating them later
- Example: Capturing authentication packets and resending them to gain access

### Protection Against Network Attacks

#### Against Packet Sniffing
- Use VPNs to encrypt data in transit
- Ensure websites use HTTPS (SSL/TLS encryption)
- Avoid unprotected public WiFi networks

#### Against DoS/DDoS
- Implement advanced firewalls that detect network anomalies
- Use traffic filtering to block suspicious patterns
- Distribute resources across dynamically scalable hosts

#### General Security Measures
- Apply encryption for data in transit
- Regularly update and patch systems
- Monitor network for unusual traffic patterns
- Implement defense-in-depth strategy (multiple layers of security)

## 4. Security Analyst Role

### Defensive Techniques
- Use network protocol analyzers (tcpdump, Wireshark) to monitor traffic patterns
- Analyze packet content for security investigations
- Establish network traffic baselines to identify anomalies
- Review logs for signs of intrusion attempts

### tcpdump Analysis
- Command-line network protocol analyzer
- Captures and displays packet information:
  - Timestamp
  - Source IP and port
  - Destination IP and port
- Used for troubleshooting and security monitoring

### Professional Perspective
- Incident response requires:
  - The "3Cs": Command, Control, and Communications
  - Calm under pressure
  - Coordination with team members
  - Clear communication about findings and actions
