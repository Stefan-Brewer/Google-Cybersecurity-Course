# Course 6: Sound the Alarm: Detection and Response

## Module 1: Introduction to Detection and Incident Response

## 1. Incident Response Fundamentals

### Incident Response Lifecycle
- Based on the NIST Cybersecurity Framework (CSF) with focus on:
  - **Detect**: Monitor systems to identify security events
  - **Respond**: Take action when incidents occur
  - **Recover**: Restore affected systems to normal operation

### NIST Incident Response Lifecycle
1. **Preparation**: Planning and readiness before incidents occur
2. **Detection and Analysis**: Identifying and investigating potential incidents
3. **Containment, Eradication, and Recovery**: Limiting damage, removing threats, restoring systems
4. **Post-incident Activity**: Documentation, lessons learned, and process improvement

### Events vs. Incidents
- **Event**: Any observable occurrence on a network, system, or device
- **Incident**: An event that jeopardizes confidentiality, integrity, or availability of information systems; or violates security policies
- Key distinction: All security incidents are events, but not all events are security incidents

### The Five W's of Incident Investigation
- **Who** triggered the incident
- **What** happened
- **When** the incident took place
- **Where** the incident took place
- **Why** the incident occurred

## 2. Incident Response Teams and Organization

### Computer Security Incident Response Teams (CSIRT)
- Specialized group trained in incident management and response
- Goals: Effectively manage incidents, provide response resources, prevent future incidents
- Works cross-functionally with other departments (legal, PR, etc.)

### Key Security Roles
- **Security Analyst**: Investigates alerts, determines incident criticality, performs initial triage
- **Technical Lead**: Provides technical guidance throughout the incident lifecycle
- **Incident Coordinator**: Tracks and manages CSIRT activities, ensures processes are followed

### Security Operations Center (SOC)
- Dedicated to monitoring networks, systems, and devices for security threats
- Organizational structure:
  - **Tier 1 SOC Analyst (L1)**: Alert monitoring, prioritization, and initial response
  - **Tier 2 SOC Analyst (L2)**: Deeper investigations, security tool configuration
  - **Tier 3 SOC Lead (L3)**: Advanced detection techniques, forensics, malware analysis
  - **SOC Manager**: Team leadership, performance metrics, stakeholder communication

### Command, Control, and Communication
- **Command**: Leadership and direction overseeing the response
- **Control**: Technical management of resources and tasks
- **Communication**: Keeping stakeholders informed

## 3. Incident Response Documentation and Planning

### Incident Response Plan
- Formal document outlining procedures for incident response
- Tailored to organization's unique requirements (mission, size, industry)
- Common elements:
  - Incident response procedures (step-by-step instructions)
  - System information (network diagrams, asset inventory, logging)
  - Supporting documents (contact lists, forms, templates)

### Documentation Types and Tools
- **Incident Handler's Journal**: Records incident details and investigation notes
- **Playbooks**: Step-by-step manuals for operational actions
- **Final Reports**: Complete incident summaries
- **Tools**: Word processors, ticketing systems, spreadsheets, audio/visual recording

### Effective Documentation Principles
- Reduces uncertainty and confusion during high-pressure incidents
- Should be clear, consistent, and accurate
- Enables swift and decisive response

## 4. Detection Tools and Technologies

### Intrusion Detection System (IDS)
- Monitors system activity and alerts on possible intrusions
- Detects suspicious activity but does not prevent/stop it
- Examples: Zeek, Suricata, Snort, Sagan

### Intrusion Prevention System (IPS)
- Monitors system activity AND takes action to stop intrusive activity
- Has all IDS capabilities plus active prevention
- Many tools (Suricata, Snort, Sagan) can function as both IDS and IPS

### Endpoint Detection and Response (EDR)
- Monitors endpoints (computers, phones, tablets) for malicious activity
- Performs behavioral analysis using ML/AI to identify threat patterns
- Can automatically stop attacks without manual intervention
- Examples: Open EDR, Bitdefender EDR, FortiEDR

### Detection Categories
- **True Positive**: Correctly detects an actual attack
- **True Negative**: Correctly identifies no malicious activity
- **False Positive**: Incorrectly identifies legitimate activity as malicious
- **False Negative**: Fails to detect actual malicious activity

## 5. Alert and Event Management Systems

### Security Information and Event Management (SIEM)
- Collects and analyzes log data to monitor critical activities
- Provides high-level overview of network security status
- Process:
  1. **Collect and Aggregate Data**: Gathers logs from multiple sources
  2. **Normalize Data**: Standardizes formats for consistent analysis
  3. **Analyze Data**: Applies detection rules to identify threats
