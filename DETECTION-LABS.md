# Detection & Investigation Labs

This file will document repeatable SOC exercises performed in the homelab.

## Lab 01 — Authentication Monitoring

**Objective:** Detect suspicious authentication activity on Windows endpoints.

**Telemetry:** Windows Security Event Logs and Wazuh alerts.

**Investigation:**

1. Identify the affected host and account.
2. Review authentication timestamps and source information.
3. Correlate related events around the same time window.
4. Determine whether the activity is expected or suspicious.
5. Record indicators, evidence, and response actions.

**Evidence:** Add screenshots, sanitized event details, and investigation notes under `evidence/` when available.

---

## Lab 02 — Network Reconnaissance

**Objective:** Generate authorized reconnaissance activity and identify it through network monitoring.

**Telemetry:** Security Onion network alerts and packet metadata.

**Investigation:**

1. Identify the source and destination systems.
2. Review timestamps and traffic patterns.
3. Determine which services were targeted.
4. Correlate network activity with endpoint logs.
5. Document the detection and recommended response.

---

## Lab 03 — Endpoint Threat Investigation

**Objective:** Investigate suspicious process or command activity on a monitored endpoint.

**Telemetry:** Wazuh endpoint telemetry and Windows event logs.

**Investigation:**

1. Identify the process, user, and host.
2. Review parent/child process relationships where available.
3. Check surrounding authentication and network events.
4. Assess whether the behavior matches a known attack technique.
5. Document containment and remediation recommendations.

---

## Investigation Template

### Incident Summary

- **Date:**
- **Host:**
- **User:**
- **Severity:**
- **Detection source:**

### Timeline

| Time | Event | Source | Significance |
|---|---|---|---|
| | | | |

### Indicators

- IP addresses:
- Hostnames:
- Users:
- Processes:
- Files / hashes:
- Domains:

### Analysis

Describe what happened, how it was detected, and how the evidence was correlated.

### Response

Document containment, eradication, recovery, and validation steps.

### Lessons Learned

Record detection gaps, tuning opportunities, and improvements for the next iteration.
