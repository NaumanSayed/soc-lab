# SOC Lab: Attack Simulation & Detection

## Overview

This project simulates a Security Operations Center (SOC) environment by performing network reconnaissance, vulnerability scanning, and traffic analysis in a virtual lab.

## Lab Setup

* Attacker: Kali Linux
* Victim: Ubuntu (Apache Web Server)
* Platform: UTM (Apple Silicon)
* Network: Shared virtual network

## Tools Used

* Nmap (port scanning)
* Nikto (web vulnerability scanning)
* Wireshark (network traffic analysis)

## Attack Simulation

### 1. Port Scanning

Used Nmap to identify open ports on the target system.

* Initially: All ports closed
* After configuring Apache: Port 80 (HTTP) opened

### 2. Vulnerability Scanning

Used Nikto to scan the web server.

Findings:

* Outdated Apache version
* Missing security headers
* Potential information disclosure (ETag)

### 3. Traffic Analysis

Captured traffic using Wireshark during scanning activity.

Observations:

* Repeated TCP SYN packets from attacker
* SYN-ACK responses from open ports
* RST packets used to terminate connections

## Key Insights

* Attackers use port scanning to discover services
* Misconfigured web servers expose security risks
* Network traffic patterns can reveal malicious activity

## Conclusion

This project demonstrates how security analysts detect and analyze malicious behavior using real-world tools in a controlled lab environment.
