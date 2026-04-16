# Contributing to the SOC Autonomy Framework

The SAF is a living framework. We welcome contributions from security researchers, SOC practitioners, vendors, and academics.

## What We're Looking For

### 1. Empirical Validation Data
The proposed operational metrics (autonomous action rates, MTTD/MTTR targets) are starting points based on operational experience. We need real-world data to validate or refine them.

Submit via issue or PR:
- Measured autonomous action rates from production SOC deployments
- MTTD/MTTR benchmarks at specific SAF levels
- False positive reduction rates at L2
- Investigation coverage metrics at L3/L4

### 2. Level Definition Refinements
If you believe a level definition is ambiguous, too broad, or missing important criteria, open an issue with:
- The specific text you believe needs refinement
- Your proposed change
- Your reasoning (operational experience, research, or both)

### 3. Classification Examples
Real-world or hypothetical examples of products/systems classified against the SAF, with reasoning. These help practitioners apply the framework.

### 4. Governance Requirement Specifications
Particularly for L3 and L4 — concrete, implementable governance specifications that could serve as reference implementations of the requirements described in the framework.

### 5. Research Pointers
Papers or datasets relevant to the open research challenges in Section 7 of the paper:
- Neurosymbolic security reasoning
- Adversarially robust confidence calibration
- Federated collective intelligence
- Formal governance specification
- End-to-end SOC benchmarks

## How to Contribute

1. **Issues** — For discussion, questions, and proposals
2. **Pull Requests** — For concrete changes to framework text
3. **Discussions** — For broader conversations about autonomy levels and SOC AI

## Guidelines

- Be specific. "L3 is unclear" is not actionable. "The L3 definition does not specify whether automated IOC blocking counts as a low-risk action" is.
- Cite evidence where possible. Operational experience is valid evidence.
- Vendor contributions are welcome but must be clearly attributed. Vendor-supplied data will be labelled as such.
- The framework is vendor-neutral by design. PRs that modify level definitions to advantage specific products will not be merged.

## Code of Conduct

Be direct, be rigorous, and assume good faith. The goal is a better framework, not winning arguments.

---

*Questions? Open an issue or contact faiz@sirp.io*
