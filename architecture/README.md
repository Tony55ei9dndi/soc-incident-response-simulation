# Architecture Overview

This project simulates a small-to-mid size SOC environment designed to detect and respond to common enterprise attack patterns.

The architecture prioritizes:
- Visibility over complexity
- Open-source tooling
- Clear separation of detection, analysis, and response

---

## High-level Architecture

The environment consists of the following components:

- **Endpoints**
  - Simulated Linux hosts generating normal and malicious activity

- **Network Layer**
  - Traffic monitored via Suricata and Zeek

- **Detection & SIEM**
  - Wazuh used for log aggregation, correlation, and alerting

- **Response Layer**
  - Analyst-driven response with documented playbooks
  - Limited automation to reduce blast radius

---

## Data Flow

1. Endpoint and network activity is generated
2. Logs and telemetry are collected by Wazuh agents
3. Network traffic is analyzed by Suricata and Zeek
4. Alerts are correlated and triaged
5. Response actions are executed based on severity

---

## Design Decisions

- Open-source tools were selected to mirror cost-conscious enterprise environments
- Manual decision points were preserved to reflect real SOC workflows
- Detection fidelity was prioritized over alert volume

---

## Assumptions & Limitations

- This is a controlled lab environment
- No production data is used
- Threats are simulated, not live adversaries

---

## Future Improvements

- SOAR-style response automation
- Threat intelligence enrichment
- Metrics for mean-time-to-detect (MTTD) and respond (MTTR)
