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

# Module 3 - Communicate Effectively to Influence Stakeholders

## Understanding Stakeholders in Cybersecurity

A **stakeholder** is an individual or group with an interest in an organization's decisions or activities. The decisions made by stakeholders directly impact the daily work of security analysts. Security threats, risks, and vulnerabilities can affect an entire company, leading to financial implications, loss of customer data, and diminished trust. Therefore, each stakeholder has a responsibility to provide input on the security team's decisions and activities to best protect the organization.

Key stakeholders with a significant interest in security include:

* **Risk Managers:** Identify risks, manage responses to security incidents, notify the legal department about regulatory issues, and inform the public relations team about potential public communications regarding an incident.
* **Chief Executive Officer (CEO):** The highest-ranking person, responsible for overall financial and managerial decisions, reporting to shareholders, and managing company operations. Security is a top priority for the CEO.
* **Chief Financial Officer (CFO):** A senior executive managing the company's financial operations. Concerned with the potential financial costs of incidents and the costs of tools and strategies to combat them.
* **Chief Information Security Officer (CISO):** A high-level executive responsible for developing the organization's security architecture, conducting risk analysis and system audits, and creating security and business continuity plans. This is the highest level of security stakeholder.
* **Operations Managers:** Oversee security professionals to identify and safeguard the organization from threats. They often work directly with analysts as the first line of defense and are generally responsible for daily security operations maintenance.

Entry-level analysts are unlikely to communicate directly with high-level stakeholders like the CEO, CFO, or CISO. However, operations managers will likely request analysts to create communications to share with these individuals. Operations managers and risk managers rely on entry-level analysts to keep them informed of daily security events. These managers, in turn, report to senior stakeholders like CISOs and CFOs, providing a broader view of the organization's security posture.

## Effective Communication with Stakeholders

Communicating with stakeholders requires clarity, conciseness, and focus, especially as the information shared is often sensitive. Avoid unnecessary technical terms and ensure communications have a clear purpose, so stakeholders don't have to guess the reason for the communication or its relevance to them.

**Key Principles for Communication:**

* **Understand Stakeholder Needs:** Ask managers or supervisors what specific information stakeholders require. A security mindset involves understanding what matters most to stakeholders.
* **Relevance:** Relay only the most relevant information. This helps stakeholders stay informed and perform their jobs effectively.
* **"Security Storytelling":** Frame communications like a story with a beginning (the security challenge), middle (its impact on the organization), and end (possible solutions). Include supporting data, such as reports summarizing key findings or lists of issues needing immediate attention.
    * **Example Scenario:** If malicious code execution is found in logs, the communication to a supervisor (stakeholder) should detail the issue, reference the organization's incident response playbook for guidance, and suggest a possible solution.
* **Follow Protocols:** Learn and adhere to the organization's established protocols and procedures for communicating with stakeholders, including acceptable applications and forms of communication (e.g., in-person meetings, email, company chat).

**To ensure clear and concise communication, ask yourself:**
* What do I want this person to know?
* Why is it important for them to know it?
* When do they need to take action?
* How do I explain the situation in a nontechnical manner?

## Communication Methods

The method of communication will vary depending on the type of information being shared and the stakeholder's focus. Lower-level stakeholders (e.g., operations managers) are often interested in day-to-day operations like log anomalies, while senior-level stakeholders (e.g., CFOs) might be more focused on underlying risks like potential financial burdens.

* **Instant Messaging/Phone Calls:** Suitable for straightforward messages or when a quick response is needed, especially if emails go unanswered for issues requiring immediate attention. Following up on an unread email with a call shows initiative.
* **Email/Documents:** Better for complex situations with multiple layers or when a detailed report is necessary (e.g., explaining an incident, what worked, what needs revision, and suggestions for improvement). Always ensure emails are sent to the correct recipient to avoid risking confidential information.
* **Visual Dashboards (Charts, Graphs, Infographics):** Highly effective for conveying key details and impactful data/metrics, especially involving numbers. They help stakeholders quickly grasp the information and make informed decisions. Visuals can compare data points or show parts of a larger issue.
    * A **visual dashboard** displays various data types quickly in one place. It can be simple (a single chart) or complex (multiple charts, graphs, tables). Tools like Google Sheets or Apache OpenOffice can be used to create them.
    * **When to use visuals:** Ideal for presenting audit results, such as the number of phishing emails clicked by different departments over time. A graph or chart can illustrate findings more clearly and quickly than a descriptive email.

