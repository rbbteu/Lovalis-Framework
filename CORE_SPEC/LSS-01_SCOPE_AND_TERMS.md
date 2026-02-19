# LSS-01: Scope and Terms
**Status:** Draft
**Version:** 1.0.0-draft
**Canonical Language:** English (normative only)

## 1.1 Scope (Normative)
LSS defines a structural governance and validation framework for long-horizon stability across:

- Environmental Integrity (ENV)
- Human Sentient Stability (SH)
- Technology Subordination (D)

LSS applies to all Lovalis implementations, simulations, and certification claims.

## 1.2 Non-Goals (Normative)
LSS SHALL NOT prescribe:
- cultural content, ideology, religion, or aesthetic doctrine;
- a required form of government beyond the minimal constraints defined in LSS;
- a “maximized happiness” objective function.

## 1.3 Core Concepts (Non-Normative)
Lovalis assumes unmanaged systems tend to drift toward technology-primacy and short-horizon optimization. LSS encodes constraints to prevent such drift via multi-layer validation and long-horizon simulation.

## 1.4 Terms and Definitions (Normative)

## 1.4.1 Entity Levels
**Cell:** The smallest functional unit capable of closed accounting for energy, water, and material flows.

**Cluster:** A functional infrastructure unit composed of one or more Cells, operating under a cluster-local governance system.

**Federation:** A regional association of Clusters for coordination and peer review. Federations SHALL NOT act as a global sovereign over clusters unless LSS explicitly permits it.

**Intercluster Layer:** The global coordination layer. The intercluster layer SHALL NOT override cluster bottleneck failures. See [LSS-02 §2.3].

## 1.4.2 Validation Layers
**ZVF:** Zangen Validation Framework (historical name), equivalent to the **Validation Layer Framework (VLF)** as defined in [LSS-03].

**ZVF-S:** Stability Layer (veto-capable).

**ZVF-E:** Engineering Layer (binding, non-veto over ZVF-S).

**ZVF-C:** Cultural Layer (non-binding, non-veto).

## 1.4.3 Environmental Integrity
**ENV:** Environmental Integrity as defined in [LSS-04].

**Domain:** One of {C, WB, N, B} as defined in [LSS-04 §4.2].

**Pressure (P):** Extraction, emission, or degradation per unit time.

**Regeneration (R):** Renewal or assimilation capacity per unit time.

**Regeneration Ratio (ρ):** ρ = P/R.

**Irreversibility Marker (K):** A domain/level threshold condition indicating non-compensable risk. See [LSS-04 §4.6].

## 1.4.4 Human Sentient Stability
**SH:** Core human sentient stability as defined in [LSS-05].

**Avoidable Burden:** Harm that is preventable under feasible, non-destructive policy and infrastructure constraints.

## 1.4.5 Technology Subordination
**D:** Technology Subordination as defined in [LSS-06].

## 1.4.6 Gates and Horizon
**Gate:** A 25-year evaluation checkpoint during a 7-generation simulation horizon. See [LSS-09 §9.2].

**Horizon:** Minimum 7 generations, currently 175 years. See [LSS-09 §9.1].

## 1.5 Claims and Labeling (Normative)
Any claim that an artifact, policy, technology, or organization is “Lovalis-compliant” or “Lovalis-certified” MUST reference:
- the exact LSS version;
- the simulation horizon used;
- and the modules used for evaluation.

Unsupported claims SHALL be considered invalid.

## 1.6 Normalization and Scoring Requirements (Normative)

Where LSS uses a “normalized score” or “index” that influences validity (e.g., ENV_primary, SH_primary, D_primary):

1. Scores MUST be defined on the closed interval [0,1].
2. Score = 0 SHALL represent a FAIL state for the evaluated element.
3. Score mappings MUST be monotonic in the direction of risk (i.e., increased risk SHALL NOT increase the score).
4. The scoring function, thresholds, and data sources MUST be declared in the evaluation report.
5. Sensitivity of results to scoring assumptions SHOULD be provided where uncertainty is non-trivial.

Scoring SHALL NOT be used to override bottleneck failure conditions.
