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

# README - Phishing Email Analysis Task

## Project Overview

This project involves analyzing a phishing email sample to identify key indicators of phishing attacks. The purpose of this task is to develop awareness of phishing tactics and improve skills in email threat analysis.

## Files Included

1. **Phishing\_Email\_Analysis\_Report\_Professional.pdf** - A detailed report analyzing the phishing email sample, including sender analysis, header inspection, suspicious links, attachments, urgent language, grammar/spelling checks, phishing traits summary, and answers to relevant interview questions.
2. **Email Sample** - The phishing email content used for analysis.

## Steps Performed

1. Obtained a sample phishing email from a reliable source.
2. Examined the sender's email address for spoofing or domain discrepancies.
3. Analyzed email headers for SPF, DKIM, DMARC, and IP inconsistencies.
4. Identified suspicious links and attachments.
5. Checked the email body for urgent/threatening language.
6. Verified spelling and grammar to detect phishing cues.
7. Summarized phishing traits in a structured table.
8. Answered key interview questions related to phishing and email security.

## Tools Used

* Email client (to view full email headers)
* MXToolbox Email Header Analyzer (online tool)
* FPDF (Python library for PDF generation)
* Text editor for documentation

## Purpose

This project demonstrates:

* Understanding of phishing and email spoofing
* Skills in identifying phishing indicators
* Knowledge of social engineering tactics

