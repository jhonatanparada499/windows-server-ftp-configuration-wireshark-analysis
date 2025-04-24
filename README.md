# FTP Server Configuration and Network Traffic Analysis

This project covers a complete deployment and security assessment of an FTP server using **Windows Server 2019** and **Wireshark**.

## Tools Used
- Windows Server 2019
- IIS FTP Server Role
- Wireshark
- CMD/PowerShell
- Internet Explorer (for FTP access)

## Lab Summary

### Part 1: FTP Server Setup
- Installed the IIS and FTP roles on Windows Server.
- Created an FTP site named `Security Lab` pointing to a custom directory.
- Configured FTP banner, welcome, and exit messages.
- Created users and managed permissions using Computer Management.
- Verified authentication and file access using Internet Explorer.

### Part 2: Traffic Capture and Analysis
- Used **Wireshark** to monitor FTP traffic and extract:
  - Plaintext login credentials (`PASS` keyword)
  - Transferred file content (`Confidential.txt`)
- Identified clear-text vulnerabilities in FTP using packet inspection.
- Resolved a firewall configuration issue blocking FTP file transfers.

## Key Security Findings
- FTP credentials are visible in plaintext without encryption.
- TCP payloads from FTP file transfers are readable using packet analysis.
- Misconfigured firewalls can silently block transfers despite successful authentication.

## Lessons Learned
- Always avoid using FTP for sensitive data due to lack of encryption.
- Firewalls can affect FTP **data** transfer even if **control** connection succeeds.
- Wireshark is a powerful tool for understanding low-level network behavior.

## 🗂 Original Lab Reports
- (./Lab6-1_Report.pdf)
- (./Lab6-2_Report.pdf)
