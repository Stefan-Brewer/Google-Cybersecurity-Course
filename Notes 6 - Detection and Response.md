## Course 6: Sound the Alarm: Detection and Response

### Module 1: Introduction to Detection and Incident Response

#### 1. Incident Response Fundamentals
* **Incident Response Lifecycle:** Based on the NIST Cybersecurity Framework (CSF) focusing on Detect (monitor systems to identify security events), Respond (take action when incidents occur), and Recover (restore affected systems to normal operation).
* **NIST Incident Response Lifecycle:** Includes Preparation (planning and readiness before incidents occur), Detection and Analysis (identifying and investigating potential incidents), Containment, Eradication, and Recovery (limiting damage, removing threats, restoring systems), and Post-incident Activity (documentation, lessons learned, process improvement).
* **Events vs. Incidents:** Event is any observable occurrence on a network, system, or device; Incident is an event that jeopardizes confidentiality, integrity, or availability of information systems or violates security policies. Key distinction: All security incidents are events, but not all events are security incidents.
* **The Five W's of Incident Investigation:** Who triggered the incident, What happened, When the incident took place, Where the incident took place, and Why the incident occurred.

#### 2. Incident Response Teams and Organization
* **Computer Security Incident Response Teams (CSIRT):** Specialized group trained in incident management and response. Goals: Effectively manage incidents, provide response resources, prevent future incidents. Works cross-functionally with other departments (legal, PR, etc.).
* **Key Security Roles:** Security Analyst (investigates alerts, determines incident criticality, performs initial triage), Technical Lead (provides technical guidance throughout the incident lifecycle), Incident Coordinator (tracks and manages CSIRT activities, ensures processes are followed).
* **Security Operations Center (SOC):** Dedicated to monitoring networks, systems, and devices for security threats. Organizational structure includes Tier 1 SOC Analyst (alert monitoring, prioritization, initial response), Tier 2 SOC Analyst (deeper investigations, security tool configuration), Tier 3 SOC Lead (advanced detection techniques, forensics, malware analysis), and SOC Manager (team leadership, performance metrics, stakeholder communication).
* **Command, Control, and Communication:** Command (leadership and direction overseeing the response), Control (technical management of resources and tasks), Communication (keeping stakeholders informed).

#### 3. Incident Response Documentation and Planning
* **Incident Response Plan:** Formal document outlining procedures for incident response, tailored to organization's unique requirements (mission, size, industry). Common elements include incident response procedures, system information (network diagrams, asset inventory, logging), and supporting documents (contact lists, forms, templates).
* **Documentation Types and Tools:** Incident Handler's Journal (records incident details and investigation notes), Playbooks (step-by-step manuals for operational actions), Final Reports (complete incident summaries). Tools include word processors, ticketing systems, spreadsheets, audio/visual recording.
* **Effective Documentation Principles:** Reduces uncertainty and confusion during high-pressure incidents, should be clear, consistent, and accurate, and enables swift and decisive response.

#### 4. Detection Tools and Technologies
* **Intrusion Detection System (IDS):** Monitors system activity and alerts on possible intrusions but does not prevent/stop it. Examples: Zeek, Suricata, Snort, Sagan.
* **Intrusion Prevention System (IPS):** Monitors system activity AND takes action to stop intrusive activity. Has all IDS capabilities plus active prevention. Many tools (Suricata, Snort, Sagan) can function as both IDS and IPS.
* **Endpoint Detection and Response (EDR):** Monitors endpoints (computers, phones, tablets) for malicious activity, performs behavioral analysis using ML/AI to identify threat patterns, and can automatically stop attacks without manual intervention. Examples: Open EDR, Bitdefender EDR, FortiEDR.
* **Detection Categories:** True Positive (correctly detects an actual attack), True Negative (correctly identifies no malicious activity), False Positive (incorrectly identifies legitimate activity as malicious), False Negative (fails to detect actual malicious activity).

