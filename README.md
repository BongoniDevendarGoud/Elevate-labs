Nmap Scan Output Analysis – Elevate Labs Internship Task 1
📌 Assignment Overview

This task involved analyzing the output of an Nmap SYN scan (nmap -sS) performed on a local network. The objective was to enumerate active hosts, identify open ports, and assess potential security risks associated with each detected service.

Tool Used: Nmap 7.95

Scan Type: SYN scan (stealth scan)

🔎 Findings – Open Ports & Risks
Port	Service	Risks	Mitigation
21	FTP	Plaintext transmission of data and credentials, brute-force attacks	Replace with SFTP/FTPS, disable if unnecessary
22	SSH	Brute-force attempts, weak configs, outdated versions	Use key-based auth, disable root login, enforce strong passwords
23	Telnet	Plaintext transmission, sniffing, MitM attacks	Replace with SSH, disable if not required
53	DNS	Amplification attacks, cache poisoning, lateral movement	Restrict access, keep DNS updated, monitor queries
80	HTTP	Vulnerable web apps, brute-force, outdated server software	Use HTTPS (443), apply patches, implement WAF
445	MSRPC / SMB	Remote code execution, ransomware (e.g., WannaCry), credential theft	Block SMB externally, patch regularly, restrict sharing permissions
139	NetBIOS-SSN	Info leaks, brute-force, Windows network exploitation	Block or disable NetBIOS over TCP/IP, enforce segmentation
🛡️ Conclusion

The analysis demonstrates how an attacker could exploit exposed services if proper mitigations are not in place. Applying security best practices such as patch management, protocol hardening, encryption, and access restriction can significantly reduce risks.
