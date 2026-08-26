# L4 — High Autonomy (Self-Driving SOC)

## Classification

| Dimension | Value |
|---|---|
| **Level** | L4 |
| **Name** | High Autonomy / Self-Driving SOC |
| **AI Decision Scope** | Full incident lifecycle within governed boundaries |
| **Human Role** | Monitor, handle exceptions, update policy |
| **Proposed Auto. Action Rate** | 70–90% |

## Description

The AI handles the complete detection-to-response lifecycle for the majority of incidents without requiring human approval at each step. Humans define governance policy, monitor system performance, handle escalated exceptions, and update boundaries as the threat landscape evolves. The system acts — humans oversee.

**No system has achieved independently verified L4 in production as of April 2026.**

## Proposed Classification Metrics

| Metric | Proposed L4 Target |
|---|---|
| Autonomous Action Rate | 70–90% |
| MTTD | Near real-time (seconds to minutes) |
| MTTR | Minutes for automated incidents; hours for complex cases |
| Investigation Coverage | 99%+ of alerts receive automated investigation |
| Human Escalation Rate | <10% of incidents |
| Confidence Calibration | Tightly calibrated against measured accuracy |
| Confidence Resolution | Non-trivial: selective risk at operating coverage materially below full-coverage risk ([MEASUREMENT.md](../MEASUREMENT.md)) |

> These are proposed operational targets, not established benchmarks.

## Governance Requirements

L4 requires significantly more rigorous governance than L3:

- **Comprehensive governance policy framework** — formal, machine-enforceable policies specifying action boundaries, escalation criteria, and prohibited actions
- **Real-time audit logging** — immutable, complete audit trail of every autonomous action with full reasoning chain
- **Confidence-gated execution** — architectural enforcement of confidence thresholds (not prompt-level), with the threshold set **per action class** from its loss asymmetry, not one value for the system ([MEASUREMENT.md](../MEASUREMENT.md) §3)
- **Regular adversarial testing** — systematic testing of the system's response to novel attack patterns and adversarial inputs
- **Formal boundary enforcement** — governance policies enforced at the architecture level, not through model instruction
- **Graceful degradation protocol** — defined behaviour when the system operates outside its competence envelope

## The L3→L4 Boundary: The Trust Threshold

The transition from L3 to L4 is primarily a **trust** challenge, not a capability challenge. The system may already be capable of making correct autonomous decisions for the majority of incidents. The question is whether the governance architecture is robust enough to trust it to act without per-action human approval.

This requires four properties:

**(a) Calibrated, discriminating confidence** — The system's stated confidence must be empirically accurate (if it says 95%, it is wrong ~5% of the time) **and must discriminate its hard cases from its easy ones**. Calibration alone is insufficient: a system reporting one honest confidence value on every case is perfectly calibrated and impossible to threshold — it can act on everything or nothing, never on only what it is good at. The formal requirement is non-trivial **resolution** (see [MEASUREMENT.md](../MEASUREMENT.md) §1), evidenced by a risk–coverage curve rather than an accuracy point estimate. Systematic overconfidence at L4 produces autonomous errors at scale; non-discriminating confidence produces them at *full* scale.

**(b) Governed boundaries** — Action boundaries must be specified with sufficient precision for machine enforcement. "Don't take high-impact actions" is not a governed boundary. "Do not execute any action affecting more than N assets or impacting availability of Tier-1 systems without human approval" is.

**(c) Auditable decision traces** — Every autonomous action must produce a complete, evidence-bound, policy-validated reasoning trace that allows a human auditor to reconstruct exactly why the system acted as it did.

**(d) Graceful degradation** — The system must recognise when it is operating outside its competence — novel attack patterns, ambiguous evidence, out-of-scope situations — and escalate appropriately rather than proceeding with false confidence.

---

*Part of the [SOC Autonomy Framework](../README.md)*
