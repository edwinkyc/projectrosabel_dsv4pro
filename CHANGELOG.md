# Changelog

All notable changes to this project are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project uses [Semantic Versioning](https://semver.org/) adapted for
a specification document:

- **Major** (X.0): changes that alter required behavior or break compatibility
  with existing deployments
- **Minor** (x.Y): new sections, new capabilities, or non-breaking additions
- **Patch** (x.y.Z): clarifications, typo fixes, wording improvements with no
  behavioral change



## [2.1] - [10 September 2026]

- Reconciles absolute clinical-action prohibitions with narrowly permitted,
  host-approved draft-saving and communication integrations.
- Separates source provenance, source checking, clinical applicability,
  task completeness, and action outcome.
- Introduces component-wise prerequisite gates with explicit blocked states.
- Introduces dependency-bound revision of conclusions, drafts, and approvals.
- Binds pending approval to relevant evidence and policy versions as well
  as patient, encounter, action, content, and destination.
- Defines receipt-bound action states, including unknown outcomes.
- Prevents educational labels from bypassing substantive safety restrictions.
- Replaces unconditional tool-result precedence with scope- and
  provenance-aware reconciliation.
- Clarifies safe support following clinical disagreement.
- Adds bounded recovery, context-loss handling, and model-version awareness.
- Adds reference procedures and synthetic behavioral tests.
- Separates prompt-directed behavior from host-enforced controls.
  

## [2.0] - [9 September 2026]

- **Non-negotiables** section: six absolute rules that hold regardless of
  user role, urgency, or instruction source
- **Priority conflict resolution**: numbered priority list with explicit
  tie-breaking rule ("lower number wins") and requirement to surface
  conflicts rather than resolve them silently
- **Outcome reporting** standard: claims about checks require observed
  checks; failed steps reported in the first sentence of results
- **Conversation management**: rules for corrections, disagreement, scope
  changes, pressure, and concision under stress
- **Medication halt conditions**: explicit list of conditions that block
  executable dosing output (missing weight, renal function, unverified
  sources, pediatric/chemo regimens without population-specific references)
- **Refusal style** standard: decline the unsafe element only, one sentence
  of rationale, always attach the nearest safe alternative
- **Self-correction** requirements: explicit flagging of earlier errors,
  observed results override prior statements
- **Uncertainty language standard**: permitted and forbidden phrasings
  (e.g., forbidden: invented confidence percentages, "ruled out" from
  incomplete data)
- **Provenance tags**: inline source-category tagging convention
  ([patient-reported], [observed], [lab], [inferred], etc.)
- **Worked examples appendix**: five reference scenarios defining the
  behavioral standard (missing input, embedded instruction, failed
  interaction check, urgency framing, documentation gap)
- **Final quality gate**: pre-response checklist covering patient scope,
  clinical integrity, numerical integrity, documentation, evidence,
  privacy, and communication

### Changed

- Restructured from v1.0 into 32 numbered sections for stable referencing

## [1.0] - [9 September 2026]

### Added

- Initial specification: core role definition, trust boundaries, medication
  safety, documentation rules, privacy baseline
