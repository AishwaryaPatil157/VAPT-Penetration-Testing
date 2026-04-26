# VAPT - Vulnerability Assessment and Penetration Testing
## By: Aishwarya Patil

## Tools Used
- Kali Linux
- Metasploitable 2
- Nmap 7.99
- Metasploit Framework v6.4.126

## Target Details
- Attacker IP: 192.168.40.128 (Kali)
- Target IP: 192.168.40.129 (Metasploitable)

## Phase 1 - Network Scan
Command: nmap -sn 192.168.40.0/24
Result: Found target at 192.168.40.129

## Phase 2 - Vulnerability Scan
Command: nmap -sV -sC 192.168.40.129
Findings:
- Port 21: vsftpd 2.3.4 VULNERABLE
- Port 22: OpenSSH 4.7
- Port 80: Apache 2.2.8
- SMB signing disabled

## Phase 3 - Exploitation
Exploit: vsftpd_234_backdoor
Result: ROOT access obtained
whoami = root

## Conclusion
Successfully exploited CVE-2011-2523
Gained full root access to target system
