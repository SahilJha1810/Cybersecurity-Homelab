# SOC Cybersecurity Homelab Architecture

## Objective

This homelab is designed as a practical Security Operations Center (SOC) environment for learning and demonstrating security monitoring, threat detection, incident response, vulnerability assessment, and attack simulation.

## Core Components

| Component | Role |
|---|---|
| Windows Server | Active Directory / domain services |
| Windows Client | Endpoint telemetry and attack simulation target |
| Ubuntu Server | Linux workload and log source |
| Kali Linux | Authorized attack and penetration-testing workstation |
| Wazuh | SIEM, XDR, endpoint monitoring, alerting |
| Security Onion | Network security monitoring, packet analysis, IDS/NSM |

## High-Level Data Flow

```text
                         ┌──────────────────────┐
                         │    Kali Linux        │
                         │ Attack Simulation    │
                         └──────────┬───────────┘
                                    │
                                    ▼
┌─────────────────┐          ┌───────────────┐          ┌──────────────────┐
│ Windows Server  │─────────▶│    Network    │─────────▶│ Security Onion  │
│ Active Directory│          │   Telemetry   │          │ IDS / NSM / PCAP │
└────────┬────────┘          └───────────────┘          └──────────────────┘
         │
         │ endpoint logs
         ▼
┌─────────────────┐          ┌──────────────────┐
│ Windows Client  │─────────▶│      Wazuh       │
│ Endpoint Target │          │ SIEM / XDR / EDR │
└─────────────────┘          └────────┬─────────┘
                                      │
                                      ▼
                             ┌──────────────────┐
                             │ Alert Triage &    │
                             │ Incident Response │
                             └──────────────────┘
```

## Security Workflow

1. Build and isolate the lab network.
2. Configure identity and endpoint systems.
3. Install and configure Wazuh agents and monitoring.
4. Deploy Security Onion for network visibility.
5. Generate controlled attack activity from Kali Linux.
6. Collect and correlate endpoint and network telemetry.
7. Investigate alerts and identify indicators of compromise.
8. Document findings, response actions, and lessons learned.

> All attack simulations should be performed only against systems owned or explicitly authorized for testing.
