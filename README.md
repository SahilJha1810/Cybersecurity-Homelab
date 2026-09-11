# 🛡️ Cybersecurity SOC Homelab

> A hands-on cybersecurity home lab for SOC monitoring, threat detection, incident response, vulnerability assessment, and controlled adversary simulation.

## 🎯 Project Overview

This project documents the design and operation of an enterprise-style cybersecurity lab built with virtual machines and open-source security tooling.

The goal is not simply to deploy security tools, but to demonstrate an end-to-end SOC workflow:

**Attack → Telemetry → Detection → Investigation → Response → Lessons Learned**

## 🏗️ Environment

| System / Tool | Purpose |
|---|---|
| **Windows Server** | Active Directory, DNS, identity services |
| **Windows Client** | Domain endpoint and security telemetry |
| **Ubuntu Server** | Linux workload and log source |
| **Kali Linux** | Authorized attack simulation and security testing |
| **Wazuh** | SIEM, XDR, endpoint monitoring and alerting |
| **Security Onion** | Network security monitoring, IDS and packet analysis |

See the [architecture documentation](ARCHITECTURE.md) for the lab design and data flow.

## 🔍 Security Capabilities

### Security Monitoring

- Windows event monitoring
- Linux log collection
- Endpoint telemetry
- Network security monitoring
- Centralized alert triage

### Detection & Investigation

- Authentication anomaly investigation
- Suspicious process analysis
- Network reconnaissance detection
- Indicator-of-compromise analysis
- Endpoint/network event correlation

### Incident Response

- Alert validation
- Investigation timelines
- Containment planning
- Eradication and recovery documentation
- Detection tuning and lessons learned

## 🧪 Hands-On Labs

| Lab | Focus | Status |
|---|---|---|
| 01 | Authentication Monitoring | 📝 Documented |
| 02 | Network Reconnaissance | 📝 Documented |
| 03 | Endpoint Threat Investigation | 📝 Documented |

Detailed scenarios and an investigation template are available in [DETECTION-LABS.md](DETECTION-LABS.md).

## 📚 Documentation

- [Architecture](ARCHITECTURE.md) — components, data flow, and SOC workflow
- [Lab Setup](LAB-SETUP.md) — VM roles, network design, and deployment checklist
- [Detection Labs](DETECTION-LABS.md) — investigation scenarios and evidence template

## 🗺️ Roadmap

- [ ] Complete Active Directory deployment
- [ ] Deploy and tune Wazuh agents
- [ ] Configure Security Onion network visibility
- [ ] Build baseline SOC dashboards
- [ ] Add Windows authentication detections
- [ ] Add Linux detection scenarios
- [ ] Document attack-to-detection walkthroughs
- [ ] Map detections to MITRE ATT&CK techniques
- [ ] Add sanitized screenshots and investigation evidence
- [ ] Add incident-response case studies

## 🔐 Safety & Ethics

All offensive-security exercises in this repository are intended for systems that are owned by the lab operator or explicitly authorized for testing. The lab should remain isolated from production and personal networks.

Never commit passwords, API keys, private certificates, tokens, or other secrets to this repository.

## 💼 Portfolio Value

This repository is intended to demonstrate practical cybersecurity skills rather than tool installation alone. Each completed lab should show:

1. **What was tested**
2. **What telemetry was generated**
3. **How the activity was detected**
4. **How the alert was investigated**
5. **What response was taken**
6. **What could be improved**

That structure turns the homelab into a growing SOC portfolio and provides concrete evidence of hands-on security operations experience.

---

**Author:** Sahil Jha  
**Focus:** SOC Operations • Threat Detection • Incident Response • Cybersecurity Engineering
