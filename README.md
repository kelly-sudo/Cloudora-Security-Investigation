# Cloudora — Identity Compromise Investigation

**SOC / Blue Team Portfolio Project**  
Microsoft Sentinel · Microsoft Entra ID · KQL · MITRE ATT&CK

## Overview

A simulated SOC investigation into suspected compromise of the Cloudora CEO's Microsoft Entra ID account.

The investigation focuses on:

- validating the suspicious sign-in and determining whether the account was compromised,
- reconstructing the incident timeline,
- identifying attacker activity and persistence,
- determining the scope of the incident,
- mapping observed behaviour to MITRE ATT&CK,
- documenting findings and recommended response actions.

The project uses synthetic data from the Cloudora training scenario (MyFirstHack).

## Scenario

**Client:** Cloudora, fictional B2B HR software company  
**Ticket:** `CLD-0001 — Suspicious sign-in activity: daniel.reeve@cloudora.io`  
**Priority:** P1  
**Initial alert:** suspicious sign-in from Lagos, Nigeria while the CEO was expected to be in London.

## Investigation

The investigation is performed using Microsoft Sentinel and KQL against:

- `cloudora_signin_logs.csv` — Entra ID sign-in logs
- `cloudora_audit_logs.csv` — audit events

The investigation follows the workflow:

```text
Triage
  → Authentication analysis
  → Timeline reconstruction
  → Persistence investigation
  → Scope analysis
  → MITRE ATT&CK mapping
  → Incident reporting
```

All conclusions in the final report are supported by investigation evidence and referenced queries.

## Repository structure

```text
.
├── incidents/
│   └── CLD-IR-0001.md
├── queries/
│   └── *.kql
└── evidence/
    └── *.png
```

| Directory | Contents |
|---|---|
| `incidents/` | Final incident report |
| `queries/` | KQL investigation queries |
| `evidence/` | Supporting screenshots and evidence |

## Skills demonstrated

**Security Operations:** alert triage, account takeover investigation, threat hunting, incident scoping, IOC analysis, incident response.

**Microsoft Security:** Microsoft Sentinel, Entra ID sign-in logs, audit logs.

**Detection & Analysis:** KQL, authentication analysis, timeline reconstruction, persistence investigation, MITRE ATT&CK.

**Reporting:** evidence-based findings, technical documentation, remediation recommendations.

## Report

[View the full incident report](./incidents/CLD-IR-0001.md)

## Disclaimer

This is a fictional training scenario using synthetic data. No real customer, production, or credential data is included.

## Author

Radosław Huppert
