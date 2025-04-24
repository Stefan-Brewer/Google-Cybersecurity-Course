# Asset Security: Comprehensive Study Notes

## Introduction to Asset Security

### Core Security Concepts

Security planning involves analyzing assets, threats, and vulnerabilities to manage risk effectively. Risk is anything impacting the confidentiality, integrity, or availability (CIA triad) of an asset. Security focuses on maintaining the CIA triad.

- **Asset**: An item perceived as having value to an organization. Examples include buildings, equipment, data, intellectual property, people, and brand reputation.
- **Threat**: Any circumstance or event that can negatively impact assets. Threats can be intentional (e.g., hackers) or unintentional (e.g., employee error, accidents).
- **Vulnerability**: A weakness in an asset that can be exploited by a threat. Vulnerabilities can be technical (e.g., misconfigured software) or human (e.g., forgetful employee).
- **Risk**: Calculated as Likelihood × Impact. Security aims to reduce the likelihood of negative events by addressing threats and vulnerabilities. Organizations analyze risk to prevent disruptions, identify improvements, determine acceptable risks, and prioritize critical assets.

### Asset Management & Classification

Security starts with knowing what needs protection.

- **Asset Management**: The process of tracking assets and the risks affecting them. You can only protect what you account for.
- **Asset Inventory**: A catalog of all assets needing protection. Essential for tracking and resource allocation.
- **Asset Classification**: Labeling assets based on their sensitivity and importance. Helps prioritize resources, manage risk, reduce costs, and ensure compliance. Classification determines how assets can be disclosed, altered, or destroyed.
  - **Common Levels**:
    - **Public**: Lowest level; no negative consequences if released.
    - **Internal-only**: Can be shared within the organization but not outside.
    - **Confidential**: Access restricted to those on specific projects; disclosure may cause significant negative impact.
    - **Restricted**: Highest level; typically highly sensitive, need-to-know information (e.g., intellectual property, health/payment info). (Note: Government classifications might differ, e.g., using "confidential" for the highest level).
- **Challenges**: Classifying information can be complex due to issues like determining ownership (especially on company devices used personally) and data having multiple sensitivity levels simultaneously (e.g., a letter containing public name and confidential address).

### Data States and Information Security (InfoSec)

In the digital world, information (data) is often the most valuable asset. Protecting data depends on its state.

- **Data States**:
  - **Data in Use**: Data being actively accessed/processed (e.g., checking email).
  - **Data in Transit**: Data traveling between points (e.g., sending an email).
  - **Data at Rest**: Data not currently being accessed, typically stored (e.g., email data on a closed laptop). (Note: Cloud storage complicates the idea of "at rest" for device data).
- **Information Security (InfoSec)**: The practice of protecting data in all states from unauthorized users. Weak InfoSec can lead to identity theft, financial loss, and reputational damage.

### Cloud Computing & Security

Cloud computing offers on-demand, scalable services over the internet, changing how businesses operate but introducing new security challenges.

- **Cloud Service Categories**:
  - **Software as a Service (SaaS)**: Front-end applications accessed via browser; provider manages all backend systems (e.g., Gmail, Slack).
  - **Platform as a Service (PaaS)**: Backend development tools accessed online; client builds/manages apps, provider manages underlying hardware/software (e.g., Google App Engine).
  - **Infrastructure as a Service (IaaS)**: Remote access to backend infrastructure (servers, storage, networking); client manages more, provider hosts hardware (e.g., Google Cloud Platform, Microsoft Azure).
- **Cloud Security**: Subfield focusing on protecting data, apps, and infrastructure in the cloud.
- **Shared Responsibility Model**: Security responsibilities are divided between the cloud provider and the client. Clients are typically responsible for identity/access management, resource configuration, and data handling. The provider's responsibility varies by service type (SaaS, PaaS, IaaS).
- **Challenges**: Misconfiguration (a major concern), difficulty monitoring access, and meeting regulatory compliance standards (HIPAA, PCI DSS, GDPR).

### Security Plans

Effective security requires a culture involving everyone, guided by a plan. Plans focus on people and address risks based on categories (damage, disclosure, loss) and factors (physical damage, malfunction, attacks, human error).

