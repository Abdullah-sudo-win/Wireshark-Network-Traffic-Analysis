# Wireshark Network Traffic Analysis

## Project Overview

This project demonstrates practical network traffic analysis using Wireshark and packet capture (PCAP) files in a cybersecurity lab environment.

The objective is to examine network communications, identify relevant network protocols, investigate suspicious traffic patterns, and understand potential security risks.

This project focuses on practical skills relevant to a Tier 1 Security Operations Center (SOC) Analyst.

## Objectives

- Analyze TCP and UDP network traffic.
- Examine ARP traffic and identify potential IP conflicts or spoofing indicators.
- Investigate HTTP requests and potential sensitive data exposure.
- Inspect HTTPS connections and TLS Client Hello information.
- Analyze DNS queries and responses.
- Examine LLMNR and WPAD traffic.
- Apply Wireshark display filters to isolate relevant network events.
- Document findings using technical evidence.

## Tools and Technologies

- Wireshark
- PCAP / PCAPNG files
- TCP/IP
- DNS
- ARP
- HTTP / HTTPS
- TLS
- LLMNR
- Nmap

## Investigation and Evidence

This project contains eight selected screenshots documenting the investigation process.

### 1. TCP Scan Patterns
**Evidence:** `01-Nmap-TCP-Scan-Patterns.png`

Examines TCP scanning patterns and network communication behavior.

### 2. UDP Port Unreachable
**Evidence:** `02-Nmap-UDP-Port-Unreachable.png`

Examines UDP traffic and ICMP port-unreachable responses.

### 3. ARP Duplicate IP / Spoofing
**Evidence:** `03-ARP-Duplicate-IP-Spoofing.png`

Examines ARP traffic and potential duplicate IP or spoofing indicators.

### 4. HTTP POST Sensitive Data Exposure
**Evidence:** `04-HTTP-POST-Sensitive-Data-Exposure.png`

Inspects HTTP POST requests and identifies the potential exposure of sensitive information.

### 5. HTTP 200 OK Server Response
**Evidence:** `05-HTTP-200-OK-Server-Response.png`

Examines HTTP server responses and communication behavior.

### 6. HTTPS TLS Client Hello and SNI
**Evidence:** `06-HTTPS-TLS-Client-Hello-SNI.png`

Inspects TLS Client Hello packets and Server Name Indication (SNI) information.

### 7. DNS Query and Response Analysis
**Evidence:** `07-DNS-Query-Response-Analysis.png`

Examines DNS queries, responses, requested domain names, and returned IP addresses.

### 8. LLMNR and WPAD Queries
**Evidence:** `08-LLMNR-WPAD-Queries.png`

Examines LLMNR name-resolution requests and WPAD-related network traffic.

## Wireshark Display Filters

The following filters were used during the investigation:

| Purpose | Display Filter |
|---|---|
| DNS traffic | `dns` |
| DNS queries | `dns.flags.response == 0` |
| DNS responses | `dns.flags.response == 1` |
| LLMNR traffic | `llmnr` |
| mDNS traffic | `mdns` |
| TLS Client Hello | `tls.handshake.type == 1` |

## Skills Demonstrated

- Network traffic analysis
- Packet inspection
- Protocol identification
- DNS investigation
- TCP/IP troubleshooting
- HTTP and HTTPS analysis
- TLS handshake inspection
- Network reconnaissance analysis
- Security event investigation
- Technical documentation

## Security Relevance

Network traffic analysis is an important SOC Analyst skill.

Understanding normal network behavior helps analysts investigate unusual communications, recognize suspicious patterns, and identify events that may require further investigation.

Network indicators must always be evaluated in context and should not automatically be treated as proof of compromise.

## Environment

This project was completed as part of hands-on cybersecurity training using TryHackMe lab environments.

All analysis was conducted for educational purposes.

## Conclusion

This project demonstrates practical experience analyzing network traffic with Wireshark, investigating multiple network protocols, applying display filters, and documenting technical observations.

These skills support preparation for an entry-level SOC Analyst position.

---

**Project Category:** Cybersecurity / Network Security  
**Focus:** Network Traffic Analysis  
**Primary Tool:** Wireshark
