# L5 — Full Autonomy

## Classification

| Dimension | Value |
|---|---|
| **Level** | L5 |
| **Name** | Full Autonomy |
| **AI Decision Scope** | Entire SOC lifecycle |
| **Human Role** | Set policy only |
| **Proposed Auto. Action Rate** | 99–100% |

## Description

The AI handles the complete security operations lifecycle — detection, investigation, decision, response, and documentation — without human approval for any individual action. Humans define high-level policy; the system executes everything within that policy envelope.

## Normative Position

**The SOC Autonomy Framework takes the explicit normative position that L5, while potentially technically achievable, is not a desirable target.**

Security decisions involve:
- **Proportional response judgments** — determining whether a response is proportionate to a threat requires contextual moral reasoning
- **Privacy considerations** — autonomous response actions may affect individuals whose privacy deserves human consideration
- **Business impact assessments** — the collateral damage of aggressive response actions requires human judgment about acceptable risk
- **Moral reasoning about acceptable collateral impact** — machines should not make these decisions unilaterally

> *"Autonomy is not about automating everything. It is about knowing what should never be automated."*

The goal of this framework is **L4 — not L5**. The Self-Driving SOC is one where AI handles the operational majority while humans retain authority over decisions requiring moral and strategic judgment. This is not a limitation. It is a design principle.

## Why L5 Is Included

L5 is included for **taxonomic completeness** — the same reason SAE J3016 includes Level 5 for fully driverless vehicles. Having a defined ceiling makes the framework complete and gives researchers and regulators a reference point for discussing full automation risks.

## Status

L5 is **theoretical** as of April 2026. No production deployment exists or is being actively pursued by any known vendor.

---

*Part of the [SOC Autonomy Framework](../README.md)*