#### 5. Alert and Event Management Systems
* **Security Information and Event Management (SIEM):** Collects and analyzes log data to monitor critical activities and provides high-level overview of network security status. Process includes collecting and aggregating data, normalizing data, and analyzing data. Examples: AlienVault OSSIM, Chronicle, Elastic, Splunk, IBM QRadar.
* **Security Orchestration, Automation, and Response (SOAR):** Uses automation to respond to security events, automates analysis and response processes, provides case management capabilities, and can track and manage multiple related incidents.
* **SIEM Advantages:** Centralized access to event data from diverse sources, real-time monitoring, detection, and alerting, historical log storage for investigations, and correlation of events across multiple systems.

### Module 2: Network Monitoring and Analysis

#### 1. Network Traffic Fundamentals
* **Network Traffic:** The amount of data moving across a network.
* **Network Data:** The actual data transmitted between devices on a network.
* **Flow:** Movement of network communications (packets, protocols, ports).
* **Baseline:** Reference point of normal network behavior that helps identify abnormal activity.

#### 2. Attack Detection Through Network Monitoring
* **Data Exfiltration:** Unauthorized transmission of data from a system.
* **Indicators of Compromise (IoC):** Observable evidence suggesting signs of a security incident.
* **Signs of Data Exfiltration:** Large internal file transfers, large external uploads, unexpected file writes, outbound traffic from unusual locations/times, communications on unusual ports/protocols.
* **Attacker Methodology for Data Exfiltration:** Gain initial access (often through phishing), perform lateral movement (pivoting), identify valuable assets, collect, package, and prepare data, exfiltrate data.
* **Defense Strategies:** Prevent access (e.g., multi-factor authentication), monitor network for suspicious activity, protect assets with proper inventory and controls, detect and stop exfiltration through monitoring.

#### 3. Network Protocol Analyzers (Packet Sniffers)
* **Packet Sniffing:** Capturing and inspecting data packets across a network.
* **Network Protocol Analyzers:** Tools that capture and analyze data traffic by placing themselves in the middle of communications to capture data packets.
* **How They Work:** NIC must be in monitoring/promiscuous mode to access all visible packets, convert binary packet data to human-readable format, display information for analysis.
* **Common Packet Sniffers:** tcpdump (command-line based analyzer for Unix-like systems), Wireshark (GUI-based open-source analyzer with visual interface), TShark (command-line version of Wireshark).

#### 4. Packet Structure and Analysis
* **Packet Components:** Header (routing/addressing information, like envelope address), Payload (actual data being transmitted, like letter contents), Footer (end marker, sometimes used for error-checking, not in all protocols).
* **IPv4 Header Fields:** Version, IHL (Internet Header Length), ToS (Type of Service), Total Length, Identification/Flags/Fragment Offset (handle packet fragmentation), TTL (Time to Live), Protocol, Header Checksum, Source/Destination Address, Options.
* **IPv6 Header Fields (differences from IPv4):** Traffic Class (similar to IPv4 ToS), Flow Label (identifies packets of a specific flow), Payload Length (length of just the data portion), Next Header (indicates header following IPv6 header), Hop Limit (similar to IPv4 TTL).

#### 5. Using tcpdump
* **Basic Syntax:** `sudo tcpdump [-i interface] [option(s)] [expression(s)]`
* **Interface Selection:** `-i any` captures on all interfaces.
* **Key Options:** `-w filename.pcap` (write captured packets to a file), `-r filename.pcap` (read packets from a file), `-v`, `-vv`, `-vvv` (verbose mode with increasing detail), `-c number` (capture specified number of packets), `-n` (disable name resolution), `-nn` (disable name and port resolution).
* **Expressions:** Filter by protocol (`tcp`, `udp`, `icmp`, `ip`, `ip6`), filter by host (`host 192.168.1.1`), filter by port (`port 80`), Boolean operators (`and`, `or`, `not`), complex filters (`'ip and (port 80 or port 443)'`).
* **Output Interpretation:** Timestamp (when packet was captured), source/destination addresses and ports, protocol details and flags.

