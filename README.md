# Network Intrusion Detection System using Suricata

## CodeAlpha Cyber Security Internship - Task 4

## Overview

This project implements a network-based Intrusion Detection System using Suricata.

The objective was to monitor network traffic, create custom detection rules, analyze generated alerts, and demonstrate a basic incident-response workflow in an isolated lab environment.

## Lab Architecture

Windows Test Endpoint
        |
        | ICMP / HTTP Traffic
        v
Ubuntu Server
        |
        v
Suricata IDS
        |
        v
Detection Rules
        |
        v
EVE JSON Alerts
        |
        v
SOC Investigation
        |
        v
Containment

## Technologies Used

- Suricata
- Ubuntu Linux
- Windows
- EVE JSON
- jq
- Python HTTP Server
- UFW
- VirtualBox

## Detection Rules

### ICMP Detection

Detects ICMP traffic entering the monitored network.

Signature ID: 1000001

### Suspicious HTTP User-Agent

Detects HTTP requests containing the custom User-Agent `SOC-LAB-TEST`.

Signature ID: 1000002

## Investigation Workflow

Traffic → Detection → Alert → Triage → Investigation → Classification → Response

## Alert Analysis

Suricata EVE JSON was used to review:

- Timestamp
- Source IP
- Destination IP
- Source/Destination ports
- Network protocol
- Alert signature
- Signature ID
- Severity

## Response

The source test endpoint was temporarily blocked using UFW to demonstrate a basic containment mechanism.

The firewall rule was removed after validation.

## Skills Demonstrated

- Network security monitoring
- Intrusion Detection Systems
- Suricata
- IDS rule creation
- Network traffic analysis
- Alert triage
- SOC investigation
- JSON log analysis
- Incident response
- Firewall-based containment

## Disclaimer

All traffic was generated in an isolated personal cybersecurity lab for educational purposes.

No unauthorized systems or networks were tested.
