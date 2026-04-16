# L0 — Manual SOC

## Classification

| Dimension | Value |
|---|---|
| **Level** | L0 |
| **Name** | Manual SOC |
| **AI Decision Scope** | None |
| **Human Role** | Everything |
| **Proposed Auto. Action Rate** | 0% |

## Description

All detection, investigation, and response decisions are made by human analysts. AI (if present) functions only as a data display layer — surfacing information without interpretation, prioritisation, or recommendation.

MTTD is entirely dependent on analyst availability, typically ranging from 4 to 24 hours for initial detection. Mean Time to Respond (MTTR) is measured in hours to days.

## Characteristic Technology

- Manual SIEM dashboards (rule-based alerting)
- Email-based alert notification
- Spreadsheet or ticketing-based case management
- Human-authored runbooks consulted manually

## Governance Requirements

- Standard IT security policies
- Analyst training and certification
- Shift coverage planning

## Classification Criteria

A system is classified as L0 if:
- No AI system makes or influences security decisions
- All alert triage is performed manually
- No automated enrichment or correlation is applied to alerts
- Response actions are exclusively human-initiated

## Limitations

- MTTD and MTTR scale linearly with analyst headcount
- Alert volume growth consistently outpaces hiring capacity
- Analyst burnout from repetitive manual triage
- Coverage gaps during off-hours and holidays

---

*Part of the [SOC Autonomy Framework](../README.md)*
