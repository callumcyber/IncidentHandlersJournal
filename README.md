# Incident Handler's Journal

*Google Cybersecurity Professional Certificate — Course 6 Portfolio Project*

## Introduction

This Incident Handler's Journal documents a series of practical cybersecurity 
exercises completed throughout my professional development. Each journal entry 
captures the investigation of a simulated security incident or hands-on 
technical activity, applying incident response principles, documenting findings, 
and reflecting on key lessons learned. Together, these entries demonstrate my 
progression in areas including threat analysis, network traffic investigation, 
security tooling, incident documentation, and defensive security practices. The 
journal provides evidence of my growing ability to approach security incidents 
methodically while continually developing the technical and analytical skills 
required for an entry-level cybersecurity role.

## Entry 01 — 06/04/2026

**Description**

Documenting a cybersecurity incident. This security incident was handled across
two distinct operational phases:

- **Detection and Analysis:** The initial phase involved the organisation
  identifying the ransomware activity on the network. Recognising the
  complexity of the threat during the analysis stage, internal teams
  immediately engaged external organisations to secure specialised technical
  assistance.
- **Containment, Eradication, and Recovery:** Immediate containment protocols
  were executed, most notably the proactive shutdown of corporate computer
  systems to isolate the threat. Due to the scale of the compromise, the
  organisation determined that independent eradication and recovery were not
  feasible, prompting further escalation to external security partners to
  assist with full system restoration.

**Tool(s) used**

None.

**The 5 W's**

- **Who:** An organised group of unethical hackers.
- **What:** A ransomware attack. The threat actors distributed phishing
  emails containing malicious attachments; at least one employee downloaded
  an attachment, allowing the malware to infect the local device before
  propagating across the network.
- **When:** Tuesday at 09:00 am.
- **Where:** A small U.S. healthcare clinic.
- **Why:** The incident occurred because unethical hackers successfully
  breached the organisation's systems via a phishing campaign. Upon gaining
  access, the attackers deployed ransomware across internal systems,
  encrypting critical files. The attackers' motivation appears to be strictly
  financial, as the recovery note demanded a large ransom in exchange for the
  decryption key.

**Additional notes**

1. A formal assessment of the company's security posture and a "lessons
   learned" session must follow to establish how the healthcare clinic can
   prevent an incident of this nature from recurring. This attack could have
   been prevented through robust security awareness training and effective
   email vetting procedures.
2. Long-term resilience measures should be implemented, such as establishing
   robust backup strategies and defining explicit Recovery Time Objectives
   (RTOs) and Recovery Point Objectives (RPOs) to minimise operational
   downtime during future incidents.
3. A critical strategic decision remains regarding whether the company should
   pay the ransom to retrieve the decryption key, weighing compliance and
   ethical risks against data recovery needs.

## Entry 02 — 30/04/2026

**Description**

Documenting a security incident involving a suspicious file hash
investigation.

An employee received a phishing email containing a password-protected
spreadsheet attachment, with the password provided in the body of the email.
Upon downloading the file and entering the credential, a malicious payload
was executed on the local machine. A cryptographic hash of the file was
subsequently generated to facilitate a technical investigation.

**Tool(s) used**

For this activity, I used VirusTotal, which is an investigative tool that
analyses files and URLs for malicious content such as viruses, worms,
trojans, and more. It's a useful tool for quickly checking whether an
indicator of compromise, such as a website or file, has been reported as
malicious by others in the cybersecurity community. I used VirusTotal to
analyse a file hash, which was reported as malicious.

This incident occurred in the Detection and Analysis phase. The scenario put
me in the place of a security analyst at a SOC investigating a suspicious
file hash. After the suspicious file was detected by the security systems in
place, I had to perform deeper analysis and investigation to determine if the
alert signified a real threat.

**The 5 W's**

- **Who:** An unknown malicious actor.
- **What:** A phishing email containing a password-protected spreadsheet
  with an embedded malicious executable. The payload generated a SHA-256
  file hash of
  `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`.
