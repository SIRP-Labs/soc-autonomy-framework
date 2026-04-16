# L2 — Automated Triage

## Classification

| Dimension | Value |
|---|---|
| **Level** | L2 |
| **Name** | Automated Triage |
| **AI Decision Scope** | Triage, enrich, correlate, filter false positives |
| **Human Role** | Validate, investigate, respond |
| **Proposed Auto. Action Rate** | 0–10% |

## Description

The AI automatically triages incoming alerts — classifying severity, enriching indicators of compromise, correlating related events, and filtering false positives (50–80% noise reduction). Investigation recommendations may be generated but are not executed without human approval. The analyst receives a pre-worked case rather than a raw alert.

## Proposed Classification Metrics

| Metric | Proposed L2 Target |
|---|---|
| False Positive Reduction | 50–80% |
| Alert Enrichment Coverage | 90%+ of alerts enriched with context |
| Correlation Rate | Related events grouped automatically |
| Autonomous Action Rate | 0–10% (limited, low-risk only) |

## Governance Requirements

- Enrichment source validation and freshness monitoring
- Correlation rule quality management
- False positive tracking and model feedback loop
- Human review of automated triage classifications

## Classification Criteria

A system is classified as L2 if:
- AI automatically triages and enriches alerts without human initiation
- AI correlates related events and builds preliminary case context
- AI reduces false positives through automated filtering
- All investigation conclusions and response decisions remain human

## What Changes at L2 vs L1

At L1, the human analyst still processes each raw alert. At L2, the AI pre-processes alerts into enriched, correlated cases. The analyst works with structured, contextualised information rather than raw signals.

The key limitation of L2: the system follows predefined or learned patterns. It cannot reason about novel situations, form hypotheses about attacker intent, or recommend actions outside its training distribution.

## Illustrative Market Examples

Based on publicly described capabilities as of April 2026:
- Dropzone AI
- Intezer
- D3 Morpheus
- SOAR platforms with AI augmentation

> Placement is illustrative, not a definitive assessment.

---

*Part of the [SOC Autonomy Framework](../README.md)*
