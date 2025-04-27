# Detection and Response in Cybersecurity
## Course 6, Module 1: Introduction to Detection and Incident Response

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
