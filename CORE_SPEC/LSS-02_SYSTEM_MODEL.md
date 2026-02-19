# LSS-02: System Model and Fractal Responsibility
**Status:** Draft
**Version:** 1.0.0-draft
**Canonical Language:** English (normative only)

## 2.1 Fractal Responsibility Principle (Normative)
Compliance with LSS MUST be satisfied at all entity levels defined in [LSS-01 §1.4.1].

No global compensation SHALL legitimize local degradation.

## 2.2 Bottleneck Validity (Normative)
System validity SHALL be bottleneck-dominated.

Let:
- ENV_primary(t) be defined in [LSS-04 §4.7],
- SH_primary(t) be defined in [LSS-05 §5.4],
- D_primary(t) be defined in [LSS-06 §6.4].

Then the overall validity at time t SHALL be:

`VALID(t) = min(ENV_primary(t), SH_primary(t), D_primary(t))`

If VALID(t) = 0 at any time, the evaluated system SHALL be invalid.

## 2.3 Sovereignty Boundaries (Normative)
Clusters SHALL be sovereign for local governance decisions within LSS constraints.

Federations and the Intercluster Layer:
- MAY coordinate data exchange, modeling, and emergency support;
- SHALL NOT override cluster-level bottleneck failures;
- SHALL NOT force structural changes absent the amendment process in [LSS-07 §7.7].

## 2.4 Autarky Default (Normative)
Clusters SHALL be designed for regenerative autonomy by default.

Import dependency MAY be permitted only under the exceptions defined in [LSS-04 §4.10] and [LSS-10 §10.3].