- **Elements**:
  - **Policies**: Foundational rules that reduce risk and protect information; address the "what" and "why" strategically (e.g., Acceptable Use Policy - AUP).
  - **Standards**: References informing how policies are set; provide benchmarks (e.g., NIST password standards like SP 800-63B).
  - **Procedures**: Step-by-step instructions for specific security tasks; ensure consistency and accountability (e.g., password reset procedure).

### Compliance and the NIST Cybersecurity Framework (CSF)

- **Compliance**: Adhering to internal standards and external regulations. Essential for maintaining trust, reputation, safety, data integrity, and avoiding penalties.
- **Regulations**: Rules set by authorities (e.g., government) controlling how things are done.
- **NIST Cybersecurity Framework (CSF)**: A voluntary framework of standards, guidelines, and best practices to manage cybersecurity risk, particularly for information assets. Developed by the U.S. National Institute of Standards and Technology. It's flexible and applicable across industries.
  - **CSF Components**:
    - **Core**: Identifies key cybersecurity outcomes via functions. Functions: Identify, Protect, Detect, Respond, Recover, and Govern (Govern added in 2024).
    - **Tiers**: Measure the sophistication of security practices (Tier 1: Partial/lowest to Tier 4: Adaptive/highest). Used for assessment and identifying improvement areas.
    - **Profiles**: Align functions/categories/subcategories with business requirements, risk tolerance, and resources; used to identify gaps and create action plans by comparing a "Current" Profile to a "Target" Profile. Can be baseline templates or comparisons to industry standards.
  - **Implementation**: Involves creating current/target profiles, performing risk assessments, analyzing gaps, and implementing an action plan. CISA provides guidance.

## Protect Organizational Assets

### Core Principles for Access Control

- **Principle of Least Privilege (PoLP)**: Grant users only the minimum level of access and authorization necessary to perform their specific tasks or functions. This reduces risk by limiting exposure of sensitive information and minimizing potential damage from accidental misuse or compromised accounts. PoLP should be applied to all assets. User accounts (Guest, User, Service, Privileged) should have baseline access levels determined, and privileges must be routinely audited (Usage, Privilege, Account Change Audits) to combat privilege creep.
- **Separation of Duties**: Divide tasks and responsibilities among different users to prevent any single user from having complete control over critical functions or misusing a system. This works alongside PoLP to limit both individual access and the scope of responsibilities.

### Data Lifecycle and Governance

- **Data Lifecycle**: Data flows through stages: Collect, Store, Use, Archive, Destroy. Security controls are needed at each stage to maintain the CIA triad (Confidentiality, Integrity, Availability).
- **Data Governance**: A structured approach defining how an organization manages data throughout its lifecycle, including privacy, accuracy, availability, and security policies. Key roles include Data Owner (decides access), Data Custodian (handles safe transport/storage), and Data Steward (maintains/implements policies). Security professionals often act as data custodians.

### Information Privacy and Regulations

- **Privacy vs. Security**: Privacy is about controlling personal information and how it's shared. Security is about protecting that information from threats. Both are crucial.
- **Legally Protected Information**:
  - **PII (Personally Identifiable Information)**: Information used to identify, contact, or locate an individual (e.g., name, address).
  - **PHI (Protected Health Information)**: Health-related information regulated by laws like HIPAA (US) and GDPR (EU).
  - **SPII (Sensitive PII)**: PII requiring stricter handling (e.g., bank accounts, login credentials).
- **Key Regulations**:
  - **GDPR (General Data Protection Regulation)**: EU regulation giving individuals control over their personal data; applies globally to businesses handling EU residents' data.
  - **PCI DSS (Payment Card Industry Data Security Standard)**: Financial industry standards to secure card transactions against fraud and theft.
  - **HIPAA (Health Insurance Portability and Accountability Act)**: US law protecting sensitive patient health information from disclosure without consent.
- **Compliance Verification**: Done through Security Audits (checking controls/policies against requirements) and Security Assessments (testing resilience against threats).

### Cryptography: Encryption and Hashing

- **Cryptography**: Transforming information so unintended readers cannot understand it. Involves Encryption (plaintext to ciphertext) and Decryption (ciphertext back to plaintext) using an Algorithm (cipher) and a Key.
- **Encryption Types**:
  - **Symmetric Encryption**: Uses a single secret key for both encryption and decryption. Faster but less secure if the key is compromised. Examples: 3DES, AES.
  - **Asymmetric Encryption**: Uses a public key (for encryption, shareable) and a private key (for decryption, kept secret) pair. More secure key management but slower. Examples: RSA, DSA.
