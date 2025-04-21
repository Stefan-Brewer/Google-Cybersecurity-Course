# Asset Security: Comprehensive Study Notes

## Core Security Concepts

### Fundamental Definitions
- **Asset**: Any item perceived as having value to an organization
- **Threat**: Any circumstance or event that can negatively impact assets
- **Vulnerability**: A weakness that can be exploited by a threat
- **Risk**: Anything that can impact the confidentiality, integrity, or availability of an asset
  - Risk can be calculated as: `Likelihood × Impact = Risk`

### CIA Triad
The primary focus of security practitioners is to maintain:
- **Confidentiality**: Protecting information from unauthorized access
- **Integrity**: Ensuring information remains accurate and unaltered
- **Availability**: Making sure information is accessible when needed

## Asset Management

### Asset Inventory and Classification
- **Asset inventory**: A catalog of assets that need to be protected
- **Asset management**: The process of tracking assets and the risks that affect them
- **Asset classification**: Labeling assets based on sensitivity and importance

### Classification Levels (from least to most restricted)
1. **Public**: Can be shared with anyone
2. **Internal-only**: Available to employees and partners but not outside the organization
3. **Confidential**: Limited to those working on a specific project
4. **Restricted**: Highly sensitive, need-to-know basis

### Asset Classification Considerations
- What you have
- Where it is
- Who owns it
- How important it is

## Data Security

### States of Data
1. **Data in use**: Being accessed by one or more users
2. **Data in transit**: Traveling from one point to another
3. **Data at rest**: Not currently being accessed (typically stored on physical device)

### Information Security (InfoSec)
The practice of keeping data in all states away from unauthorized users, protecting against:
- Identity theft
- Financial loss
- Reputational damage

## Cloud Security

### Cloud-Based Service Models
1. **Software as a Service (SaaS)**: Front-end applications accessed via web browser
   - Examples: Gmail, Slack, Zoom
2. **Platform as a Service (PaaS)**: Development tools accessed online
   - Examples: Google App Engine, Heroku, VMware Cloud Foundry
3. **Infrastructure as a Service (IaaS)**: Remote access to back-end systems

### Shared Responsibility Model
- Clients are responsible for securing elements within their control:
  - Identity and access management
  - Resource configuration
  - Data handling
- Service providers secure underlying infrastructure

### Cloud Security Challenges
- Misconfiguration issues
- Cloud-native breaches
- Access monitoring difficulties
- Regulatory compliance (HIPAA, PCI DSS, GDPR)

## Security Planning and Compliance

### Security Plan Elements
1. **Policies**: Set of rules that reduce risk and protect information
   - Address what we're protecting and why
   - Example: Acceptable Use Policy (AUP)
2. **Standards**: References that inform how to set policies
   - Example: NIST password requirements
3. **Procedures**: Step-by-step instructions for security tasks
   - Example: Password reset process

### Compliance
- Process of adhering to internal standards and external regulations
- Regulations: Rules set by government/authority to control how something is done

## NIST Cybersecurity Framework (CSF)

### Main Components
1. **Core**: Key functions of a security plan
   - **Identify**: Asset management, risk assessment
   - **Protect**: Controls to safeguard assets
   - **Detect**: Identifying security events
   - **Respond**: Actions taken during an incident
   - **Recover**: Restoration after an incident
   - **Govern**: Leadership and decision-making (added 2024)

2. **Tiers**: Measures security performance maturity
   - Level 1 (Passive): Bare minimum standards
   - Level 4 (Adaptive): Exemplary implementation

3. **Profiles**: Templates tailored for specific industries or needs
   - Captures the current state of a security plan
   - Helps identify gaps and improvement areas

### Implementation Steps
1. Create a current profile of security operations
2. Perform risk assessment
3. Analyze and prioritize gaps
4. Implement action plan to achieve objectives

## Risk Management

### Risk Categories
- Damage to assets
- Disclosure of information
- Loss of information

### Risk Factors
- Physical damage
- Equipment malfunction
- Attacks
- Human error

### Threat Categories
- **Intentional**: Malicious hackers, deliberate attacks
- **Unintentional**: Employee mistakes, accidents

### Vulnerability Categories
- **Technical**: Misconfigured software, outdated systems
- **Human**: Forgetfulness, lack of training

## Security in Practice
- Security is a culture and shared responsibility
- Effective plans consider diverse backgrounds and perspectives
- Security planning is continuous as digital landscapes evolve
- Security professionals must stay current with best practices and trends