Communicating effectively by tailoring the message and method to the stakeholder's needs and interests makes everyone's job easier and helps showcase both technical and transferable skills.

# Module 4: Engage with the Cybersecurity Community

This module emphasizes the importance of continuous learning and community engagement for cybersecurity professionals. The field is constantly evolving, so staying updated on the latest security trends, threats, risks, vulnerabilities, and tools is crucial.

### I. Staying Updated in Cybersecurity

* **Constant Evolution**: The cybersecurity landscape is dynamic. For instance, the OWASP Top 10, a list of critical security risks to web applications, is updated every three to four years, highlighting the evolving nature of threats.
* **Importance of Continuous Learning**: Continuing education beyond formal programs demonstrates a commitment to staying current and can provide a competitive edge in the job market. This includes keeping up with industry news, new breach analyses, and malware developments.

### II. Reliable Resources for Security News & Trends

To stay informed, professionals should periodically review reputable security websites, blogs, and mailing lists.

* **Key Websites and Blogs**:
    * **CSO Online**: Provides news, analysis, and research on security and risk management topics, often used by Chief Security Officers (CSOs).
    * **Krebs on Security**: An in-depth security blog by Brian Krebs, covering security news and investigations into cyber-attacks.
    * **Dark Reading**: A popular site for security professionals, offering information on diverse topics like analytics, application security, mobile/cloud security, and IoT.
* **Mailing Lists**:
    * **Cybersecurity & Infrastructure Security Agency (CISA)** offers valuable mailing lists:
        * One focused on security threat information, cybersecurity best practices, and partner analyses.
        * Another providing weekly summaries of new vulnerabilities.

### III. Engaging with the Cybersecurity Community

Actively participating in the cybersecurity community offers opportunities for knowledge gain, networking, and career advancement.

* **Security Organizations and Conferences**:
    * **Benefits**: Gain knowledge from seasoned professionals and learn about new strategies and techniques.
    * **Finding the Right Fit**: Identify your specific interests within security (e.g., incident response, forensics, GRC) before searching for relevant organizations or conferences. Use web searches like "incident response cybersecurity conferences in my area" or "forensic security organizations in my area".
    * **Examples**:
        * **BSides Conferences**: Smaller, locally organized, and often informal conferences that offer good opportunities to interact with the local security community. Many also have virtual components.
        * **Women in Cybersecurity (WiCyS)**: A community helpful for networking and support, offering webinars, forums, and conferences.
* **Using Social Media (e.g., LinkedIn®)**:
    * **Connecting with Professionals**:
        * Follow leaders like Chief Information Security Officers (CISOs) who often share insights, interviews, and articles. LinkedIn® is the preferred platform for this.
        * Connect with other security analysts and professionals. When sending connection requests, include a brief, clear message explaining your intent.
        * Find security groups or organizations to join.
    * **Caution**: Be mindful of social engineering tactics. Do not click on unexpected links or attachments from unfamiliar users.
* **Joining Security Associations**: Research and join associations that align with your professional goals. An internet search for "cybersecurity industry associations" can be a good starting point.

### IV. Establishing and Advancing a Career in Security

Engagement with the community plays a direct role in career development.

* **Networking**:
    * Meeting peers and potential employers is crucial.
    * Connecting with peers from certificate programs can provide motivation and support.
* **Diverse Backgrounds are Valuable**: The cybersecurity field benefits from diverse perspectives. Individuals from non-traditional backgrounds (e.g., biology, non-computer science degrees) can bring unique value and should not be discouraged.
* **It's Okay Not to Know Everything**: The field is vast, and no one knows everything. Teamwork and continuous learning are key.

### Key Takeaways for Community Engagement:

* **Be Proactive**: Seek out information, connections, and opportunities.
* **Be Purposeful**: Align your engagement activities with your interests and career goals.
* **Be Cautious**: Protect yourself from online threats, even while networking.
* **Be Open**: Embrace continuous learning and diverse perspectives.

This dynamic field offers many opportunities for those willing to learn and engage.