- **When:** At 01:20 pm, an alert was generated and sent to the
  organisation's SOC after the intrusion detection system flagged the file
  execution.
- **Where:** A financial services company, on an employee computer.
- **Why:** The threat actor targeted the organisation to compromise an
  internal endpoint and gain unauthorised access to sensitive data. The
  attack succeeded because the organisation's security controls allowed the
  malicious email to reach the recipient, enabling the employee to download
  and execute the attachment.

**Additional notes**

1. A comprehensive security audit should be conducted at the financial
   services firm to evaluate existing perimeter boundaries and endpoint
   defence measures.
2. Advanced Threat Protection (ATP) solutions must be explored, such as
   Secure Email Gateways (SEGs), API-based cloud email security, or
   Next-Generation Firewalls (NGFWs). Implementing these controls will
   establish a layered, defence-in-depth posture capable of inspecting
   encrypted attachments or flagging anomalous inbound sender behaviour.
3. Targeted security awareness training should be formalised for all
   personnel, specifically focusing on identifying sophisticated social
   engineering tactics, such as password-protected attachments, and
   reinforcing internal reporting protocols for suspicious emails.

## Entry 03 — 07/05/2026

**Description**

Analysing a packet capture file.

**Tool(s) used**

For this activity, Wireshark was utilised to analyse a packet capture file.
Wireshark is a network protocol analyser with a graphical interface, valued
in cybersecurity for its ability to capture and inspect network traffic. By
allowing security analysts to examine live or recorded data packets, the
tool serves as a critical asset for detecting and investigating malicious
activity across a network.

**The 5 W's**

Not applicable — this entry was a skills exercise rather than a live
incident.

**Additional notes**

This was my first time using Wireshark, so I was excited to complete this
exercise and analyse a packet capture file. At first glance, the interface
was challenging, but I enjoyed learning how to use it and getting hands-on
experience with Wireshark. I can see why it's such a powerful tool for
understanding network traffic.

## Entry 04 — 15/05/2026

**Description**

Capturing my first packet.

**Tool(s) used**

For this activity, tcpdump was utilised to capture and analyse network
traffic. Accessible via the command-line interface, tcpdump is a network
protocol analyser that, similar to Wireshark, provides essential value in
cybersecurity by allowing security analysts to capture, filter, and inspect
network traffic data.

**The 5 W's**

Not applicable — this entry was a skills exercise rather than a live
incident.

**Additional notes**

I'm still new to using the command-line interface, so using it to capture
and filter network traffic was a challenge. I got stuck a couple of times
because I used the wrong commands. However, after revisiting the learning
materials and repeating some of the steps, I was able to complete the
activity and successfully capture network traffic.

## Entry 05 — 20/05/2026

**Description**

Documenting a data breach incident and subsequent technical investigation.

A web application vulnerability enabled an external threat actor to bypass
authorisation controls and gain unauthorised access to customer Personally
Identifiable Information (PII) and financial records, impacting
approximately 50,000 customer records. The financial impact is estimated at
$100,000 in direct costs and potential revenue loss. The root cause was
isolated to the e-commerce platform's URL parameter handling, allowing the
attacker to systematically scrape sensitive transaction data.

**Tool(s) used**

SIEM Tool & Wireshark: Utilised within the Detection and Analysis phase to
review web server access logs and network traffic data, which confirmed a
single log source generating an exceptionally high volume of sequentially
listed customer order requests.

**The 5 W's**

- **Who:** An independent unethical hacker.
- **What:** An employee received an email stating that they had stolen
  customer data, demanding a ransom. The root cause of the incident was
  identified as a vulnerability in the e-commerce web application. This
  vulnerability allowed the attacker to perform a forced browsing attack and
  access customer transaction data by modifying the order number included in
  the URL string of a purchase confirmation page. This vulnerability allowed
  the attacker to access customer purchase confirmation pages, exposing
  customer data, which the attacker then collected and exfiltrated. The
  logs indicated that the attacker accessed the information of thousands of
  purchase confirmation pages.
