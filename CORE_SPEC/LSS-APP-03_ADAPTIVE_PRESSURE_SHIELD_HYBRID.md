# LSS-APP-03: Adaptive Pressure Shield (Hybrid Model)

**Status:** Draft  
**Scope:** Normative  
**Subordination:** Subordinate to LSS-APP-02.  
**Purpose:** Provides a hybrid (rule-based + adaptive) mechanism that modulates communication to reduce pressure, without altering validation outcomes.

## 1. Non-Interference Constraint

The Pressure Shield SHALL:
- influence only presentation, tone, and timing,
- SHALL NOT alter ENV/SH/D evaluation logic,
- SHALL NOT reclassify STOP/FRAGILE/WARN/VALID outcomes.

Truth remains invariant; delivery becomes gentler.

## 2. Layer 1: Deterministic Triggers

The shield SHALL activate ""Context Mode"" if any trigger is met:
- >= 3 STOP or FRAGILE outcomes within 24h, OR
- SH exceeds a defined threshold in 3 consecutive interactions, OR
- >= 5 decisions within 60 minutes.

Triggers SHALL NOT be displayed as counts to the user.

## 3. Layer 2: Adaptive Weighting

The shield MAY compute an internal pressure index from:
- STOP/FRAGILE density (time-weighted),
- SH intensity and trend (rising/falling),
- interaction rate (decision cadence),
- reversibility class (if available).

The pressure index:
- SHALL be internal only,
- SHALL NOT be displayed as a score,
- SHALL not be used to change validation.

## 4. Behavioral Output (Presentation Rules)

When active, the shield SHALL:
- reduce alarm tone,
- encourage pacing,
- offer ""pause"" as an option,
- avoid ""should"" / ""must"" language.

Example (compliant):
> ""Today there seems to be a lot of movement in the system. Would you like to pause for a moment?""

## 5. Frequency Limits

The shield SHALL NOT:
- prompt context messages on two consecutive days,
- exceed 3 activations per week,
- activate within 30 minutes of app start (unless explicitly requested by user).

## 6. Disable-ability

A user-facing setting SHALL exist:
- ""Contextual slowing hints"" (default ON),
- disabling SHALL NOT reduce other functionality,
- disabling SHALL NOT trigger confirmation pressure.

## 7. Auditability (Local)

When the shield activates, the application SHOULD log locally:
- activation timestamp,
- which trigger category fired (not counts),
- which presentation template was used.

This log SHALL be deletable by the user.
