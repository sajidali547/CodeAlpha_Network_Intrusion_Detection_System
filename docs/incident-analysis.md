# Suricata IDS Incident Analysis

## Alert

SOC LAB - Suspicious HTTP User Agent

## Detection Rule

Signature ID: 1000002

## Source

Windows test endpoint

## Destination

Ubuntu IDS/Web Server

## Protocol

HTTP

## Observed Activity

An HTTP request containing the custom User-Agent string `SOC-LAB-TEST` was detected by Suricata.

## Investigation

The Suricata EVE JSON alert was reviewed to identify:

- Timestamp
- Source IP
- Source port
- Destination IP
- Destination port
- Protocol
- Detection signature
- Severity

## Classification

True Positive

## Disposition

Authorized lab simulation.

## Recommended Response

In a production environment, the analyst would:

1. Validate the source system.
2. Review related network events.
3. Investigate the process responsible for the connection.
4. Determine whether the signature represents malicious activity.
5. Contain or block the source if malicious activity is confirmed.
6. Document and escalate the incident where appropriate.
