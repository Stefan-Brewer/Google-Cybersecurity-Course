# Course 8: Put It to Work: Prepare for Cybersecurity Jobs

# Module 1: Protect Data and Communicate Incidents

## Core Concepts

### The Security Mindset
A **security mindset** is the ability to continuously evaluate risk and identify potential or actual breaches of systems, applications, or data. It involves understanding what assets need defending and who or what they are being defended against. This mindset helps in recognizing essential assets for an organization's business functions and the threats, risks, and vulnerabilities that could impact them. Staying updated on the latest security threats and vulnerabilities is crucial for maintaining this mindset. Such a proactive approach prepares security professionals for worst-case scenarios and is vital for protecting all levels of assets, from guest Wi-Fi networks to intellectual property and PII.

### Asset and Data Classification
Protecting an organization's assets and data is paramount. Classification helps prioritize protection efforts.

* **Data Classification Types**:
    * **Public Data**: Accessible to the public; minimal risk if exposed (e.g., press releases, job descriptions). Basic security measures are still needed.
    * **Private Data**: Not for public disclosure; unauthorized access poses a serious risk (e.g., company email addresses, employee IDs, research data).
    * **Sensitive Data**: Requires protection from unauthorized access; exposure can cause significant financial and reputational damage (e.g., PII, SPII, PHI like bank account numbers, passwords, Social Security numbers, medical information).
    * **Confidential Data**: Crucial for ongoing business operations, with access often restricted and potentially requiring NDAs (e.g., trade secrets, financial records, sensitive government data).

* **Asset Classification**:
    * Assets are labeled based on sensitivity and importance.
    * **Low-Level Assets**: Public data is an example; its compromise has minimal negative impact (e.g., company website address).
    * **High-Level Assets**: Sensitive and confidential data fall here; public leakage can severely impact competitive edge, reputation, and customer trust (e.g., internal email discussing trade secrets).
    * Organizations have their own data classification policies that security professionals must understand.

### Incident Detection and Response
* **Events vs. Incidents**: A security event that results in a data breach is categorized as a **security incident**. If an event is resolved without a breach, it's not an incident.
* **Importance of Reporting**: All potential issues, regardless of perceived size, should be reported or escalated. For instance, an employee installing an unapproved app should be escalated due to potential vulnerabilities. Malicious code in logs is a more significant issue requiring escalation.
* **Impact of Breaches**: Compromised data and assets can lead to financial losses, regulatory fines, and loss of credibility. Protecting customer data (credit card numbers, PII, etc.) is a primary concern.

## Key Processes and Plans

### Escalation
The process of escalating incidents is crucial for an organization's security posture. Incidents need to be escalated to stakeholders to protect assets and data. It's always best to be cautious and report events to appropriate team members if unsure of the potential impact.

### Business Continuity and Disaster Recovery
It's vital to have plans to minimize the impact of security incidents and ensure business operations can continue or recover.

* **Four-Part Security Process**:
    1.  Identify assets requiring protection.
    2.  Determine potential threats to those assets.
    3.  Implement tools and processes to detect potential threats.
    4.  Create Business Continuity and Disaster Recovery plans.

* **Business Continuity Plan (BCP)**: A document outlining procedures to sustain business operations during and after a significant disruption.
    * **Essential Steps for BCPs**:
        1.  **Conduct a business impact analysis (BIA)**: Assess potential effects of business function disruptions.
        2.  **Identify, document, and implement recovery steps**: For critical business functions and processes.
        3.  **Organize a business continuity team**: Comprising members from cybersecurity, IT, HR, communications, and operations.
        4.  **Conduct training**: For the BCP team, covering various risk scenarios.

* **Disaster Recovery Plan (DRP)**: Outlines steps to minimize the impact of a security incident (e.g., ransomware attack) and resolve the threat.
    * **Steps should include**:
        * Implementing recovery strategies for software and hardware functionality.
        * Identifying applications and data potentially impacted post-incident.

### Information Lifecycle Strategy
This strategy helps ensure assets are protected effectively.
* **Steps in the Information Lifecycle**:
    1.  **Identify important assets**: Including sensitive customer information (PII, financial data, etc.).
    2.  **Assess security measures**: Review existing protections and information security policies (can include vulnerability scanning, process reviews).
    3.  **Protect identified assets**: Implement security controls and measures.
    4.  **Monitor security processes**: Continuously observe implemented protections.

## The Role of the Security Analyst
Security analysts play a vital role in protecting an organization's tangible (software, hardware) and intangible (PII, copyrights, intellectual property) assets. Their work is crucial because a data exposure can be devastating to an organization's reputation and financial stability. Collaboration is key, as security involves many individuals across an organization focusing on different aspects like financial data, PII, or third-party vendor security. Every decision made affects the company, its customers, and team members. An ethical security mindset is essential for protecting secured assets and data.

Understanding the value of their role helps analysts put their work into perspective, as every individual contributes to the smooth flow of company operations.

# Module 2 - Escalate Incidents

## The Importance of Escalation

Protecting an organization's data and assets is the primary goal of a security team. Recognizing when and how to escalate security incidents is crucial to prevent simple issues from becoming larger problems. Incident escalation is the process of identifying a potential security incident, triaging it, and, if appropriate, handing it off to a more experienced team member. Not every incident requires escalation.

As an entry-level analyst, you play an important role in identifying issues and alerting the correct personnel. Failure to escalate a seemingly minor incident in a timely manner can lead to significant consequences, including financial loss, exposure of sensitive customer data, or damage to the company's reputation.

