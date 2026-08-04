# Active Directory Security Lab

A vulnerable Active Directory lab built for learning Windows security, penetration testing, privilege escalation, and Active Directory attack paths in a safe environment.

> This project was created for educational purposes inside an isolated virtual lab.

---

## Objectives

- Deploy an Active Directory environment
- Configure intentionally vulnerable settings
- Practice Active Directory enumeration
- Simulate privilege escalation
- Study lateral movement
- Gain hands-on experience with common AD attack techniques

---

# Lab Architecture

Machines

- Windows Server 2019 (Domain Controller)
- Windows 10 Enterprise Client 1
- Windows 10 Enterprise Client 2
- Kali Linux Attacker

Network Design

Kali -> Windows Client -> Domain Controller

The Domain Controller was intentionally isolated so it could only be reached after compromising a client machine.

---

# Technologies

- Windows Server 2019
- Active Directory Domain Services
- DNS
- Group Policy
- Windows 10 Enterprise
- Kali Linux
- VirtualBox

---

# Lab Configuration

The environment includes intentionally vulnerable configurations such as:

- Disabled Windows Defender
- Disabled Windows Firewall
- Enabled WinRM
- Enabled RDP
- Weak passwords
- AlwaysInstallElevated
- Kerberos Pre-Authentication disabled
- Passwords stored in Description field
- Sensitive credentials stored on client
- Service Account with SPN
- Anonymous RPC enumeration

---

# Attack Workflow

The following attack chain was performed inside the lab.

1. LLMNR Poisoning
2. NTLM Hash Capture
3. Offline Password Cracking
4. Evil-WinRM Remote Access
5. WinPEAS Enumeration
6. AlwaysInstallElevated Privilege Escalation
7. SYSTEM access on Client
8. Discovery of stored administrator credentials
9. Pivoting using Ligolo-ng
10. RDP access to Domain Controller
11. Credential Dumping using Mimikatz
12. Domain Controller compromise using Impacket PsExec

---

# Tools Used

- Responder
- Evil-WinRM
- WinPEAS
- Ligolo-ng
- Mimikatz
- Impacket
- Hashcat
- PowerShell

---

# Learning Outcomes

This project helped me understand:

- Active Directory architecture
- Windows authentication
- Lateral movement
- Credential attacks
- Privilege escalation
- Pivoting
- Domain compromise methodology

---

# Documentation

Detailed setup documentation is included in:

[AD Lab Setup Report](AD_Lab_Setup_Report.pdf)

---

## Disclaimer

This project was performed entirely inside an isolated virtual laboratory for educational purposes.
