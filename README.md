# Code-Academy-Diploma-Project
# Shadow Hackers: CTF Walkthroughs and Vulnerability Analyses

## Overview

This repository contains comprehensive walkthroughs, vulnerability analyses, and proof-of-concept (PoC) exploitations for a series of Capture the Flag (CTF) challenges. These challenges are designed to simulate real-world penetration testing scenarios involving common and critical vulnerabilities across various environments. The repository documents methods, tools, and remediations for vulnerabilities, making it an excellent resource for cybersecurity enthusiasts and professionals.

## Features

- **CTF Machines Analyzed**:
  - **Collabs**: Focused on PHP vulnerabilities, SSH exploitation, and privilege escalation using tools like PwnKit.
  - **Blitz**: Emphasized SQL injection, Node.js misconfigurations, Jenkins exploitation, and multi-level privilege escalation.
  - **Bytescribe**: Highlighted FTP enumeration, crontab misconfigurations, and outdated software vulnerabilities.
  - **GitLab**: Exploited CVE-2023-2825 and CVE-2023-5536, LXD privilege escalation, and sensitive data exposure.
  - **ShadowStore**: Covered LFI, XXE, SQL injection, file uploads, and reverse shell execution.
  - **PoD**: Focused on sensitive data exposure, SSH misconfigurations, and multi-user privilege escalations.

- **Key Vulnerabilities Exploited**:
  - **Web Exploits**: SQL Injection (SQLi), Cross-Site Scripting (XSS), Local File Inclusion (LFI), and PHP Object Injection.
  - **System Misconfigurations**: Crontab misuse, SUID binaries, and outdated software versions.
  - **Privilege Escalation**: LXD group privilege misuse, Node.js command injection, and misconfigured sudo permissions.
  - **Sensitive Data Exposure**: Analysis of phpinfo, robots.txt, and exposed credentials in system logs and source files.

- **Tools and Techniques Used**:
  - Reconnaissance: `nmap`, `dirb`, and `sqlmap`
  - Exploitation: Metasploit, reverse shells, and crafted payloads
  - Privilege Escalation: PwnKit, custom scripts, and LXD-based container escapes
  - Hash Cracking: John the Ripper, Base64 decoding, and other encoding mechanisms

## Highlights from Walkthroughs

### Collabs
- **Vulnerabilities Exploited**: Outdated PHP, weak SSH credentials, and directory enumeration.
- **Key Exploits**:
  - Uploaded a reverse shell for remote access.
  - Used PwnKit to escalate privileges to root.
- **Flags Captured**: ICSD{66d74978b307889bea234a4bc6570a36}, ICSD{45caa8f3afa6fc94aa3c039ceeeb7883}.

### Blitz
- **Vulnerabilities Exploited**: SQL injection, Jenkins misconfigurations, and Node.js privilege escalation.
- **Key Exploits**:
  - Leveraged SQLMap for OS shell access.
  - Exploited Jenkins Script Console for reverse shell execution.
  - Crafted Node.js scripts to escalate privileges to root.
- **Flags Captured**: ICSD{21a81470de1660a78f10fa4d93480f11}, ICSD{d82010d823a7b754fb741f17fc2606b3}.

### GitLab
- **Vulnerabilities Exploited**: Path traversal (CVE-2023-2825) and LXD group privilege escalation (CVE-2023-5536).
- **Key Exploits**:
  - Brute-forced credentials from `robots.txt`.
  - Exploited GitLab vulnerabilities for access and privilege escalation.
- **Flags Captured**: ICSD{0e705c84c1a17ed632e91f9304676f07}.

### ShadowStore
- **Vulnerabilities Exploited**: 
  - LFI, XXE, PHP Object Injection, SQL Injection, and File Upload.
  - Remote Code Execution (RCE) and Reverse Shell Execution (RSE).
  - Sensitive data exposure through `/phpinfo.php`.
- **Key Exploits**:
  - Uploaded reverse shells via the vulnerable file upload mechanism and executed them through RCE.
  - Used XXE to extract sensitive data and escalated privileges using SSH after decoding credentials.
  - Creative use of cultural references and hints enhanced the CTF experience.
- **Insights**: ShadowStore offers a holistic test bed of vulnerabilities, from web-based exploits to logical hints for privilege escalation.

### PoD
- **Vulnerabilities Exploited**:
  - Sensitive Data Exposure through misconfigured files and SSH keys.
  - SQL Injection vulnerabilities and LFI examples for privilege escalation.
- **Key Exploits**:
  - Cracked multi-layered encoded messages using SQLmap and decoding tools.
  - Found hidden SSH credentials in `.profile` files for lateral movement.
  - Extracted images containing credentials for higher-privilege users.
- **Final Stage**:
  - Used `.bash_history` to reveal the root password and successfully captured all flags.
- **Insights**: The PoD machine focuses on multi-step exploitation requiring lateral movement, file analysis, and decoding skills.

## Learning Outcomes
This repository demonstrates:
1. How to identify and exploit web application vulnerabilities.
2. Effective use of enumeration tools for system and network discovery.
3. Techniques for escalating privileges using system misconfigurations and known CVEs.
4. Methods for securing vulnerable systems, mapped to ISO 27001 controls.

## Tools and Dependencies
- **Enumeration**: `nmap`, `dirb`, `sqlmap`
- **Exploitation**: Metasploit, custom scripts, Burp Suite
- **Privilege Escalation**: `john`, PwnKit, and custom Node.js scripts

## Future Enhancements
- Adding machine-specific remediation recommendations.
- Expanding scenarios to include advanced tactics like lateral movement and Active Directory exploitation.
- Integrating more machine learning techniques for automated vulnerability detection.

## Credits
This repository was created and documented by the **Shadow Hackers** team:
- **Azarin Bayali** (Leader)
- **Nijat Mazanli**
- **Farid Hamzayev**
- **Seymur Shukurlu**
