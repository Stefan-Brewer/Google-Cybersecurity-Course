# Consolidated Cybersecurity Study Notes

## Core Cybersecurity Concepts

### The Security Mindset
A security mindset involves continuously evaluating risks and identifying potential or actual breaches of systems, applications, or data. It requires understanding what assets need protection and from whom or what. This mindset helps in recognizing essential organizational assets and the threats, risks, and vulnerabilities that could affect them. Staying updated on the latest security threats and vulnerabilities is crucial. This proactive approach is vital for protecting all assets, from guest Wi-Fi networks to intellectual property and Personally Identifiable Information (PII).

### Asset and Data Classification
Protecting an organization's assets and data is crucial. Classification helps prioritize these protection efforts.

* **Data Classification Types**:
    * **Public Data**: Information accessible to the public, with minimal risk if exposed (e.g., press releases, job descriptions). Basic security measures are still necessary.
    * **Private Data**: Information not intended for public disclosure, where unauthorized access poses a serious risk (e.g., company email addresses, employee IDs, research data).
    * **Sensitive Data**: Information requiring robust protection from unauthorized access, as exposure can cause significant financial and reputational damage (e.g., PII, SPII, PHI like bank account numbers, passwords, Social Security numbers, medical information).
    * **Confidential Data**: Information crucial for ongoing business operations, often with restricted access and potentially requiring Non-Disclosure Agreements (NDAs) (e.g., trade secrets, financial records, sensitive government data).

* **Asset Classification**:
    * Assets are labeled based on their sensitivity and importance.
    * **Low-Level Assets**: Include public data; their compromise results in minimal negative impact (e.g., company website address).
    * **High-Level Assets**: Encompass sensitive and confidential data; public leakage can severely impact competitive advantage, reputation, and customer trust (e.g., internal emails discussing trade secrets).
    * Organizations establish their own data classification policies that security professionals must understand.

