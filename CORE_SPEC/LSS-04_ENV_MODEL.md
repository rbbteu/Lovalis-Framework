# LSS-04: Environmental Integrity (ENV) Model
**Status:** Draft
**Version:** 1.0.0-draft
**Canonical Language:** English (normative only)

## 4.1 Purpose (Non-Normative)
This module defines the Environmental Integrity (ENV) model, including domain structure, regeneration ratios, irreversibility markers, and drift control mechanisms.

## 4.2 Stability Domains (Normative)
ENV SHALL be evaluated across the following domains:

- C  — Climate & Energy Stability
- WB — Water & Soil Regeneration
- N  — Nutrient & Chemical Cycles
- B  — Biosphere Functional Integrity

The domain set SHALL be:

D = {C, WB, N, B}

## 4.3 Entity-Level Evaluation (Normative)
For each entity level e ∈ {Cell, Cluster, Federation, Intercluster}
and each domain d ∈ D,
the regeneration ratio SHALL be defined as:

ρ(e,d,t) = P(e,d,t) / R(e,d,t)

Where:
- P = Pressure (extraction, emission, degradation per unit time)
- R = Regeneration capacity per unit time

## 4.4 Gate Condition (Normative)
At each Gate (see [LSS-09 §9.2]):

ρ(e,d,t_gate) SHALL satisfy:

ρ(e,d,t_gate) ≤ 1

for all entity levels e and domains d.

If any ρ(e,d,t_gate) > 1,
ENV SHALL fail at that entity level.

## 4.5 Temporal Continuity Constraint (Normative)
Short-term compliance SHALL NOT compensate for long-term exceedance.

Transient exceedance MAY only occur if:
- Explicitly modeled,
- Bounded,
- And followed by measurable restoration within the same Gate cycle.

## 4.6 Irreversibility Markers (K) (Normative)
Each domain d at each entity level e SHALL define one or more Irreversibility Markers K(e,d,t).

Triggering a K-marker SHALL result in immediate ENV failure.

Irreversible damage SHALL NOT be offset by improvements in other domains.

## 4.7 ENV Primary Score (Normative)
ENV_primary(t) SHALL be defined as min_{e∈EntityLevels, d∈D} score(e,d,t).

ENV_primary(t) = min(score(e,d,t))

If ENV_primary(t) = 0, the evaluated system SHALL be invalid.

## 4.8 ENV Health Index (Normative)
An auxiliary ENV_health(t) MAY be calculated as a weighted mean of normalized domain scores.

ENV_health SHALL NOT override ENV_primary bottleneck logic.

## 4.9 Progressive Drift Escalation (Normative)
If for any (e,d):

ρ(e,d,t_gate) ≥ 0.9 for two consecutive Gates:
- Transparency requirements SHALL increase.
- Probability of Peer Review SHALL increase (see [LSS-08]).

If ρ ≥ 0.9 for three consecutive Gates:
- Extended simulation SHALL be mandatory.

If ρ ≥ 0.9 for four consecutive Gates:
- Import thresholds SHALL be reduced as defined in [LSS-10].

## 4.10 Autarky and Import Constraint (Normative)
Clusters SHALL operate under regenerative autonomy by default.

Import dependency MAY be permitted only if:
1. Local regeneration is physically unachievable;
2. Supplying entity remains ENV-compliant;
3. Import share does not cause upstream ρ exceedance;
4. A restoration-to-autonomy plan exists.

## 4.11 Reporting Requirements (Normative)
ENV evaluation reports SHALL include:
- ρ values per domain and entity level;
- K-marker definitions and status;
- Drift classification;
- Simulation assumptions;
- Data provenance and measurement methods.


## 4.12 Domain Score Interface Requirements (Normative)
Domain score(e,d,t):

1. MUST be a monotonic function of ρ(e,d,t).
2. MUST collapse to 0 if any Irreversibility Marker K(e,d,t) is triggered.
3. MUST be defined on [0,1] per [LSS-01 §1.6].
4. MUST disclose formula, thresholds, and data sources in evaluation reports.