#### 6. Using Wireshark
* **Display Filters:** Protocol filtering (`dns`, `http`, `ftp`, `ssh`, etc.), IP filtering (`ip.addr == 192.168.1.1`, `ip.src == 10.10.10.10`, `ip.dst == 4.4.4.4`), MAC filtering (`eth.addr == 00:70:f4:23:18:c4`), port filtering (`tcp.port == 80`, `udp.port == 53`).
* **Comparison Operators:** Equal (`==` or `eq`), not equal (`!=` or `ne`), greater than (`>` or `gt`), less than (`<` or `lt`), greater/less than or equal (`>=`/`<=` or `ge`/`le`).
* **Other Operators:** `contains` for string matching (e.g., `http contains "moved"`), `matches` for regular expression matching.
* **Following Streams:** Reassembles conversation between devices for easier reading.

#### 7. Packet Capture File Formats
* **Libpcap:** Default format for Unix-like systems (used by tcpdump).
* **WinPcap:** Older format for Windows systems.
* **Npcap:** Library by Nmap for Windows.
* **PCAPng:** Modern "next generation" format that can capture and store data simultaneously.

#### 8. Network Monitoring & Security Context
* **Network Operations Center (NOC):** Focuses on network performance and availability.
* **Security Operations Center (SOC):** Focuses on security threat detection and response.
* **Command and Control (C2):** Techniques used by attackers to maintain communications with compromised systems.
* **Packet Analysis Applications:** Security incident investigation, network performance troubleshooting, detecting data exfiltration, identifying malware communications, network baseline development.

#### 9. Soft Skills in Cybersecurity
* **Clear Communication:** Ability to summarize complex information.
* **Open Mindset:** Willingness to adapt to changing threats.
* **Curiosity:** Leaving no stone unturned in investigations.
* **Diversity of Thought:** Different perspectives improve security solutions.

### Module 3: Incident Investigation and Response

#### 1. Detection and Analysis Phase
* **Goal:** Promptly discover security events and then investigate/validate alerts to determine if an incident has occurred.
* **Tools:** Intrusion Detection Systems (IDS) and Security Information and Event Management (SIEM) tools collect and analyze data from various sources to identify unusual activity and potential intrusions, triggering alerts.
* **Challenges:** It's impossible to detect everything due to tool limitations or incomplete deployment. Analysts often face high alert volumes, frequently caused by misconfigured rules (false positives) or sometimes genuine widespread attacks.
* **Detection Methods:**
  * **Threat Hunting:** Proactively searching for threats missed by automated tools, combining technology with human analysis and threat intelligence. Hunters use threat intelligence, IoCs, IoAs, and machine learning.
  * **Threat Intelligence:** Using evidence-based information (from industry reports, government advisories, data feeds) to understand existing/emerging threats and attacker TTPs. Threat Intelligence Platforms (TIPs) help manage and analyze this data.
  * **Cyber Deception:** Employing decoys like honeypots (fake vulnerable systems/resources) to attract and alert on malicious actors' activity.
  * **CI/CD Pipeline Monitoring:** Continuously monitoring CI/CD pipelines is crucial for supply chain security. Automation helps detect unusual activity (IoCs) in build processes, code, or deployments. Common CI/CD IoCs include unauthorized code changes, suspicious deployment patterns, compromised dependencies, unusual pipeline execution, and secret exposure attempts. Monitoring involves comprehensive logging (execution, commit, access, deployment), SIEM integration for anomaly detection, real-time alerting, performance monitoring, and vulnerability scanning.

