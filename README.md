# Security Incident Analysis: Brute-Force Attack and Malicious Redirection

## Project Overview

A practical case study developed during the [Google Cybersecurity Professional Certificate](https://www.coursera.org/google-certificates/cybersecurity-certificate), focused on analyzing a simulated security incident. This project's objective was to investigate a security alert, analyze network traffic logs (`tcpdump`), document the findings in a technical report, and propose effective mitigation measures to prevent future attacks.

---

## The Scenario

The analysis was based on an incident where a disgruntled ex-employee compromised the company's web server, `yummyrecipesforme.com`. The attack unfolded as follows:

1.  **Initial Access:** The attacker performed a **brute-force attack** against the administration panel, exploiting a default password that had not been changed.
2.  **Compromise:** After gaining access, the attacker injected a malicious JavaScript code snippet into the website.
3.  **Malicious Action:** The script prompted site visitors to download a fake executable file.
4.  **Redirection:** After the file was executed, the user's browser was redirected to a fake website (`greatrecipesforme.com`), which was controlled by the attacker and hosted malware.

---

## Tools and Methodology

To investigate and respond to the incident, the following methodology was applied:

* **Controlled Environment (Sandbox):** The suspicious website was accessed in a sandbox environment to observe its behavior without risking the production network.
* **Network Traffic Analysis:** The `tcpdump` tool was used to capture and analyze network packets, allowing for the reconstruction of the event sequence.
* **Log Analysis:** The `tcpdump` logs were inspected to identify the DNS queries, TCP handshakes, and HTTP requests that confirmed the malicious redirection.
* **Technical Documentation:** All findings were consolidated into a formal security incident report.

---

## Incident Reports (PDF)

The complete reports, detailing the analysis and conclusions, are available at the links below. They were created in Portuguese and also translated into English to demonstrate proficiency in both languages.

* 📄 **[Incident Report - English Version (PDF)](https://github.com/cleyandson/case-study-brute-force-attack/blob/2ff81cfff4c6cf0b1e8a91fd4037acae57f7edc5/Documents/%5BEN%5D%20Security%20incident%20report%20template.pdf)**

---

## Proposed Mitigations

Based on the attack's root cause (weak credentials and lack of controls), the following remediation actions were recommended, aligned with industry best practices such as **NIST** and **CIS Controls**:

* **Implementation of a Strong Password Policy:** Requiring complexity and a minimum length for all passwords.
* **Account Lockout Mechanism:** Automatically locking accounts after multiple failed login attempts.
* **Multi-Factor Authentication (MFA):** Enabling MFA for all administrative accounts as the most effective defense against credential compromise.

---

## Skills Demonstrated

This project highlights the following essential cybersecurity skills:

-   ✅ **Network Traffic Analysis** with `tcpdump`
-   ✅ **Security Incident Response**
-   ✅ **Network Protocol Analysis** (DNS, TCP, HTTP)
-   ✅ **Technical Report Writing** and Incident Documentation
-   ✅ **Root Cause Analysis (RCA)**
-   ✅ **Recommendation of Security Controls**

---

## Contact

* **LinkedIn:** [Cleyandson Fragoso](https://www.linkedin.com/in/cleyandson-fragoso/)
* **Email:** cleyandsontech@gmail.com
