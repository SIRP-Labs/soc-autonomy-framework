# SOC Autonomy Framework (SAF)

> A vendor-neutral classification system for degrees of security operations autonomy.
> Analogous to SAE J3016 for automated driving — applied to the autonomous SOC.

**Author:** Faiz Shuja, SIRP Labs  
**Paper:** [The Autonomous SOC Manifesto](paper/Autonomous-SOC-Manifesto-Faiz-Shuja.pdf)  
**Published:** April 2026 | https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6641798  
**Web:** [sirp.io/manifesto](https://sirp.io/manifesto)

---

## The Framework

The SOC Autonomy Framework defines **six levels** of security operations autonomy (L0–L5), each characterised by four dimensions:

| Dimension | Description |
|---|---|
| **Decision Scope** | What categories of security decisions the AI makes without human initiation |
| **Autonomous Action Rate** | % of incidents resolved end-to-end without human intervention |
| **Governance Requirements** | Oversight mechanisms required at each level |
| **Human Role** | Nature of human involvement at each level |

> A system's SAF level is determined by the **lowest** dimension at which it operates. A system with L3-level decision scope but L1-level governance is classified as L1.

---

## Levels at a Glance

| Level | Name | AI Decision Scope | Human Role | Auto. Action Rate |
|---|---|---|---|---|
| L0 | Manual SOC | None | Everything | 0% |
| L1 | Assisted Detection | Surface, prioritise alerts | Investigate, decide, respond | 0% |
| L2 | Automated Triage | Triage, enrich, correlate, filter FPs | Validate, investigate, respond | 0–10% |
| L3 | Conditional Autonomy | Investigate, recommend, execute low-risk | Approve high-impact, supervise | 20–50% |
| L4 | High Autonomy (Self-Driving SOC) | Full lifecycle within governed boundaries | Monitor, exceptions, policy updates | 70–90% |
| L5 | Full Autonomy | Entire SOC lifecycle | Set policy only | 99–100% |

> **Note:** Autonomous action rates are proposed operational targets based on the author's operational experience and available industry data. They are not industry-established benchmarks.

---

## Level Specifications

Detailed specifications for each level, including governance requirements, classification metrics, and representative characteristics:

- [L0 — Manual SOC](levels/L0-manual.md)
- [L1 — Assisted Detection](levels/L1-assisted-detection.md)
- [L2 — Automated Triage](levels/L2-automated-triage.md)
- [L3 — Conditional Autonomy](levels/L3-conditional-autonomy.md)
- [L4 — High Autonomy (Self-Driving SOC)](levels/L4-high-autonomy.md)
- [L5 — Full Autonomy](levels/L5-full-autonomy.md)

---

## Critical Transitions

### The Reasoning Gap (L2 → L3)
The most significant architectural leap. L2 systems follow predefined or learned logic through pattern matching. L3 systems must **reason** about novel situations — correlating evidence never correlated before, forming hypotheses about attacker intent, recommending actions outside any playbook.

Requires: (a) contextual reasoning, (b) causal inference, (c) uncertainty quantification.

### The Trust Threshold (L3 → L4)
Primarily a **trust** challenge. Moving from "human approves high-impact actions" to "system acts autonomously within governance boundaries" requires:

- **Calibrated confidence** — tightly calibrated against measured accuracy
- **Governed boundaries** — formal policy specifications enforced architecturally
- **Auditable decision traces** — evidence-bound, policy-validated action paths
- **Graceful degradation** — recognition of operation outside competence

### The L5 Position
We include L5 for taxonomic completeness but take the explicit normative position that L5 raises fundamental questions about the appropriate role of human moral reasoning in security. **The goal of this framework is L4 — not L5.**

---

## Why This Exists

The cybersecurity industry currently has no shared vocabulary for classifying degrees of SOC autonomy. This creates:

1. **Vendor confusion** — "AI-powered SOC" claims range from simple alert correlation to autonomous incident response with no standard for comparison
2. **Misaligned expectations** — buyers cannot specify what level of autonomy they need or what governance must accompany it
3. **Unfocused research** — literature is heavily weighted toward detection and triage, with minimal formal treatment of autonomous decision-making

SAF is the cybersecurity equivalent of what SAE J3016 did for self-driving cars.

---

## Related Projects

| Repo | Description |
|---|---|
| [saf-benchmark](https://github.com/sirp-labs/saf-benchmark) | Open benchmark suite for measuring SOC autonomy level |
| [saf-classifier](https://github.com/sirp-labs/saf-classifier) | CLI tool to classify a SOC product's autonomy level |

---

## Citation

```bibtex
@article{shuja2026autonomoussoc,
  title     = {The Autonomous SOC Manifesto: A Framework for Classifying
               Levels of Security Operations Autonomy},
  author    = {Shuja, Faiz},
  year      = {2026},
  month     = {April},
  institution = {SIRP Labs},
  url       = {https://sirp.io/manifesto},
  note      = {ORCID: 0009-0008-3106-2972}
}
```

---

## Contributing

We welcome contributions from researchers, practitioners, and vendors. See [CONTRIBUTING.md](CONTRIBUTING.md).

**Ways to contribute:**
- Propose refinements to level definitions
- Submit empirical data that validates or challenges the proposed metrics
- Add governance requirement specifications
- Share real-world classification examples

---

## License

The SOC Autonomy Framework specification is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to share and adapt this framework for any purpose, provided you give appropriate credit.

---

*Built by [SIRP Labs](https://sirp.io) — creators of OmniSense, the Self-Driving SOC platform.*
