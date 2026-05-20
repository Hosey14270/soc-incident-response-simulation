# 🛡️ SOC Incident Response Simulation

## Overview

This project simulates a real-world Security Operations Center (SOC) Level 2 incident response scenario involving:

- Unauthorized account access
- Suspicious internal activity
- Sensitive data access
- Potential data exfiltration
- Misconfigured system permissions

The objective was to investigate the incident, identify the attack path, confirm the breach, and recommend containment actions.

---

## Incident Summary

An attacker successfully compromised an administrative account after multiple failed login attempts.

The attacker escalated privileges, accessed sensitive internal files, and transferred unusually large amounts of outbound traffic to an external IP address.

The incident was analyzed using log review, traffic analysis, and access control inspection.

---

## Investigation Process

### 1. Breach Confirmation

Reviewed authentication logs to determine:

- Whether unauthorized access occurred
- Compromised account
- Attacker IP address
- Severity of incident

### Key Findings

- **Compromised User:** `admin`
- **Attacker IP:** `203.45.67.89`
- **Severity:** `High`
- **Privilege Escalation:** Detected

---

### 2. Suspicious Data Access

Analyzed internal file access logs to identify:

- Sensitive files accessed
- Abnormal access behavior
- Potential exposure risk

### Key Findings

Sensitive resources accessed:

- `/secure/customer_data.csv`
- `/secure/financial_records.csv`
- `/secure/internal_docs.pdf`

**Risk Level:** `High`

---

### 3. Data Exfiltration Analysis

Reviewed outbound traffic logs to detect suspicious transfers.

### Key Findings

- **Destination IP:** `203.45.67.89`
- **Protocol/Method:** `HTTPS`
- **Suspicious outbound transfers detected**
- Large outbound data transfer observed

---

### 4. Misconfiguration Analysis

Reviewed system access controls and account configurations.

### Findings

Security weaknesses identified:

- Weak admin credentials
- Excessive admin privileges
- `NOPASSWD` privilege escalation risk
- Missing restrictions on sensitive directories

---

## Containment Actions Recommended

Immediate actions recommended:

- Disable compromised admin account
- Block malicious IP address
- Reset credentials
- Remove unnecessary privileges
- Restrict sensitive directory access
- Investigate persistence mechanisms
- Monitor outbound traffic

---

## Tools Used

- Kali Linux
- GitHub
- Log Analysis
- Incident Response Techniques

---

## Skills Demonstrated

- Incident Validation
- Log Analysis
- Threat Detection
- Data Exfiltration Analysis
- Access Control Review
- Security Recommendations
- SOC Investigation Workflow

---

## Repository Structure

```text
soc-incident-response-simulation/
│
├── screenshots/
├── findings/
└── README.md
```

---

## Author

Osi Oarue-Itseuwa
Aspiring Cybersecurity Analyst | SOC & Incident Response Enthusiast
