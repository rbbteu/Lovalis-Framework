# LSS-09: Simulation Requirements
**Status:** Draft
**Version:** 1.0.0-draft
**Canonical Language:** English (normative only)

## 9.1 Horizon Requirement (Normative)
All structural evaluations under LSS SHALL simulate a minimum horizon of:

- Seven (7) generations
- Currently defined as 175 years

Shorter simulation horizons SHALL NOT be considered LSS-compliant.

## 9.2 Gate Structure (Normative)
The simulation SHALL include evaluation Gates at 25-year intervals.

Gate sequence:
t0, t25, t50, t75, t100, t125, t150, t175

At each Gate, ENV, SH, and D constraints SHALL be evaluated.

## 9.3 Baseline Scenario Requirement (Normative)
Simulations SHALL include at minimum:

1. Baseline scenario (intended operation).
2. Stress scenario (resource scarcity or supply disruption).
3. Shock scenario (unexpected infrastructure failure or environmental shift).
4. Governance stress scenario (institutional instability).

Failure under any required scenario SHALL invalidate compliance.

## 9.4 Irreversibility Testing (Normative)
Simulations SHALL explicitly test for:

- Domain-specific K-markers (see [LSS-04 §4.6]);
- Structural lock-in of monopoly control (see [LSS-06 §6.3]);
- Long-term SH regression under demographic change (see [LSS-05]).

Irreversible failure SHALL immediately terminate compliance evaluation.

## 9.5 Model Transparency (Normative)
Simulation models SHALL:

- Document assumptions;
- Provide parameter sensitivity analysis;
- Identify uncertainty bounds;
- Disclose data provenance.

Opaque simulation models SHALL NOT be accepted.

## 9.6 Reproducibility Requirement (Normative)
Simulation inputs, model structure, and parameter sets SHALL be archived in a reproducible form.

Independent review clusters MUST be able to reproduce simulation results within declared tolerance margins.

## 9.7 Extended Simulation (Normative)
Extended Simulation SHALL be required if:

- Drift triggers are activated under [LSS-04 §4.9], [LSS-05 §5.7], or [LSS-06 §6.8];
- Peer Review mandates extension under [LSS-08];
- A Core Amendment is proposed under [LSS-07 §7.7].

Extended Simulation SHALL include amplified stress parameters and worst-case bounding.

## 9.8 Simulation Output Requirements (Normative)
Simulation reports SHALL include:

- Time-series for ρ(e,d,t);
- SH indicator trajectories;
- D index trajectories;
- Gate-by-Gate pass/fail classification;
- Irreversibility marker status;
- Assumption sensitivity impact.

## 9.9 Prohibition of Cosmetic Compliance (Normative)
Temporary improvements that mask long-term degradation SHALL NOT be accepted.

Front-loaded resource extraction followed by late collapse SHALL invalidate compliance, even if early Gates pass.

## 9.10 Tolerance Declaration Requirement (Normative)
Tolerance margins for reproducibility:

1. MUST be declared per ENV domain, SH indicator, and D index.
2. MUST include justification for chosen tolerance levels.
3. MUST disclose impact of tolerance variation on validity classification.