- Examples: AlienVault OSSIM, Chronicle, Elastic, Splunk, IBM QRadar

### Security Orchestration, Automation, and Response (SOAR)
- Uses automation to respond to security events
- Automates analysis and response processes
- Provides case management capabilities
- Can track and manage multiple related incidents

### SIEM Advantages
- Centralized access to event data from diverse sources
- Real-time monitoring, detection, and alerting
- Historical log storage for investigations
- Correlation of events across multiple systems


## Module 2: Network monitoring and analysis

### 1. Network Traffic Fundamentals

- **Network traffic**: The amount of data moving across a network
- **Network data**: The actual data transmitted between devices on a network
- **Flow**: Movement of network communications (packets, protocols, ports)
- **Baseline**: Reference point of normal network behavior that helps identify abnormal activity

### 2. Attack Detection Through Network Monitoring

- **Data exfiltration**: Unauthorized transmission of data from a system
- **Indicators of Compromise (IoC)**: Observable evidence suggesting signs of a security incident
- **Signs of data exfiltration**:
  - Large internal file transfers
  - Large external uploads
  - Unexpected file writes
  - Outbound traffic from unusual locations/times
  - Communications on unusual ports/protocols

- **Attacker methodology** for data exfiltration:
  1. Gain initial access (often through phishing)
  2. Perform lateral movement (pivoting)
  3. Identify valuable assets
  4. Collect, package, and prepare data
  5. Exfiltrate data

- **Defense strategies**:
  1. Prevent access (e.g., multi-factor authentication)
  2. Monitor network for suspicious activity
  3. Protect assets with proper inventory and controls
  4. Detect and stop exfiltration through monitoring

### 3. Network Protocol Analyzers (Packet Sniffers)

- **Packet sniffing**: Capturing and inspecting data packets across a network
- **Network protocol analyzers**: Tools that capture and analyze data traffic
- **Function**: Place themselves in the middle of communications to capture data packets

- **How they work**:
  1. NIC must be in monitoring/promiscuous mode to access all visible packets
  2. Convert binary packet data to human-readable format
  3. Display information for analysis

- **Common packet sniffers**:
  - **tcpdump**: Command-line based analyzer for Unix-like systems
  - **Wireshark**: GUI-based open-source analyzer with visual interface
  - **TShark**: Command-line version of Wireshark

### 4. Packet Structure and Analysis

- **Packet components**:
  - **Header**: Routing/addressing information (like envelope address)
  - **Payload**: Actual data being transmitted (like letter contents)
  - **Footer**: End marker, sometimes used for error-checking (not in all protocols)

- **IPv4 Header Fields**:
  - **Version**: Specifies IP version (IPv4 or IPv6)
  - **IHL (Internet Header Length)**: Length of the IP header
  - **ToS (Type of Service)**: Priority information for packet delivery
  - **Total Length**: Length of entire packet (header + data)
  - **Identification, Flags, Fragment Offset**: Handle packet fragmentation
  - **TTL (Time to Live)**: Limits how long packet can circulate before being dropped
  - **Protocol**: Specifies protocol used (e.g., TCP=6)
  - **Header Checksum**: Used for error detection
  - **Source/Destination Address**: IP addresses of sender/receiver
  - **Options**: Optional field for network troubleshooting

- **IPv6 Header Fields** (differences from IPv4):
  - **Traffic Class**: Similar to IPv4 ToS
  - **Flow Label**: Identifies packets of a specific flow
  - **Payload Length**: Length of just the data portion
  - **Next Header**: Indicates header following IPv6 header
  - **Hop Limit**: Similar to IPv4 TTL

### 5. Using tcpdump

- **Basic syntax**: `sudo tcpdump [-i interface] [option(s)] [expression(s)]`
- **Interface selection**: `-i any` captures on all interfaces

- **Key options**:
  - `-w filename.pcap`: Write captured packets to a file
  - `-r filename.pcap`: Read packets from a file
  - `-v, -vv, -vvv`: Verbose mode (increasing detail)
  - `-c number`: Capture specified number of packets
  - `-n`: Disable name resolution (IP addresses shown as numbers)
  - `-nn`: Disable name and port resolution

- **Expressions**:
  - Filter by protocol: `tcp`, `udp`, `icmp`, `ip`, `ip6`
  - Filter by host: `host 192.168.1.1`
  - Filter by port: `port 80`
  - Boolean operators: `and`, `or`, `not`
  - Complex filters: `'ip and (port 80 or port 443)'`