- **Public Key Infrastructure (PKI)**: A framework using asymmetric/symmetric encryption and digital certificates to secure online information exchange. Digital Certificates verify a public key holder's identity, establishing trust. They are issued by a Certificate Authority (CA).
- **Key Length**: Longer keys are generally more secure against brute-force attacks but result in slower processing. AES (128, 192, 256 bits) and RSA (1024, 2048, 4096 bits) offer strong key lengths.
- **Kerckhoff's Principle**: A cryptosystem should be secure even if everything about the system, except the private key, is public knowledge. Security through obscurity is not real security.
- **Hashing**: A one-way function creating a unique, fixed-size digest (hash value) from an input. Used for Non-repudiation (ensuring authenticity/integrity) by verifying if data has been altered. Even a tiny change in input drastically changes the output hash.
- **Hashing Issues & Solutions**:
  - **Hash Collision**: When two different inputs produce the same hash value. More likely with shorter hash algorithms like MD5 (128-bit). Collision-resistant algorithms like the SHA family (SHA-224, SHA-256, etc.) produce longer, safer hashes.
  - **Rainbow Tables**: Precomputed tables of hashes and their corresponding plaintext used to crack passwords.
  - **Salting**: Adding a unique, random string to data (like passwords) before hashing. This makes rainbow table attacks ineffective as even identical passwords will have different salted hashes.

### Identity and Access Management (IAM)

- **IAM & AAA Framework**: IAM encompasses processes and technologies for managing digital identities. Both IAM and the Authentication, Authorization, and Accounting (AAA) framework aim to ensure the right user accesses the right resources at the right time for the right reasons, implementing PoLP and Separation of Duties.
- **Authentication**: Verifying "Who are you?". Based on three factors:
  - **Knowledge**: Something you know (e.g., password, security question answer).
  - **Ownership**: Something you have (e.g., OTP device, phone for SMS code).
  - **Characteristic**: Something you are (e.g., fingerprint, facial scan - biometrics).
- **Authentication Technologies**:
  - **Single Sign-On (SSO)**: Combines multiple logins into one, improving user experience and security by reducing attack surfaces. Uses protocols like LDAP (on-prem) and SAML (cloud).
  - **Multi-Factor Authentication (MFA)**: Requires two or more independent authentication factors (e.g., password + OTP) to verify identity. Significantly strengthens security, often used with SSO.
- **Authorization**: Determining "What are you allowed to do?" after authentication. Heavily influenced by PoLP and Separation of Duties.
  - **Frameworks**: MAC (Mandatory - strict, central control), DAC (Discretionary - owner controls access), RBAC (Role-Based - access based on job function).
  - **Technologies**: Basic Auth (older, insecure HTTP method sending credentials openly), HTTPS (secure version), OAuth (standard protocol sharing designated access between apps using API tokens instead of passwords).
- **Accounting**: Monitoring and logging user activity ("What did you do?"). Access logs record session details (who, when, what resources used). Essential for detecting trends, investigating incidents, and identifying unauthorized access.
  - **Sessions**: A sequence of requests/responses from a user. Involve Session IDs (unique user/device token) and Session Cookies (server-issued token validating the session).
  - **Session Hijacking**: Attackers stealing a valid session ID/cookie to impersonate a legitimate user. Accounting helps detect this.
- **User Provisioning**: The process of creating, maintaining, and importantly, deprovisioning (removing) user digital identities and access rights.

## Vulnerabilities in Systems

### Foundational Concepts: Vulnerabilities, Exposures, and Exploits

- **Vulnerability**: A weakness in an asset or system that can potentially be exploited by a threat. Think of it as an inherent flaw.
- **Exposure**: A mistake that creates an opportunity for a threat to exploit a vulnerability. For example, leaving sensitive data unprotected is an exposure.
- **Exploit**: The specific method or action taken to leverage a vulnerability. An exploit turns a potential weakness into an actual security incident.
- **Zero-Day Exploit**: An exploit targeting a vulnerability that was previously unknown, meaning there were "zero days" to prepare a defense or patch.

### Vulnerability Management