- **When:** An initial ransom email was received at 03:13 pm on 22 December
  2022 but was dismissed as spam. A second email containing a data sample
  was received on 28 December 2022, prompting an investigation. The formal
  security incident and unauthorised access footprint were established on
  28 December 2022 at 19:20 PT. The investigation concluded on 31 December
  2022.
- **Where:** A mid-sized retail company's public-facing e-commerce web
  application.
- **Why:** The attack was motivated by financial gain, as evidenced by an
  initial $25,000 cryptocurrency demand that escalated to $50,000 upon the
  second contact.

**Additional notes**

1. **Defensive Gaps & Detection:** This incident highlights a critical gap
   in behavioural alerting. A single external source was permitted to query
   thousands of sensitive customer pages sequentially without triggering a
   rate-limiting threshold or generating a high-priority SOC alert. A
   defence-in-depth approach is needed; a SIEM system and an IPS tool
   working in tandem could have flagged this through behavioural analysis,
   allowing the IPS to dynamically block the IP address and limit the
   damage.
2. **Remediation & Response Actions:** Following containment, the
   organisation collaborated with public relations to disclose the data
   breach transparently to customers. To mitigate external impact and
   preserve brand reputation, free identity protection services were offered
   to all affected individuals.
3. **Strategic Resilience:** The immediate recommendations proposed,
   including routine vulnerability scanning, penetration testing, strict URL
   allowlisting, and enforcing robust authentication requirements, are
   critical to hardening the perimeter. However, current security systems
   must be continuously revised to ensure that if these initial
   authorisation controls are ever bypassed again, active monitoring and
   automated response capabilities are in place to rapidly detect and
   contain threats, helping to minimise their impact and strengthen the
   organisation's overall security posture.

## Reflections/Notes

**Technical Progression and Command-Line Adaptation**

While expanding my hands-on experience with command-line utilities,
configuring tcpdump using the correct command syntax and filtering flags
required a methodical approach. Rather than relying on graphical interfaces,
adapting to the CLI environment required a structured approach to accurately
configure packet capture parameters. By systematically auditing my syntax
against expected network behaviours and breaking down the commands into
modular components, I quickly achieved a solid working understanding. This
process reinforced a critical engineering principle: accurate packet capture
and log collection depend on precise command syntax to produce reliable
results.

**Operational Evolution of Incident Response**

My understanding of the incident response lifecycle has progressed from a
conceptual foundation to a more structured, practical methodology. Developing
these journals reinforced that effective incident response depends on
structured processes, clear documentation, and the appropriate use of
security tools, rather than isolated technical actions. Navigating the
phases from initial detection to long-term eradication highlighted how an
organisation's security posture relies on well-defined incident response
playbooks, clear communication procedures, and defensive frameworks to limit
the spread and operational impact of an incident, reducing potential damage
to the organisation.

**Telemetry Analysis and Risk Mitigation**

Exploring network traffic analysis and log auditing proved to be one of the
most engaging aspects of this technical curriculum. Gaining exposure to
protocol analysers provided valuable insight into network traffic,
infrastructure communications, and technical troubleshooting, and how
technical evidence can be used to identify potential security risks.
Developing this foundation has solidified my focus on defensive security
operations, technical vendor support, and risk governance. I am actively
expanding my skill set to bridge the gap between technical system
diagnostics and the broader controls required to maintain an organisation's
overall security and compliance posture.

## Skills Demonstrated

- Incident documentation using a structured 5 W's methodology
- Hands-on use of investigative and network analysis tools: VirusTotal,
  Wireshark, and tcpdump
- Applying incident response principles through practical, 
tool-based investigations
- Reflective practice — identifying gaps, lessons learned, and next steps
  after each incident

---
*This project is based on fictional scenarios as part of the Google
Cybersecurity Professional Certificate coursework.*