Two essential skills for identifying incidents that need escalation are:
* **Attention to detail:** This helps in quickly identifying anomalies within the organization's network or systems.
* **Ability to follow escalation guidelines:** Adherence to the company's specific processes ensures proper handling of identified issues.

Security teams vary in size; larger organizations have multi-level teams (including CISO, engineering, public relations, and legal teams), while smaller companies might have only one or two individuals responsible for security. The roles and responsibilities within the escalation process depend on the nature and scope of the incident, as outlined in the company's escalation process.

## Notification of Breaches

Many countries have breach notification laws requiring companies and government entities to inform individuals of security breaches involving Personally Identifiable Information (PII). PII includes items like Social Security numbers, driver's license numbers, medical records, and addresses. Security analysts must be aware of applicable security laws, which are regularly updated.

## Low-Level Security Issues

Low-level security issues are risks that do not immediately result in PII exposure. Examples include an employee having a single failed login attempt or downloading unapproved software. While not significant threats on their own, they must be investigated as they could be indicators of a larger problem (e.g., multiple failed login attempts could signify a malicious actor trying to compromise an account, or downloaded software could contain malware). Malware can lead to financial loss and reputational damage.

## The Escalation Process

Every company has unique escalation policies and procedures. These policies detail who to notify when a security alert is received, who to contact if the primary responder is unavailable, and the specific methods for escalation (e.g., IT help desk, incident management tool, direct communication). It is crucial for security analysts to be familiar with their organization's specific escalation protocols. Both small and large security issues should be escalated appropriately.

## Incident Classification Types

Understanding different incident types helps in proper escalation:

* **Malware Infection:** Occurs when malicious software (e.g., phishing, ransomware) infiltrates an organization's computers or network. This can cause system slowdowns or block access to critical data. Due to the sensitive data stored on networks, escalating malware infections is crucial.
* **Unauthorized Access:** Happens when an individual gains digital or physical access to a system, application, or data without permission (e.g., through brute force attacks). The urgency of escalating unauthorized access depends on the criticality of the affected system to business operations.
* **Improper Usage:** Occurs when an employee violates the organization's acceptable use policies. This can be unintentional (e.g., accessing software licenses for personal use, not being aware of a policy) or intentional. Distinguishing between accidental and intentional improper usage can be difficult, so these incidents should always be escalated to a supervisor.

## Roles and Responsibilities in Escalation

Understanding the roles within the escalation process is important, though terminology may vary between organizations:

* **Data Owners:** Decide who can access, edit, use, or destroy their specific information, hardware, or software. They are accountable for data classification, protection, access, and use. Incidents like unauthorized access to software would be escalated to the data owner.
* **Data Controllers:** Determine the procedure and purpose for processing data, particularly customer PII. They ensure data is used, stored, and processed according to security and privacy regulations. Events risking sensitive customer information are escalated to data controllers.
* **Data Processors:** Report to data controllers and are responsible for processing data on their behalf, often a vendor tasked with installing security measures. Data processing issues are typically escalated to the individual overseeing this third-party organization.
* **Data Custodians:** Assign and remove access to software or hardware. They implement security controls, grant/revoke access, create data storage/transmission policies, advise on threats, and monitor data. They are notified when data security controls need strengthening or are compromised.
* **Data Protection Officers (DPOs):** Monitor internal compliance with data protection procedures. They advise the security team on obligations required by data protection standards and conduct assessments to ensure security measures are adequate. DPOs are notified when standards or protocols are violated.

Entry-level analysts typically escalate incidents to their direct supervisor but should understand these broader roles.

## Impact of Unescalated Incidents & Incident Criticality

Even a seemingly small incident, if unescalated, can lead to significant problems like a data breach, operational halts, financial loss, and reputational damage.

**Incident criticality** is key. An incident's initial criticality level might be set to medium if the analyst lacks enough information. An experienced incident handler can then adjust this to high or low. The urgency of a security incident depends heavily on the asset(s) it affects.
* Low-impact incidents (e.g., an employee with repeated failed login attempts due to a forgotten password) need addressing but are likely minimal in impact.
* High-impact incidents involve assets critical to business operations (e.g., a manufacturing plant's application, a database storing PII). Unauthorized access to these can cause severe disruption or data exposure and requires urgent escalation.

## When and How to Escalate

The specific steps for escalation depend on the organization's **escalation policy**. This policy outlines who to notify and how to handle incidents. It's crucial to:
* Have access to and understand your organization's escalation policy (e.g., save or bookmark it).
* Pay attention to detail within the policy to ensure correct escalation and prioritization.

Challenges can occur, such as an immediate supervisor being unavailable. The escalation policy should cover such contingencies.

## Escalation Timing and Analyst's Role

Security is a fast-paced environment. Entry-level analysts are crucial for escalating potential security events before they become major incidents.
* **Trust your instincts and ask questions:** Confidence in decision-making is important, built by understanding the escalation policy. Don't hesitate to ask questions to ensure correct procedures.
* **Recognize asset importance:** Understand which assets and data are most critical to your organization (via onboarding materials, supervisor discussions, security policies). This helps prioritize incidents. Incidents directly impacting essential business operations always take priority.
* **Quick Escalation Tips:**
    * Familiarize yourself with the organization's escalation policy.
    * Follow the policy at all times.
    * Ask questions when in doubt.

Your attention to detail and understanding of how incidents affect data and assets are vital, as your decisions impact the entire security team and organization.