#### 2. Indicators & Investigation Tools
* **Indicators:**
  * **Indicators of Compromise (IoCs):** Observable evidence suggesting a potential past incident (e.g., malicious file hash, IP address). They help identify the 'who' and 'what'. Note: IoCs aren't always confirmation of an incident.
  * **Indicators of Attack (IoAs):** Observed events indicating a real-time incident, focusing on attacker behavior ('why' and 'how'). E.g., a process making a network connection.
  * **Pyramid of Pain:** Ranks IoCs based on the difficulty ("pain") caused to attackers when blocked. Blocking higher-level IoCs is more effective. Levels (from easiest to hardest for attackers to change): Hash values, IP addresses, Domain names, Network artifacts, Host artifacts, Tools, Tactics, Techniques, and Procedures (TTPs).
* **Investigative Tools & Context:** Analyze IoCs using tools to add context via threat intelligence (crowdsourced or OSINT) for a broader understanding. Examples:
  * **VirusTotal:** Analyzes suspicious files, domains, URLs, IPs using multiple vendor engines and community input. Provides detection verdicts, details (hashes, file types), relations (contacted domains, dropped files), behavior analysis, and community comments.
  * **Others:** Jotti's malware scan, Urlscan.io, MalwareBazaar.

#### 3. Documentation & Evidence Handling
* **Importance:** Essential for transparency (legal/regulatory proof), standardization (consistent processes/policies), and clarity (understanding roles/tasks).
* **Chain of Custody:** Critical process for documenting the handling (possession, control, transfer) of evidence throughout an incident's lifecycle. Ensures evidence integrity and admissibility in legal proceedings. A 'broken chain' occurs with inconsistencies, potentially compromising evidence reliability. Forms typically log evidence description, who handled it, when, where, and why.
* **Best Practices:** Know your audience (tailor language/detail), be concise (establish purpose quickly), and update documentation regularly to reflect evolving threats and processes.

#### 4. Incident Response Plans & Playbooks
* **Incident Response Plan (IRP):** A formal document outlining procedures for each step of incident response, establishing standardization.
* **Playbooks:** Manuals providing specific, step-by-step instructions for responding to particular incident types (e.g., malware, DDoS). They offer structure, reduce guesswork, and enable faster, more effective responses. Can be non-automated, fully automated (via SIEM/SOAR tools), or semi-automated. Must be regularly updated.

#### 5. Triage
* **Purpose:** Prioritizing incidents based on urgency and potential impact (considering confidentiality, integrity, availability) to manage limited resources effectively.
* **Process:**
  * **Receive & Assess:** Validate the alert (check for false positives, history, related known vulnerabilities, severity).
  * **Assign Priority:** Determine urgency based on factors like functional impact (effect on business operations), information impact (data compromise), and recoverability (effort/cost vs. benefit).
  * **Collect & Analyze:** Gather evidence (e.g., logs), conduct research, add context by asking questions (e.g., unusual timing/location for logins), and document findings thoroughly before deciding on escalation or closure.
* **Benefits:** Efficient resource management and a standardized approach to handling alerts.

#### 6. Containment, Eradication, and Recovery Phase
* **Goal:** Limit damage, remove the threat, and restore normal operations.
* **Containment:** Actions to limit the incident's spread and prevent further damage (e.g., isolating an infected machine from the network). Strategies vary by incident type and are outlined in the IRP.
* **Eradication:** Completely removing all elements of the incident from affected systems (e.g., deleting malware, patching exploited vulnerabilities).
* **Recovery:** Restoring affected systems and services to normal operation (e.g., reimaging systems from clean backups, resetting compromised passwords, restoring firewall rules).

#### 7. Business Continuity & Resilience
* **Business Continuity Plan (BCP):** Outlines procedures to sustain critical business functions during and after major disruptions (distinct from Disaster Recovery Plans focused on IT system recovery from disasters). Essential for minimizing operational impact from incidents like ransomware.
* **Resilience:** The ability to prepare for, respond to, and recover from disruptions. Site resilience ensures infrastructure availability via recovery sites:
  * **Hot Site:** Fully operational duplicate, immediate activation.
  * **Warm Site:** Configured duplicate, requires some setup time.
  * **Cold Site:** Basic infrastructure, requires significant setup.

