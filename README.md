# Intrusion Detection Investigation

## Project Overview
This project explores intrusion detection and web application security using Kali Linux, Metasploitable 2, DVWA, and PHPIDS in an isolated cybersecurity home lab. The investigation examines how suspicious web requests appear in security logs.

## Tools Used
- Kali Linux
- Oracle VirtualBox
- Metasploitable 2
- Damn Vulnerable Web Application (DVWA)
- PHPIDS
- Nmap

## Project Objectives
- Identify network services in an authorized lab.
- Review suspicious web application activity.
- Examine PHPIDS security logs.
- Document findings with screenshots.

## Lab Environment
Testing was performed against an intentionally vulnerable Metasploitable 2 virtual machine from a Kali Linux virtual machine in an isolated, authorized lab.

## Investigation Process
1. Verified connectivity to the lab target at `192.168.56.20`.
2. Used Nmap to identify open ports and service versions.
3. Checked whether the FTP service allowed anonymous login.
4. Examined Telnet and HTTP services.
5. Opened DVWA in Firefox and explored its security testing interface.
6. Reviewed the PHPIDS log for recorded suspicious requests.
7. Captured screenshots of recreated lab demonstrations for documentation.

## Findings
- **FTP (TCP/21):** Nmap's `ftp-anon` script reported that anonymous FTP login was allowed.
- **Telnet (TCP/23):** The Telnet service was open. Telnet does not encrypt traffic by default.
- **HTTP (TCP/80):** Nmap identified Apache HTTP Server 2.2.8.
- **PHPIDS:** The log displayed entries associated with suspicious requests, including XSS-related activity. These entries illustrate the value of log review in investigating potential attacks.

## Evidence
Screenshots captured during the recreated lab demonstration include network scans, the DVWA dashboard, and the PHPIDS log. Screenshots can be added to a `screenshots/` folder in this repository.

## Skills Demonstrated
- Intrusion detection and log analysis
- Network service enumeration with Nmap
- Web application security fundamentals
- Security findings documentation

## What I Learned
I practiced identifying exposed services, reviewing suspicious web requests, and documenting evidence from an intentionally vulnerable lab environment.

## Ethical Notice
All testing was performed in an isolated, authorized cybersecurity lab for educational purposes.
