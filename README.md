# SIEM Log Analysis – Brute Force Detection

## 📌 Objective
This project simulates a Security Information and Event Management (SIEM) use case where suspicious authentication activity is detected, analyzed, and escalated. The goal is to demonstrate SOC Analyst Level 1 capabilities in alert triage, log analysis, and incident reporting.

---

## 🛠️ Tools & Concepts
- SIEM (Simulated)
- Log Analysis
- Linux Authentication Logs
- Threat Detection
- Incident Response Lifecycle

---

## 🚨 Alert Scenario
A SIEM alert was triggered due to multiple failed SSH login attempts from a single IP address followed by a successful login.

---

## 🔍 Investigation Process

### 1. Alert Review
- High severity alert triggered
- Suspicious login behavior detected

### 2. Log Analysis
- Multiple failed login attempts observed
- Same IP targeting multiple usernames
- Successful login after repeated failures

### 3. Threat Identification
- Attack Type: SSH Brute Force
- Source IP: 192.168.1.100

### 4. Risk Assessment
- Severity: HIGH
- Possible account compromise

---

## 🚩 Indicators of Compromise (IOCs)

- Malicious IP: 192.168.1.100
- Event Type: Authentication Attack
- Target System: Linux Server

---

## 🛡️ Response Actions

- Block malicious IP
- Reset compromised credentials
- Enable brute-force protection (Fail2Ban)
- Enforce SSH key-based authentication

---

## 📊 Outcome
Successfully simulated a SIEM workflow including alert generation, investigation, and incident response.

---

## 📁 Project Structure

logs/
alerts/
analysis/
screenshots/

## 📌 Notes

This project simulates a SIEM environment without a live SIEM tool such as Splunk or Wazuh. The alert data and logs are generated to demonstrate SOC Analyst Level 1 skills in:

- Alert triage
- Log correlation
- Threat detection
- Incident documentation

This approach reflects real-world SOC workflows in a controlled lab environment.


---

## 👨‍💻 Author
Rodgers Rono  
GitHub: https://github.com/Ronoh12