#### 8. Post-Incident Activity Phase
* **Goal:** Learn from the incident to improve future responses and overall security posture.
* **Lessons Learned Meeting (Post-Mortem):** A meeting held shortly after incident resolution (ideally within two weeks) involving all relevant parties. Focuses on reviewing what happened, actions taken, effectiveness, and identifying improvements without assigning blame. Should result in actionable recommendations.
* **Final Report:** Comprehensive documentation reviewing the incident. Includes an executive summary, detailed timeline, investigation findings, and recommendations for prevention. Should be tailored to the intended audience (e.g., less technical for executives).

### Module 4: Network Traffic and Logs using IDS and SIEM Tools

#### 1. The Importance and Analysis of Logs
* **Logs:** Records of observable events occurring within an organization's systems, networks, or devices. They detail the what, where, and when of an event, including actions and users/systems involved.
* **Purpose:** Logs are crucial for security professionals to detect unusual or malicious activity, troubleshoot system issues, and support incident investigations by building a timeline and understanding events.
* **Log Analysis:** The process of examining logs to identify events of interest. This helps create context around alerts and interpret actions taken on a system.
* **Log Management:** The process of collecting, storing, analyzing, and disposing of log data. Best practices include:
  * **Selective Logging:** Choosing what to log is crucial to manage volume and efficiency, potentially excluding excessive verbosity or non-relevant data. Be mindful of regulations regarding Personally Identifiable Information (PII).
  * **Avoiding Overlogging:** Logging everything can increase costs, strain systems, and make searching difficult.
  * **Log Retention:** Policies should define how long logs are kept, often dictated by industry regulations (e.g., FISMA, HIPAA, PCI DSS, SOX).
  * **Log Protection:** Storing logs on a centralized, dedicated server helps maintain integrity and makes it harder for attackers to modify or hide their activity.
* **Log Collection:** Software called log forwarders automatically collect logs from various sources (network devices, OS, applications, security tools, authentication systems) and send them to a centralized repository like a SIEM.
* **Telemetry:** Refers to the collection and transmission of data (like logs or packet captures) for analysis. Logs and telemetry serve as evidence during investigations.

#### 2. Common Log Formats
* **Syslog:** A standard protocol for transporting logs and a common log format, especially in Unix® systems. It typically includes a header (timestamp, hostname, app name, message ID), optional structured data (key-value pairs), and a message. It also has a Priority (PRI) field indicating urgency.
* **JSON (JavaScript Object Notation):** A lightweight, text-based format using key-value pairs, commas, quotes, curly brackets (for objects), and square brackets (for arrays). Known for simplicity and readability, often used in web and cloud environments.
* **XML (eXtensible Markup Language):** Uses tags (start and end pairs like `<tag>`, `</tag>`), elements (data + tags), and attributes (additional info within tags) to structure data. Native format in Windows systems.
* **CSV (Comma Separated Value):** Uses separators (like commas) to distinguish data values. The position of data often corresponds to its field name, which might not be explicitly included.
* **CEF (Common Event Format):** Uses key-value pairs and a defined structure separated by pipe characters (`|`). Structure: `CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension`. The Extension part uses key-value pairs. Often transported via Syslog.

#### 3. Intrusion Detection Systems (IDS)
* **IDS:** An application that monitors system or network activity and alerts on possible intrusions.
* **Types:**
  * **Host-based IDS (HIDS):** Monitors the activity of the single host (endpoint) it's installed on. Can monitor internal activity like file systems, system resources, and user actions.
  * **Network-based IDS (NIDS):** Collects and analyzes network traffic at specific points in the network. Often deployed at multiple points for visibility.