- **Output interpretation**:
  - Timestamp: When packet was captured
  - Source/destination addresses and ports
  - Protocol details and flags

### 6. Using Wireshark

- **Display filters**:
  - Protocol filtering: `dns`, `http`, `ftp`, `ssh`, etc.
  - IP filtering: `ip.addr == 192.168.1.1`, `ip.src == 10.10.10.10`, `ip.dst == 4.4.4.4`
  - MAC filtering: `eth.addr == 00:70:f4:23:18:c4`
  - Port filtering: `tcp.port == 80`, `udp.port == 53`

- **Comparison operators**:
  - Equal: `==` or `eq`
  - Not equal: `!=` or `ne`
  - Greater than: `>` or `gt`
  - Less than: `<` or `lt`
  - Greater/less than or equal: `>=`/`<=` or `ge`/`le`

- **Other operators**:
  - `contains`: String matching (e.g., `http contains "moved"`)
  - `matches`: Regular expression matching

- **Following streams**: Reassembles conversation between devices for easier reading

### 7. Packet Capture File Formats

- **Libpcap**: Default format for Unix-like systems (used by tcpdump)
- **WinPcap**: Older format for Windows systems
- **Npcap**: Library by Nmap for Windows
- **PCAPng**: Modern "next generation" format that can capture and store data simultaneously

### 8. Network Monitoring & Security Context

- **Network Operations Center (NOC)**: Focuses on network performance and availability
- **Security Operations Center (SOC)**: Focuses on security threat detection and response
- **Command and Control (C2)**: Techniques used by attackers to maintain communications with compromised systems
- **Packet analysis applications**:
  - Security incident investigation
  - Network performance troubleshooting
  - Detecting data exfiltration
  - Identifying malware communications
  - Network baseline development

### 9. Soft Skills in Cybersecurity

- **Clear communication**: Ability to summarize complex information
- **Open mindset**: Willingness to adapt to changing threats
- **Curiosity**: Leaving no stone unturned in investigations
- **Diversity of thought**: Different perspectives improve security solutions

# Module 3: Incident Investigation and Response

This module focuses on the processes and procedures involved in the lifecycle of a cybersecurity incident, aligning with the NIST framework. Key areas include detection, analysis, investigation, response, documentation, and post-incident activities.

## 1. Detection and Analysis Phase

* **Goal:** Promptly discover security events and then investigate/validate alerts to determine if an incident has occurred. Remember, all incidents are events, but not all events (like website visits or password resets) are incidents.
* **Tools:** Intrusion Detection Systems (IDS) and Security Information and Event Management (SIEM) tools collect and analyze data from various sources to identify unusual activity and potential intrusions, triggering alerts.
* **Challenges:** It's impossible to detect everything due to tool limitations or incomplete deployment. Analysts often face high alert volumes, frequently caused by misconfigured rules (false positives) or sometimes genuine widespread attacks.
* **Detection Methods:**
    * **Threat Hunting:** Proactively searching for threats missed by automated tools, combining technology with human analysis and threat intelligence. Hunters use threat intelligence, IoCs, IoAs, and machine learning.
    * **Threat Intelligence:** Using evidence-based information (from industry reports, government advisories, data feeds) to understand existing/emerging threats and attacker TTPs. Threat Intelligence Platforms (TIPs) help manage and analyze this data.
    * **Cyber Deception:** Employing decoys like honeypots (fake vulnerable systems/resources) to attract and alert on malicious actors' activity.
* **CI/CD Pipeline Monitoring:** Continuously monitoring CI/CD pipelines is crucial for supply chain security. Automation helps detect unusual activity (IoCs) in build processes, code, or deployments. Common CI/CD IoCs include unauthorized code changes, suspicious deployment patterns, compromised dependencies, unusual pipeline execution, and secret exposure attempts. Monitoring involves comprehensive logging (execution, commit, access, deployment), SIEM integration for anomaly detection, real-time alerting, performance monitoring, and vulnerability scanning.

## 2. Indicators & Investigation Tools

* **Indicators:**
    * **Indicators of Compromise (IoCs):** Observable evidence suggesting a *potential past* incident (e.g., malicious file hash, IP address). They help identify the 'who' and 'what'. *Note: IoCs aren't always confirmation of an incident*.
    * **Indicators of Attack (IoAs):** Observed events indicating a *real-time* incident, focusing on attacker behavior ('why' and 'how'). E.g., a process making a network connection.
