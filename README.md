# network-recon-nmap-task1
Task 1 - Port Scanning and Network Reconnaissance with Nmap (Elevate Labs Internship)

# Network Recon — Nmap Task 1

**Task:** Port scanning & basic network reconnaissance (Elevate Labs — Task 1)

## Overview
Performed TCP SYN scan to identify open ports on the local VM network (<REDACTED_IP>). Captured packets during the scan with Wireshark (capture file kept privately).

## Tools
- Nmap 7.95
- Wireshark (capture used locally)
- xsltproc (for HTML conversion)

## What I did
1. Host discovery and SYN scan:
   - `sudo nmap -sS -T4 --open <REDACTED_IP> -oN scan_results_redacted.txt -oX scan_results_redacted.xml`
2. Converted XML to HTML:
   - `xsltproc /usr/share/nmap/nmap.xsl scan_results_redacted.xml -o scan_results.html`
3. Captured packets using Wireshark and kept the raw pcap privately (not uploaded).

## Results (summary)
- Devices discovered: Not Any  
- Common open ports observed: `135 (MSRPC)`, `445 (microsoft-ds)`, `3306 (MySql)`  

## Files in this repo
- `scan_results_redacted.txt` — redacted Nmap output
- `scan_results_redacted.xml` — redacted XML
- `Wireshark-task1-ss-edited.jpg` — redacted wireshark screenshot
- `wireshark_summary.txt` - wireshark data summary file

## Key learnings
- How TCP SYN scan works and how to interpret SYN/SYN-ACK.
- Importance of redacting sensitive information before public sharing.
- How Nmap and Wireshark complement each other for network reconnaissance.
