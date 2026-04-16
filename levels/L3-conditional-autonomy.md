# L3 — Conditional Autonomy

## Classification

| Dimension | Value |
|---|---|
| **Level** | L3 |
| **Name** | Conditional Autonomy |
| **AI Decision Scope** | Investigate, recommend, execute low-risk actions |
| **Human Role** | Approve high-impact actions, supervise |
| **Proposed Auto. Action Rate** | 20–50% |

## Description

The AI investigates alerts end-to-end, correlates evidence across data sources, forms hypotheses about attacker intent, and recommends response actions. Low-risk actions (e.g., blocking an IP, quarantining a file) may execute automatically within defined boundaries. High-impact actions (e.g., isolating a production server, resetting credentials) require human approval.

Every recommendation includes a full reasoning chain — the AI must be able to explain why it reached its conclusion and what evidence it used.

## Proposed Classification Metrics

| Metric | Proposed L3 Target |
|---|---|
| Autonomous Action Rate | 20–50% |
| MTTD Improvement | 60–80% reduction vs. L0 baseline |
| MTTR Improvement | 50–70% reduction vs. L0 baseline |
| Investigation Coverage | 80–95% of alerts receive automated investigation |
| Explainability Rate | 100% of recommendations include reasoning chain |

> These are proposed operational targets, not established benchmarks.

## Governance Requirements

- **Confidence thresholds** — minimum confidence score required before autonomous execution
- **Auditable decision traces** — every autonomous action logged with full evidence chain
- **Action boundary definitions** — explicit policy specifying which action types may execute autonomously
- **Continuous accuracy monitoring** — ongoing measurement of investigation quality and false positive rate
- **Human escalation protocol** — defined criteria and SLA for escalating to human analyst

## What Changes at L3 vs L2

L2 systems follow predefined or learned logic through pattern matching. L3 systems must **reason** about novel situations.

This requires:

**(a) Contextual reasoning** — the system understands the organisational environment: which assets are critical, what constitutes normal behaviour for this specific organisation, what the current threat landscape is.

**(b) Causal inference** — the system distinguishes correlation from causation, forming directional hypotheses about attacker intent rather than simply clustering related events.

**(c) Uncertainty quantification** — the system maintains calibrated confidence in its own conclusions and communicates what it does not know alongside what it does know.

## The L2→L3 Boundary: The Reasoning Gap

This is the hardest architectural leap in the SAF. It is not achievable through playbook expansion alone. It requires:

- Large language models or equivalent reasoning capability for natural language security analysis
- A persistent knowledge representation of the organisation's environment (knowledge graph, RAG, or equivalent)
- A mechanism for forming and testing hypotheses against evidence
- A calibrated confidence model that distinguishes "I am certain" from "I am inferring"

## Illustrative Examples

- SIRP OmniSense is designed toward L3, with architecture targeting L4 (see paper Section 5)
- Prophet Security describes autonomous investigation capabilities consistent with aspects of L3

> Verified L3 operation requires independent measurement against the metrics above. Public claims of L3 without measurement should be treated as aspirational.

---

*Part of the [SOC Autonomy Framework](../README.md)*