### Incident Detection, Response, and Escalation
* **Events vs. Incidents**: A security event that results in a data breach is classified as a **security incident**. If an event is resolved without a breach, it is not considered an incident.
* **Importance of Reporting and Escalation**: All potential issues, regardless of their perceived significance, should be reported or escalated. For instance, an employee installing an unapproved application should be escalated due to potential vulnerabilities. Malicious code in logs represents a more significant issue requiring escalation. Escalation is the process of identifying a potential security incident, triaging it, and, if appropriate, handing it off to a more experienced team member. Not every incident requires escalation. Failure to escalate appropriately can lead to significant consequences.
* **Impact of Breaches**: Compromised data and assets can lead to financial losses, regulatory fines, and a loss of credibility. Protecting customer data (e.g., credit card numbers, PII) is a primary concern.
* **Escalation Policies**: Every company has unique escalation policies detailing who to notify, contact persons if primary responders are unavailable, and specific escalation methods (e.g., IT help desk, incident management tool, direct communication). Analysts must be familiar with these protocols.
* **Incident Criticality**: The urgency of a security incident depends heavily on the asset(s) it affects. Low-impact incidents (e.g., an employee with repeated failed login attempts due to a forgotten password) need addressing but are likely minimal in impact. High-impact incidents involve assets critical to business operations (e.g., a manufacturing plant's application, a database storing PII).
* **Analyst's Role in Escalation**: Entry-level analysts are crucial for escalating potential security events. They need attention to detail and the ability to follow escalation guidelines. Trusting instincts, asking questions, and understanding asset importance are key.

### Key Processes and Plans

* **Four-Part Security Process**:
    1.  Identify assets requiring protection.
    2.  Determine potential threats to those assets.
    3.  Implement tools and processes to detect potential threats.
    4.  Create Business Continuity and Disaster Recovery plans.

* **Business Continuity Plan (BCP)**: A document outlining procedures to sustain business operations during and after a significant disruption.
    * **Essential Steps for BCPs**:
        1.  Conduct a business impact analysis (BIA).
        2.  Identify, document, and implement recovery steps for critical functions.
        3.  Organize a business continuity team (cybersecurity, IT, HR, communications, operations).
        4.  Conduct training for the BCP team.

* **Disaster Recovery Plan (DRP)**: Outlines steps to minimize the impact of a security incident and resolve the threat.
    * **Steps should include**: Implementing recovery strategies for software and hardware, and identifying potentially impacted applications and data.

* **Information Lifecycle Strategy**:
    1.  Identify important assets.
    2.  Assess existing security measures and policies.
    3.  Protect identified assets by implementing security controls.
    4.  Monitor security processes continuously.

### Notification of Breaches
Many jurisdictions have breach notification laws requiring companies and government entities to inform individuals of security breaches involving PII (e.g., Social Security numbers, driver's license numbers, medical records, addresses). Security analysts must stay informed about applicable, regularly updated security laws.

### Common Incident Types for Escalation

* **Malware Infection**: Malicious software (e.g., phishing, ransomware) infiltrates systems or networks.
* **Unauthorized Access**: An individual gains digital or physical access without permission (e.g., through brute force attacks).
* **Improper Usage**: An employee violates acceptable use policies, intentionally or unintentionally.

### Roles and Responsibilities in Escalation

* **Data Owners**: Accountable for data classification, protection, access, and use; decide who can access, edit, use, or destroy their specific information.
* **Data Controllers**: Determine the procedure and purpose for processing data, especially customer PII, ensuring compliance with regulations.
* **Data Processors**: Report to data controllers and process data on their behalf, often third-party vendors.
* **Data Custodians**: Assign and remove access to software or hardware, implement controls, grant/revoke access, create data policies, advise on threats, and monitor data.
* **Data Protection Officers (DPOs)**: Monitor internal compliance with data protection procedures, advise on obligations, and conduct assessments.

Entry-level analysts typically escalate to their direct supervisor but should understand these broader roles.

## Communicating Effectively with Stakeholders

### Understanding Stakeholders
A **stakeholder** is an individual or group with an interest in an organization's decisions or activities. Security threats affect the entire company, so stakeholder input is vital.

* **Key Stakeholders**:
    * **Risk Managers**: Identify risks, manage incident responses, notify legal and PR.
    * **Chief Executive Officer (CEO)**: Overall responsibility for company operations and security.
    * **Chief Financial Officer (CFO)**: Manages financial operations, concerned with incident costs.
    * **Chief Information Security Officer (CISO)**: Develops security architecture, conducts risk analysis, and creates security/BCP plans.
    * **Operations Managers**: Oversee security professionals, often the first line of defense and responsible for daily security operations.

Entry-level analysts usually communicate with operations managers, who then report to senior stakeholders.

### Principles for Effective Communication

* **Clarity, Conciseness, Focus**: Avoid jargon and ensure a clear purpose.
* **Understand Stakeholder Needs**: Tailor information to what stakeholders require.
* **Relevance**: Share only the most pertinent information.
* **"Security Storytelling"**: Frame communications with a beginning (challenge), middle (impact), and end (solutions), supported by data.
* **Follow Protocols**: Adhere to organizational communication procedures.
* **Self-Reflection for Clarity**: Ask yourself: What do they need to know? Why is it important? When do they need to act? How can I explain it non-technically?

### Communication Methods

* **Instant Messaging/Phone Calls**: For straightforward messages or urgent responses.
* **Email/Documents**: For complex situations requiring detailed reports. Ensure correct recipients.
* **Visual Dashboards (Charts, Graphs, Infographics)**: Effective for conveying key details and metrics quickly.

## Engaging with the Cybersecurity Community

### Importance of Continuous Learning
The cybersecurity landscape is constantly evolving (e.g., OWASP Top 10 updates). Continuous learning beyond formal education is crucial for staying current and competitive.

### Reliable Resources

* **Websites and Blogs**: CSO Online, Krebs on Security, Dark Reading.
* **Mailing Lists**: Cybersecurity & Infrastructure Security Agency (CISA) offers lists on threats, best practices, and vulnerability summaries.

### Community Engagement

* **Security Organizations and Conferences**: (e.g., BSides, Women in Cybersecurity - WiCyS). Offer knowledge sharing and networking. Identify your interests (e.g., incident response, forensics) to find relevant events.
* **Social Media (e.g., LinkedIn®)**: Connect with professionals and leaders (e.g., CISOs), join groups. Be cautious of social engineering.
* **Security Associations**: Join associations aligned with professional goals.

### Career Advancement Through Engagement

* **Networking**: Meeting peers and potential employers is vital.
* **Diverse Backgrounds**: The field benefits from varied perspectives; non-traditional backgrounds are valuable.
* **It's Okay Not to Know Everything**: Teamwork and continuous learning are key in this vast field.

## Finding and Applying for Cybersecurity Jobs

### Common Entry-Level Roles

* **Security Analyst**: Monitors networks, develops strategies, researches trends. Requires log monitoring and SIEM tool knowledge.
* **Information Security Analyst**: Creates plans and implements security measures. Knowledge of controls, frameworks (NIST CSF, CIA Triad), SIEMs, and packet sniffers is beneficial.
* **Security Operations Center (SOC) Analyst**: Handles incidents by following policies and playbooks.

### Job Search Strategies
Utilize job sites (ZipRecruiter, Indeed, Monster Jobs), LinkedIn for networking and research. Thoroughly research companies and roles.

### Defining Your Career Identity
Your unique value based on experiences, strengths, motivations, and values.
* **Components**: Strengths (what you do well and enjoy), Motivations (passions, purpose), Values (what's important).
* **Career Identity Statement**: A 3-4 sentence summary of qualifications, passions, and purpose. Incorporate into resume, LinkedIn, cover letters, and elevator pitch.

### Resume Creation

* **Key Sections**:
    * Name and Professional Title.
    * Contact Information.
    * Summary Statement (1-2 sentences, keywords from job description).
    * Skills Section (relevant technical and transferable skills).
    * Experience Section (work history, quantifiable accomplishments, action verbs).
    * Education and Certifications (most recent first).
* **Considerations**: No errors, typically two pages, tailored to the job.

### Cover Letter
Tells your story, explains your interest in cybersecurity and the specific role. Focus on passion, uniqueness, soft skills, and alignment with the company's mission.

### The Interview Process

* **Pre-screening Phone Call**: Short call to verify resume details.
* **In-person or Online Interview**: Panel or one-on-one.
    * **Preparation**: Review job description/resume, practice, dress professionally, prepare tech for online interviews.
* **Interview Components**:
    * **Background Interview**: About experience, skills, cultural fit.
    * **Technical Interview**: Specific technical questions. It's okay to admit not knowing and explain how you'd find an answer.
* **Post-Interview**: Send a thank-you email within 24 hours.
* **Perseverance**: If not hired, process emotions, thank them, ask for feedback.

### Preparing for Technical Interviews

* **Key Areas**: Python basics, general security concepts (frameworks like NIST CSF, network security, TCP/IP & OSI models, SIEM tools like Splunk, packet sniffers like Wireshark).
* **Tips**: Understand fundamentals, practice answering open-ended questions, ask clarifying questions, use STAR method, think aloud, be honest about knowledge gaps but emphasize learning ability.

### Pre-Interview Research
Research the organization's mission, vision, values, and culture. Identify how your values align and how you can meet their needs. Prepare questions to ask.

### Building Rapport
Establish a friendly relationship based on mutual understanding and good communication.
* **Initial Interactions**: Professional, polite, friendly tone.
* **During Interview**: Smile, active engagement, eye contact.
* **Asking Questions**: Shows engagement (e.g., "What is the biggest challenge I might face?", "What's the best part about working here?").
* **Follow-Up Email**: Brief thank-you, referencing a specific conversation point.

### Interview Question Strategies

* **STAR Method**: For behavioral/situational questions (Situation, Task, Action, Result).
* **Confident Answering**: Admit when you don't know, state eagerness to learn. Take a moment to think.

### Interview Practice
Use tools like Interview Warmup to practice various question types.

### Developing an Elevator Pitch
A brief (<=60 seconds) summary of experience, skills, and background. Be persuasive, genuine, and speak clearly.

### Tips for Remote Interviews

* **Test Technology**: Platform, camera, microphone. Have a backup plan.
* **Practice Video Communication**: Be mindful of delays.
* **Professional Background**: Well-lit, tidy, distraction-free.
* **Dress Appropriately**.
* **Look at the Interviewer (on screen)**.
* **Sign In Early**.

### Overcoming Imposter Syndrome
Feeling incompetent despite evidence otherwise.
* **Strategies**: Connect with others, find a mentor, recognize small wins, reflect on your journey, understand you don't need to know everything, stay flexible, ask questions.

## Introduction to AI in Cybersecurity

**Artificial Intelligence (AI)**: Computer programs performing cognitive tasks.
**Generative AI (Gen AI)**: Creates new content (text, images). Interact via **prompts**.

### Applications in Cybersecurity

* Create content (e.g., fake test data).
* Analyze information quickly (e.g., summarize reports).
* Answer detailed questions.
* Simplify tasks (e.g., initial analysis of malicious emails).

### Prompting Framework (T-C-R-E-I)
Task, Context, References, Evaluate, Iterate. (Mnemonic: Thoughtfully Create Really Excellent Inputs).

### Responsible AI Use

* **Human-in-the-loop**: Combine machine and human intelligence.
* Be mindful of confidential/sensitive information; follow organizational policies.
* Review AI outputs for accuracy.
* Disclose AI use.

### Specific AI Use Cases

* **Decode Complex Security Frameworks**: Explain documents like NIST publications.
* **Refine Code**: Add comments, explain, suggest improvements.
* **Understand System Vulnerabilities**: Define, identify impact, suggest mitigation.
* **Prioritize Alerts**: Review IDS alerts, suggest next steps.
* **AI as a Learning Tool**: Generate sample interview questions.
