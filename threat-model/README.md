# Threat Model Overview

This project simulates common cyber attack scenarios to test detection and response capabilities of a small SOC environment. The goal is to understand potential threats, their impact and how security tools can detect and mitigate them.

## Attack Scenarios

### 1. Network Reconnaissance (Port Scanning)
- **Target:** Internal host ports
- **Behavior:** Simulated TCP/UDP scans to identify open ports
- **Purpose:** Detect early-stage reconnaissance activity
- **Detection Tools:** Suricata, Zeek

### 2. Web Application Attacks
- **Target:** Simulated web server
- **Behavior:** SQL injection, Cross-Site Scripting (XSS), Directory Traversal
- **Purpose:** Test application layer monitoring and log analysis
- **Detection Tools:** Wazuh, Suricata

### 3. Malware-like Behavior
- **Target:** Host filesystem and processes
- **Behavior:** Creation of suspicious files, simulated process injection, DNS queries to suspicious domains
- **Purpose:** Test endpoint detection and response procedures
- **Detection Tools:** Wazuh, Zeek
- 
## Risk & Impact Summary

- **Port Scanning:** Low immediate impact, but can indicate a potential attacker presence.
- **Web Attacks:** Medium to high impact; may lead to data exposure or service disruption.
- **Malware Simulation:** High impact; could compromise host integrity and critical data.

## Assumptions
- All attacks are simulated in a lab environment.
- No real user or production data is involved.
- The goal is detection and response practice, not exploitation.

