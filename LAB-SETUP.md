# Lab Setup

## Lab Goals

The environment is intended to provide hands-on practice with:

- SOC monitoring and alert triage
- Windows and Linux log analysis
- Active Directory security
- Network security monitoring
- Vulnerability assessment
- Detection engineering
- Incident response
- Controlled adversary simulation

## Suggested Virtual Machines

| VM | Suggested Role |
|---|---|
| Windows Server | Domain Controller / Active Directory |
| Windows 10/11 | Domain-joined endpoint |
| Ubuntu | Linux server and application workload |
| Kali Linux | Security testing workstation |
| Wazuh | SIEM/XDR platform |
| Security Onion | Network security monitoring |

## Network Design

Use an isolated virtual network for the lab. Keep intentionally vulnerable systems and attack simulations separated from personal devices and production networks.

Example logical layout:

```text
                    LAB NETWORK
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
  Windows Server   Windows Client     Ubuntu Server
       AD/DC          Endpoint          Linux Host
        │                │                │
        └────────────────┼────────────────┘
                         │
                 Security Onion
                 Network Sensors
                         │
                         ▼
                      Wazuh
                   SIEM / XDR
                         ▲
                         │
                   Kali Linux
                Attack Simulation
```

## Initial Configuration Checklist

- [ ] Create an isolated lab network
- [ ] Deploy Windows Server
- [ ] Configure Active Directory and DNS
- [ ] Join Windows client to the domain
- [ ] Deploy Ubuntu server
- [ ] Deploy Wazuh
- [ ] Install Wazuh agents on endpoints
- [ ] Deploy Security Onion
- [ ] Configure network visibility
- [ ] Verify logs are reaching monitoring platforms
- [ ] Create baseline detections
- [ ] Document each lab exercise

## Operational Notes

Keep credentials, API keys, private IP details that expose your real network, and other secrets out of GitHub. Use placeholders in documentation and store sensitive configuration locally or in a secrets manager.