* **Detection Methods:**
  * **Signature-based Analysis:** Detects known threats by matching activity against predefined patterns (signatures) associated with malicious activity (e.g., specific byte sequences, IP addresses). Advantages: Low false positive rate for known threats. Disadvantages: Can be evaded by modifying attacks, requires constant signature updates, cannot detect unknown (zero-day) threats.
  * **Anomaly-based Analysis:** Identifies threats by detecting deviations from an established baseline of normal behavior. Involves a training phase to establish the baseline and a detection phase to compare current activity against it. Advantages: Can detect new and unknown threats. Disadvantages: High rate of false positives, baseline can be corrupted if an attacker is present during training.
* **IDS Signatures/Rules (NIDS):** Specify detection rules defining what intrusions to look for. Generally consist of:
  * **Action:** What to do if criteria are met (e.g., `alert`, `pass`, `drop`, `reject`).
  * **Header:** Defines the traffic parameters (protocol, source/destination IPs, source/destination ports, direction).
  * **Rule Options:** Additional parameters to customize the rule (e.g., matching packet content, specifying alert messages, signature ID, revision number). Enclosed in parentheses, separated by semicolons.
* **Suricata:** An open-source tool that functions as an IDS (network or host-based), Intrusion Prevention System (IPS), and Network Security Monitoring (NSM) tool.
  * Uses rules/signatures (terms often used interchangeably) for detection. Syntax follows the Action, Header, Rule Options structure. Rule order matters for processing.
  * Custom rules are highly recommended to tailor detection to specific environments and reduce false positives.
  * Configuration is done via the `suricata.yaml` file.
  * Generates logs, primarily `eve.json` (standard, detailed JSON format, better for analysis/SIEM ingestion) and `fast.log` (minimal alert info, legacy format).
  * `eve.json` uses `flow_id` to correlate related logs to a single network flow.

#### 4. Security Information and Event Management (SIEM) Tools
* **SIEM:** An application that collects, normalizes, correlates, and analyzes log data from multiple sources across an organization to monitor critical activities and identify security incidents.
* **SIEM Process:**
  1. **Collect & Aggregate:** Gathers vast amounts of log data from diverse sources. Log ingestion is the process of importing this data. Log forwarders often automate this.
  2. **Normalize:** Converts disparate log formats into a single, consistent format for easier analysis and searching.
  3. **Analyze & Index:** Analyzes data, correlates events to find patterns, and indexes data for fast searching.
* **Benefits:** Provides a centralized view, processes large volumes of data in real-time, enables quick searching and analysis, and aids in incident investigation.
* **SIEM Querying:** Accessing data stored in SIEMs requires using search queries. Specific queries yield faster, more relevant results than broad ones.
* **Specific SIEM Tools:**
  * **Splunk:** A data analysis platform with SIEM capabilities (Splunk Enterprise Security). Uses its own query language, **Search Processing Language (SPL)**.
    * SPL searches can filter, transform, and visualize data.
    * Uses the pipe character (`|`) to chain commands, sending the output of one to the next.
    * Supports wildcards (e.g., `*`) to match variations in search terms (like `fail*` matching `fail`, `failed`, `failure`).
    * Uses `index=` to specify the data source to search.
    * Double quotes (`"`) search for exact phrases.
  * **Google SecOps (Chronicle):** Google Cloud's SIEM. Uses **YARA-L** language for detection rules.
    * Searches can target specific fields like hostname, IP, domain, username, etc.
    * Offers **UDM Search** (Unified Data Model) which searches normalized, structured data (faster, default). UDM events have common fields like entities (device, user), event metadata (type, timestamp), network metadata, and security results.
    * Offers **Raw Log Search** which searches original, unparsed logs (slower, used when normalized data is insufficient or for troubleshooting). Supports regular expressions.
    * Provides filtering capabilities (Procedural Filtering) to refine results.
