# L1 — Assisted Detection

## Classification

| Dimension | Value |
|---|---|
| **Level** | L1 |
| **Name** | Assisted Detection |
| **AI Decision Scope** | Surface alerts, provide basic prioritisation |
| **Human Role** | Investigate, decide, respond |
| **Proposed Auto. Action Rate** | 0% |

## Description

The AI assists human analysts by surfacing alerts, reducing noise (approximately 20–40%), and providing basic prioritisation signals. All investigation and response decisions remain with human analysts. The AI does not form hypotheses, recommend actions, or execute any response.

## Characteristic Technology

- AI-assisted SIEM with alert scoring
- NLP-based alert summarisation
- Basic threat intelligence correlation
- Prioritisation dashboards

## Governance Requirements

- Model tuning and monitoring for alert quality
- False positive / false negative tracking
- Analyst feedback mechanisms

## Classification Criteria

A system is classified as L1 if:
- AI surfaces and prioritises alerts but does not triage or enrich them
- All investigation decisions are human-initiated
- No automated response actions occur
- AI output is advisory only — human initiates all next steps

## Illustrative Market Examples

Based on publicly described capabilities as of April 2026:
- CrowdStrike Charlotte AI
- Microsoft Copilot for Security
- SentinelOne Purple AI
- Google SecOps Gemini

> The majority of current "AI SOC" products appear to operate at this level based on publicly described capabilities. Placement is illustrative, not a definitive assessment.

---

*Part of the [SOC Autonomy Framework](../README.md)*
