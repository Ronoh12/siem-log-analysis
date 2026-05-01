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
```

Analysis

The source IP address 192.168.1.100 attempted several usernames within a short time window. The successful login after repeated failures increases the severity of the alert from suspicious activity to a potential account compromise.

Indicators of Compromise
Indicator	      Value
Source IP	      192.168.1.100
Target Host	    linux-server-01
Attack Type	    SSH Brute Force
Affected User	  validuser
Severity	       High

Recommended Response Actions
Block the source IP address.
Reset the affected user password.
Review login activity for validuser.
Enable Fail2Ban or equivalent brute-force protection.
Disable SSH password login and enforce SSH keys.
Escalate to Level 2 SOC Analyst for deeper investigation.
Conclusion

The alert is classified as a high-severity brute-force incident due to multiple failed authentication attempts followed by a successful login.
