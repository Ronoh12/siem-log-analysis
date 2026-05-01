# SIEM Investigation Report – SSH Brute Force Alert

## Alert Details

- Alert ID: SIEM-2026-001
- Severity: High
- Rule Name: Multiple SSH Failed Logins Followed by Successful Login
- Source IP: 192.168.1.100
- Destination Host: linux-server-01
- Event Type: Authentication Attack

## Incident Summary

A SIEM-style alert was generated after multiple failed SSH login attempts were detected from the same source IP address, followed by a successful login. This pattern indicates a likely brute-force attack with possible account compromise.

## Log Evidence

```text
Failed password for invalid user admin from 192.168.1.100
Failed password for invalid user root from 192.168.1.100
Failed password for invalid user test from 192.168.1.100
Failed password for invalid user guest from 192.168.1.100
Failed password for invalid user user from 192.168.1.100
Accepted password for validuser from 192.168.1.100
