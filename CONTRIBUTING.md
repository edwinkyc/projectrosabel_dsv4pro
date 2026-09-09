# Contributing to Rosabel

Thank you for your interest in improving this prompt. Because this project
governs AI behavior in a healthcare context, contributions are held to a
higher standard of justification than a typical software project.

## Ways to Contribute

### 1. Report a problem or gap

Open an issue describing:

- **What happened:** the behavior you observed or the gap you found
- **What should happen:** the behavior the prompt should produce
- **Why it matters clinically:** the patient-safety, privacy, or integrity
  impact
- **Reproduction:** the input or scenario that triggers the issue
  (use synthetic cases only — never real patient data)

### 2. Propose a change

1. **Fork** this repository (button at the top right of the repo page).
2. Create a branch for your change:
   `git checkout -b your-change-name`
3. Make your edits.
4. **Commit** with a clear message explaining the clinical rationale.
5. **Open a Pull Request** against the `main` branch.

### 3. Add a worked example

The appendix of worked examples defines the behavioral standard. New examples
are especially welcome for scenarios the current set doesn't cover
(e.g., multi-patient mix-ups, conflicting records, tool timeouts, translation
ambiguity). Follow the existing format: scenario, wrong behavior, right
behavior.

## Rules for Clinical Content Changes

Changes to clinical or safety-related sections require:

- **A written rationale** — why the change improves safety, honesty, or
  usability
- **Supporting evidence or reference** where applicable (guideline,
  standard, or documented failure mode)
- **Consistency check** — confirm the change doesn't contradict the
  Non-Negotiables or Priorities sections, which override everything else

Changes that weaken a safety control will be scrutinized heavily and need a
compelling justification.

## What Will Not Be Accepted

- Content that weakens the Non-Negotiables (section at the top of the prompt)
- Real patient data in any issue, pull request, or example
- Changes that claim capabilities a prompt cannot actually guarantee
  (e.g., "the model will always...")
- Promotional content, advertising, or unrelated links

## Style Guidelines

- Keep the prompt's existing voice: direct, imperative, no filler
- One rule per bullet; short sentences for safety-critical content
- Preserve the numbered section structure; add new sections at the end
  rather than renumbering existing ones (renumbering breaks external
  references)
- Update the version notes at the top of the prompt and
  [CHANGELOG.md](CHANGELOG.md) with any substantive change

## Code of Conduct

All participation is governed by our [Code of Conduct](CODE_OF_CONDUCT.md)
(if present). In short: be respectful, assume good faith, and remember the
goal is patient safety.

## Questions

Not sure whether something belongs here? Open an issue and ask — a
"should I contribute this?" question is always welcome.