* **Pyramid of Pain:** Ranks IoCs based on the difficulty ("pain") caused to attackers when blocked. Blocking higher-level IoCs is more effective. Levels (from easiest to hardest for attackers to change): Hash values, IP addresses, Domain names, Network artifacts, Host artifacts, Tools, Tactics, Techniques, and Procedures (TTPs).
* **Investigative Tools & Context:** Analyze IoCs using tools to add context via threat intelligence (crowdsourced or OSINT) for a broader understanding. Examples:
    * **VirusTotal:** Analyzes suspicious files, domains, URLs, IPs using multiple vendor engines and community input. Provides detection verdicts, details (hashes, file types), relations (contacted domains, dropped files), behavior analysis, and community comments.
    * **Others:** Jotti's malware scan, Urlscan.io, MalwareBazaar.

## 3. Documentation & Evidence Handling

* **Importance:** Essential for transparency (legal/regulatory proof), standardization (consistent processes/policies), and clarity (understanding roles/tasks).
* **Chain of Custody:** Critical process for documenting the handling (possession, control, transfer) of evidence throughout an incident's lifecycle. Ensures evidence integrity and admissibility in legal proceedings. A 'broken chain' occurs with inconsistencies, potentially compromising evidence reliability. Forms typically log evidence description, who handled it, when, where, and why.
* **Best Practices:** Know your audience (tailor language/detail), be concise (establish purpose quickly), and update documentation regularly to reflect evolving threats and processes.

## 4. Incident Response Plans & Playbooks

* **Incident Response Plan (IRP):** A formal document outlining procedures for each step of incident response, establishing standardization.
* **Playbooks:** Manuals providing specific, step-by-step instructions for responding to particular incident types (e.g., malware, DDoS). They offer structure, reduce guesswork, and enable faster, more effective responses. Can be non-automated, fully automated (via SIEM/SOAR tools), or semi-automated. Must be regularly updated.

## 5. Triage

* **Purpose:** Prioritizing incidents based on urgency and potential impact (considering confidentiality, integrity, availability) to manage limited resources effectively.
* **Process:**
    1.  **Receive & Assess:** Validate the alert (check for false positives, history, related known vulnerabilities, severity).
    2.  **Assign Priority:** Determine urgency based on factors like functional impact (effect on business operations), information impact (data compromise), and recoverability (effort/cost vs. benefit).
    3.  **Collect & Analyze:** Gather evidence (e.g., logs), conduct research, add context by asking questions (e.g., unusual timing/location for logins), and document findings thoroughly before deciding on escalation or closure.
* **Benefits:** Efficient resource management and a standardized approach to handling alerts.

## 6. Containment, Eradication, and Recovery Phase

* **Goal:** Limit damage, remove the threat, and restore normal operations.
* **Containment:** Actions to limit the incident's spread and prevent further damage (e.g., isolating an infected machine from the network). Strategies vary by incident type and are outlined in the IRP.
* **Eradication:** Completely removing all elements of the incident from affected systems (e.g., deleting malware, patching exploited vulnerabilities).
* **Recovery:** Restoring affected systems and services to normal operation (e.g., reimaging systems from clean backups, resetting compromised passwords, restoring firewall rules).

## 7. Business Continuity & Resilience

* **Business Continuity Plan (BCP):** Outlines procedures to sustain critical business functions during and after major disruptions (distinct from Disaster Recovery Plans focused on IT system recovery from disasters). Essential for minimizing operational impact from incidents like ransomware.
* **Resilience:** The ability to prepare for, respond to, and recover from disruptions. Site resilience ensures infrastructure availability via recovery sites:
    * **Hot Site:** Fully operational duplicate, immediate activation.
    * **Warm Site:** Configured duplicate, requires some setup time.
    * **Cold Site:** Basic infrastructure, requires significant setup.

## 8. Post-Incident Activity Phase

* **Goal:** Learn from the incident to improve future responses and overall security posture.
* **Lessons Learned Meeting (Post-Mortem):** A meeting held shortly after incident resolution (ideally within two weeks) involving all relevant parties. Focuses on reviewing what happened, actions taken, effectiveness, and identifying improvements without assigning blame. Should result in actionable recommendations.
* **Final Report:** Comprehensive documentation reviewing the incident. Includes an executive summary, detailed timeline, investigation findings, and recommendations for prevention. Should be tailored to the intended audience (e.g., less technical for executives).