- **Definition**: The ongoing process of identifying, evaluating, treating (patching), and reporting on security vulnerabilities in systems and software.
- **Cyclical Process**: It typically involves four key steps performed regularly:
  1. **Identify**: Discovering vulnerabilities through assessments and scanning.
  2. **Analyze/Consider Exploits**: Understanding the potential impact and how vulnerabilities could be exploited.
  3. **Remediate/Prepare Defenses**: Taking action to fix vulnerabilities (e.g., patching, configuration changes).
  4. **Evaluate Defenses**: Assessing the effectiveness of the implemented controls and restarting the cycle.

### Key Resources for Vulnerability Information

- **CVE (Common Vulnerabilities and Exposures)**: A publicly accessible dictionary listing known vulnerabilities and exposures, maintained by MITRE. Each entry gets a unique CVE ID after verification by a CVE Numbering Authority (CNA).
- **CVSS (Common Vulnerability Scoring System)**: A standardized system used (often by NIST's NVD) to rate the severity of vulnerabilities, typically on a scale of 0-10. This helps prioritize remediation efforts.
- **OWASP (Open Worldwide Application Security Project)**: A non-profit foundation focused on improving software security. Their OWASP Top 10 list highlights the most critical web application security risks, influencing secure development practices. Common examples include Injection, Broken Access Control, and Cryptographic Failures.
- **OSINT (Open-Source Intelligence)**: Gathering and analyzing publicly available information to generate actionable intelligence about threats and vulnerabilities. Tools like VirusTotal and MITRE ATT&CK® can assist.

### Defense Strategies and Assessment Methods

- **Defense in Depth (Castle Approach)**: A strategy using multiple layers of security controls to protect assets. If one layer fails, another is in place. Common layers include:
  - Perimeter (e.g., authentication)
  - Network (e.g., firewalls)
  - Endpoint (e.g., antivirus on devices)
  - Application (e.g., MFA)
  - Data (e.g., encryption, classification)
- **Vulnerability Assessment**: An internal review process to identify, analyze, score (risk assessment), and remediate security weaknesses within an organization's systems.
- **Vulnerability Scanning**: Using automated tools (vulnerability scanners) to compare system configurations and software against databases of known vulnerabilities. Scans can be:
  - External (testing perimeter defenses) vs. Internal (testing systems inside the network).
  - Unauthenticated (simulating an outside attacker) vs. Authenticated (simulating an attacker with user/admin credentials).
  - Comprehensive (all devices) vs. Limited (specific devices/areas).
- **Penetration Testing (Pen Testing)**: A simulated attack to actively exploit vulnerabilities and test the effectiveness of defenses. It's a form of ethical hacking and can use different strategies based on the tester's knowledge (e.g., white-box/open-box, black-box/closed-box, gray-box). Red teams simulate attackers, blue teams focus on defense/response, and purple teams combine both.
- **Security Hardening**: The process of strengthening systems by reducing vulnerabilities and minimizing the attack surface, often by implementing security controls and configurations.

### Attack Surface and Attack Vectors

- **Attack Surface**: The sum of all potential entry points or vulnerabilities that a threat actor could possibly exploit. It includes both physical (people, devices) and digital (network connections, software, cloud services) elements. Cloud computing has significantly expanded the digital attack surface.
- **Attack Vector**: The specific pathway or method an attacker uses to penetrate defenses and exploit a vulnerability. Examples include email, removable media, social media, weak credentials, unpatched software, and compromised supply chains.

### Understanding Threats

- **Threat Actor**: Any entity (person or group) that poses a security risk, intentionally or accidentally. Categories include competitors, state actors, criminal syndicates, insider threats, and shadow IT.
- **Hacker Types**: Categorized by intent:
  - **Unauthorized/Malicious (Black Hat)**: Illegally exploit systems.
  - **Authorized/Ethical (White Hat)**: Test systems legally to improve security (e.g., pen testers).
  - **Semi-Authorized (Gray Hat)**: May violate standards but without malicious intent (e.g., hacktivists).
- **Advanced Persistent Threat (APT)**: A sophisticated, often state-sponsored, threat actor that maintains stealthy, long-term unauthorized access to a target's systems, usually for espionage or strategic disruption.
- **Brute Force Attacks**: A trial-and-error method used to guess credentials or cryptographic keys. Tactics include simple guessing, dictionary attacks (using common word lists), reverse brute force (trying one password against many accounts), and credential stuffing (using credentials stolen from other breaches). Defenses include strong password policies, MFA, CAPTCHA, and account lockouts.

### Attacker Mindset

- **Concept**: Thinking like an adversary to anticipate threats, identify weaknesses, and understand how systems might be exploited.
- **Application**: Used in vulnerability assessments, penetration testing, and threat modeling to proactively identify and address security gaps before real attackers do. It involves challenging assumptions and considering how features could be misused.

### Importance of Updates and Patching

- **Purpose**: Updates fix bugs, improve performance, and crucially, address security vulnerabilities.
- **Patching**: Applying updates specifically designed to fix security flaws. This is a critical part of remediation in vulnerability management.
- **Strategies**: Updates can be manual (controlled deployment) or automatic (ensures timeliness but risks untested patches causing issues). CISA generally recommends automatic updates.
- **End-of-Life (EOL) Software**: Software no longer supported by the vendor poses significant risks as it receives no security patches.

## Threats to Asset Security

### Social Engineering

Social engineering is a manipulation technique exploiting human error to gain private information, access, or valuables, often tricking people into breaking security procedures. It preys on natural feelings like curiosity and generosity. Attacks can be quick (like impersonating tech support) or take months (like monitoring social media).

- **Stages**:
  - **Preparation**: Gathering information about the target.
  - **Pretexting (Establishing Trust)**: Using gathered information to open communication, often in disguise.
  - **Persuasion**: Manipulating the target into volunteering information.
  - **Disconnection**: Breaking communication after obtaining the desired information.
- **Common Tactics**:
  - **Baiting**: Tempting people into compromising security (e.g., infected USB drives).
  - **Phishing**: Using digital communications (mainly email) to trick people into revealing sensitive data or deploying malware.
  - **Quid Pro Quo**: A form of baiting promising a reward for sharing information or access.
  - **Tailgating/Piggybacking**: Unauthorized individuals following authorized personnel into restricted areas.
  - **Watering Hole**: Compromising a website frequently visited by a specific group, often infecting it with malware.
- **Prevention**:
  - Managerial controls (policies, standards like NIST SP 800-40 for patch management).
  - Staying informed and sharing knowledge about attack signs.
  - User awareness training: staying alert to suspicious communications, being cautious about sharing information (especially on social media), and controlling curiosity.
  - Technological controls: firewalls, MFA, block lists, email filtering.

### Phishing

Phishing is a prevalent social engineering technique using digital communications (email, text, voice) to deceive users. Attackers often use phishing kits containing tools like malicious attachments, fake data-collection forms, and fraudulent web links.

- **Types**:
  - **Email Phishing**: The most common form, using emails pretending to be from trusted entities. Mass phishing targets large numbers of people.
  - **Smishing**: Phishing via SMS/text messages.
  - **Vishing**: Phishing via voice calls or messages.
  - **Spear Phishing**: Targeted email phishing aimed at specific individuals or groups.
  - **Whaling**: Spear phishing specifically targeting high-ranking executives.
  - **Angler Phishing**: Impersonating customer service representatives on social media.
- **Prevention**:
  - Anti-phishing policies and employee training.
  - Email security: filters, blocklists, allowlists.
  - Intrusion Prevention Systems (IPS) to monitor email traffic for unusual patterns.

### Malware (Malicious Software)

Malware is software designed to harm devices or networks, often spread via infected media or online. It interferes with normal operations and allows attackers unauthorized control.

- **Types**:
  - **Virus**: Malicious code interfering with operations, damaging data/software. Requires user activation to spread by cloning itself into other files/programs.
  - **Worm**: Malware that duplicates and spreads itself across systems without user action, using the infected device as a host to scan and infect the network.
  - **Trojan (Trojan Horse)**: Malware disguised as a legitimate file or program to trick users into installing it. Often used to gain access and install other malware like ransomware.
  - **Ransomware**: Encrypts an organization's data and demands payment for restoration. Makes itself known to collect payment.
  - **Spyware**: Gathers and sells information (credentials, PINs) without consent. Often considered a Potentially Unwanted Application (PUA).
  - **Adware**: Displays digital ads. Malicious adware can be a PUA hidden in freeware, monetizing ads for the attacker.
  - **Scareware**: Uses tactics (fake warnings) to frighten users into infecting their own devices. Also a type of PUA.
  - **Fileless Malware**: Uses legitimate, pre-installed programs to infect a computer, residing in memory without writing to the hard drive. Detected via memory analysis.
  - **Rootkit**: Provides remote, administrative access (backdoor) to install other malware or conduct attacks. Often spread using a dropper (delivers/installs payload) and/or a loader (downloads/installs payload from external source).
  - **Botnet**: A network of malware-infected computers ("bots") controlled by a single "bot-herder". Infections often spread via viruses, worms, trojans.
  - **Cryptojacking**: Installs software to illegally use the victim's computing resources to mine cryptocurrencies. Signs include system slowdown, increased CPU usage, crashes, high electricity costs.
- **Detection & Prevention**:
  - Intrusion Detection Systems (IDS) monitor activity and alert on intrusions.
  - Recognizing signs of infection (slowdown, crashes, high resource usage).
  - Defenses: browser extensions to block malware, ad blockers, disabling JavaScript, staying alert.
  - Educating users within organizations.

### Web-Based Exploits

These use malicious code/behavior to take advantage of coding flaws in web applications, often to obtain sensitive information. Injection attacks, inserting malicious code into vulnerable applications, are common.

- **Cross-Site Scripting (XSS)**: Injects malicious code (often HTML/JavaScript) into vulnerable websites/apps. Can access session cookies, geolocation, webcams.
  - **Reflected XSS**: Malicious script sent to the server (e.g., via a crafted link) and activated in the server's response back to the user's browser.
  - **Stored XSS**: Malicious script injected directly onto the server (e.g., in site elements like images/buttons) and activated when any user visits the site.
  - **DOM-based XSS**: Malicious script exists within the web page loaded by the browser (often visible in the URL parameters), doesn't need server round-trip to activate.
- **SQL Injection (SQLi)**: Executes unexpected SQL queries on a database, often via unsanitized user input fields (like login forms). Can steal/modify/delete data or gain admin rights.
  - **In-band (Classic)**: Uses the same channel for attack and results (e.g., results displayed in a vulnerable search box).
  - **Out-of-band**: Uses different channels for attack and results (e.g., creates a separate connection to attacker-controlled database). Uncommon.
  - **Inferential (Blind)**: Attacker infers database structure/data by analyzing system behavior/responses (like error messages) rather than seeing direct results.
- **Prevention (Injection Attacks)**:
  - **Input Sanitization**: Removing user input that could be interpreted as code.
  - **Input Validation**: Ensuring user input meets expected format/criteria.
  - **Prepared Statements (for SQLi)**: Coding technique executing SQL structure separately from user parameters, validating before querying the database.
  - Escaping user inputs.

### Threat Modeling

Threat modeling is a proactive security process to identify assets, their vulnerabilities, and how threats expose them. It applies to systems, applications, or processes. It's often performed by experienced teams but involves collaboration.

- **General Steps**:
  - **Define Scope**: Inventory and classify assets.
  - **Identify Threats**: Define potential threat actors (internal/external) and map threats to assets using attack trees.
  - **Characterize Environment**: Apply attacker mindset; consider user interactions, partners, vendors.
  - **Analyze Threats**: Examine existing protections, identify gaps, rank threats by risk.
  - **Mitigate Risk**: Plan defenses (avoid, transfer, reduce, or accept risk).
  - **Evaluate Findings**: Document exercise, apply fixes, note successes and lessons learned.
- **Common Frameworks**:
  - **STRIDE (Microsoft)**: Identifies vulnerabilities in 6 categories: Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege.
  - **PASTA (Process for Attack Simulation and Threat Analysis)**: Risk-centric, evidence-based 7-stage process focusing on viable threats. Stages include defining objectives, technical scope, decomposing application, threat analysis, vulnerability analysis, attack modeling, and risk/impact analysis.
  - **Trike**: Open-source, security-centric methodology focusing on permissions, use cases, privilege models.
  - **VAST (Visual, Agile, Simple Threat)**: Part of the automated ThreatModeler® platform.
- **Importance**: Essential for application security (DevSecOps) to find weaknesses proactively, especially given the volume of data handled by modern web and mobile apps. Should be incorporated throughout the Software Development Lifecycle (SDLC). Effective threat modeling involves asking key questions about the system, potential issues, mitigation, and evaluation.
