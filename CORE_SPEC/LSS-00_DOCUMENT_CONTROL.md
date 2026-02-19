# LSS-00: Document Control and Normative Hierarchy
**Status:** Draft
**Version:** 1.0.0-draft
**Canonical Language:** English (normative only)
**Last-Updated:** 2026-02-16

## 0.1 Purpose (Non-Normative)
This module defines the normative document hierarchy, change control, and interpretation rules for the Lovalis System Specification (LSS).

## 0.2 Normative Keywords (Normative)
The key words **MUST**, **MUST NOT**, **SHALL**, **SHALL NOT**, **SHOULD**, and **MAY** are to be interpreted as described in RFC 2119.

## 0.3 Document Set (Normative)
The Lovalis System Specification (LSS) SHALL consist of modular documents named `LSS-xx_*.md`.

## 0.4 Normative Hierarchy (Normative)
In case of inconsistency, the following precedence order SHALL apply:

1. **LSS (CORE_SPEC)** — the normative core specification
2. **Constitution / Legal Texts** — if explicitly referenced by LSS
3. **Compendium / Commentary / Guides** — non-normative unless explicitly stated
4. **Examples / Tutorials / Public Materials** — non-normative

If any non-core document conflicts with LSS, **LSS SHALL prevail**.

## 0.5 Compatibility with Translations (Normative)
Translations MAY be produced for commentary and public materials.

Translations SHALL NOT be considered normative unless explicitly ratified as an LSS module via the change-control process.

## 0.6 Change Control (Normative)
Any change to the LSS modules that affects:
- safety constraints,
- validation hierarchy,
- simulation horizon,
- governance structure,
- irreversibility rules,
- or auditability requirements

SHALL be treated as a **Core Amendment**.

Core Amendments SHALL require the governance process defined in **[LSS-07 §7.7]** (Hard Fork / Supermajority / Cooling-off / Re-validation).

Non-core editorial changes (spelling, formatting, cross-reference repairs) MAY be applied without Core Amendment, provided they do not change normative meaning.

## 0.7 Reference Format (Normative)
All normative cross-references SHALL use the format:

`[LSS-03 §3.2.1]`

A reference SHALL uniquely identify a section within a single module.

This specification formalizes the normative kernel of Lovalis v5.1+ (Eternity Edition lineage).

## Canonical Normative Source
The modular documents within the `CORE_SPEC/` directory constitute the sole canonical normative specification of Lovalis.

Any consolidated or overview documents outside this directory SHALL be considered non-normative summaries unless explicitly stated otherwise.
