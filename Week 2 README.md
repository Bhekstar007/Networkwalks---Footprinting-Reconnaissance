# Week 2: Footprinting & Network Scanning Phases

## 📌 Project Overview
This repository contains the documentation, commands, and evidence for the Week 2 practical modules of my Cybersecurity internship at Networkwalks. The project covers Phase 1 (Reconnaissance & Footprinting) and Phase 2 (Scanning & Network Discovery) of a penetration testing lifecycle. 

All activities were performed against the **networkwalks.com** domain (with written permission) and my own **local LAN network**.

## 🛠️ Tools & Technologies Used
*   **Operating Systems:** Kali Linux, Windows
*   **Footprinting & OSINT:** WHOIS, WhatWeb, Nslookup, cURL, Wafw00f, DNSRecon, GHDB (Google Hacking Database), Maltego, theHarvester
*   **Network Scanning:** Zenmap (Nmap GUI), Windows CMD (`ipconfig`)

## 🔍 Activities & Key Findings

### 1. Footprinting & Reconnaissance
*   **WHOIS:** Identified domain registration details and name servers.
*   **WhatWeb:** Fingerprinted web technologies, identifying WordPress 7.1.4, JQuery 3.7.1, and Bootstrap.
*   **Nslookup:** Resolved the target domain to IP `192.232.216.135`.
*   **cURL:** Inspected HTTP response headers, revealing the WordPress REST API endpoint (`/wp-json/`).
*   **Wafw00f:** Detected the presence of a Web Application Firewall (**ModSecurity SpiderLabs**).
*   **DNSRecon:** Enumerated DNS records (NS, MX, SPF, TXT, SRV).
*   **GHDB & Maltego:** Discovered publicly available information, including open live cameras, math PDFs, and the email `info@networkwalks.com`.
*   **theHarvester:** Gathered subdomains, hosts, and public OSINT data.

### 2. Network Scanning (Zenmap)
*   Used `ipconfig` to identify the local IP and subnet.
*   Performed a Ping Scan (`nmap -sn`) on the local subnet (`192.168.xxxx.xxxx/24`).
*   Discovered **4 live hosts** and identified their IP and MAC addresses.
*   Generated a **Network Topology map** using Zenmap's GUI.

## ⚠️ Risk Analysis & Recommendations
The report includes a risk analysis based on the exposed technology and network architecture, along with actionable recommendations such as:
*   Reviewing publicly exposed HTTP headers and technology versions.
*   Properly configuring and monitoring the ModSecurity WAF.
*   Conducting regular internal network discovery scans to identify unknown devices.

## ⚖️ Disclaimer
These activities were performed strictly for **educational and research purposes** only. All testing was conducted on systems where written permission was secured, or on my own local network. The author is not responsible for any misuse of this information. Unauthorized access is illegal.

---
*Author: Bongani Fuzwayo | Batch: B084-Networkwalks | Date: 13 November 2026*