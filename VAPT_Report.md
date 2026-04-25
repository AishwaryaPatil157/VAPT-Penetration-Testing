# Vulnerability Assessment and Penetration Testing (VAPT)
## Internship Project Report - Aishwarya Patil

## 1. Objective
Identify vulnerabilities in a simulated environment and perform
penetration testing to exploit weaknesses ethically.

## 2. Tools Used
- Kali Linux (Attack Machine)
- Metasploitable 2 (Target Machine)
- Nmap 7.99
- Metasploit Framework v6.4.126

## 3. Environment Setup
- Attacker: Kali Linux - 192.168.40.128
- Target: Metasploitable 2 - 192.168.40.129
- Network: VMware NAT

## 4. Phase 1 - Reconnaissance
Command: nmap -sn 192.168.40.0/24
Result: Discovered target at 192.168.40.129

## 5. Phase 2 - Scanning
Command: nmap -sV -sC 192.168.40.129
Findings:
- Port 21: vsftpd 2.3.4 (VULNERABLE)
- Port 22: OpenSSH 4.7
- Port 80: Apache 2.2.8
- SMB signing disabled (dangerous)
- OS: Ubuntu 8.04

## 6. Phase 3 - Exploitation
Tool: Metasploit Framework
Exploit: e