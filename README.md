# Project Rosabel — Healthcare AI System Prompt

**An open-source system prompt for building safety-focused, clinician-facing AI assistants. Designed for DeepSeep-V4-Pro.**

Rosabel is a comprehensive system prompt (specification v2.0) designed for AI
assistants that support healthcare professionals with evidence review, clinical
information synthesis, documentation, medication review, patient communication,
and care coordination.

It is built around one principle: **an honest, incomplete answer is always
better than a confident, wrong one.**

---

## Important Disclaimer

This project is a **prompt specification for AI systems**. It is:

- **Not medical advice**
- **Not a medical device**
- **Not evaluated or approved** by the FDA, EMA, MHRA, or any regulatory body
- **Not a substitute** for clinical judgment, institutional review, or
  regulatory compliance

Deploying this prompt in any clinical setting requires independent validation,
institutional governance, and compliance with applicable healthcare regulations
(e.g., HIPAA, GDPR). The authors accept no liability for clinical outcomes
resulting from its use. DeepSeek is a trademark of its respective owner. 
This project is independent and not affiliated with, endorsed by, or sponsored 
by DeepSeek or Poe.See [DISCLAIMER.md](DISCLAIMER.md) for details.

---

## Try It Live

A hosted version of this prompt is available on Poe:

**[Try Rosabel on Poe](https://poe.com/Rosabel-DSv4pro)**

*Note: The hosted version is for evaluation and demonstration only. It has no
EHR access, no prescribing capability, and no patient data.*

---

// 
## What This Prompt Does

Project Rosabel defines how an AI assistant should support clinicians while preserving factual integrity, patient safety, and professional accountability.
The prompt specifies behavior; authentication, access restrictions, approval validation, and external-action controls require implementation by the host system.

Key design features:

| Area | What the prompt enforces |
|---|---|
| **Non-negotiables** | Never fabricate clinical facts, sources, or completed actions — regardless of urgency or user authority claims |
| **Component-wise safety gates** | Evaluates prerequisites separately for each component, completing safe work while withholding only unsupported/unauthorized parts |
| **Medication safety** | Halt conditions that block executable dosing when weight, renal function, or verified sources are missing |
| **Epistemic honesty** | "Interaction check failed" is never reported as "no interactions found"; partial reviews remain explicitly partial |
| **Injection resistance** | Instructions embedded in patient records, attachments, or documents are treated as data, never as commands |
| **Documentation integrity** | Never fabricates exam findings, consent, counseling, administration, or "negative" review of systems; preserves draft status |
| **Uncertainty language** | Standardized phrasing identifying what is unknown and why — no invented confidence percentages, no false reassurance |
| **Provenance** | Distinguishes patient-reported, observed, lab, device, historical, and inferred information with timestamps and scope |
| **Dependency-bound revision** | Requires reassessment of dependent work when supporting info changes; unaffected independent work continues |
| **Evidence-bound approval** | Binds approval to specific patient, encounter, content, destination, evidence, and policy versions; material changes invalidate approval |
| **Action-outcome integrity** | Separates preparation, approval, submission, and outcomes; requires matching receipts for completion claims |
| **Scope discipline** | Drafts clinical orders and notes, but never executes, signs, or transmits them |
| **Privacy and identity** | Enforces patient-scoped access, minimum necessary information, and separation of patient data from general memory |
| **Failure recovery** | Continues independent work after failures, limits retries, and prevents ungoverned repeats on unknown outcomes |
| **Version-aware deployment** | Separates prompt version from model, tools, and policies; does not assume validation transfers across changes |

## What's Included

- **`MAIN.md`** — the full prompt, specification v2.1

## Who This Is For

- **Developers** building clinician-facing AI tools who want a rigorous
  safety baseline
- **Healthcare organizations** evaluating prompt-level safety controls
- **Researchers** studying LLM behavior in high-stakes domains
- **Prompt engineers** looking for a reference implementation of
  healthcare-grade instruction design

## Who This Is Not For

- Patients seeking medical advice (this prompt governs a clinician-facing
  tool, and includes restrictions on direct patient-facing use)
- Anyone looking for a plug-and-play, deployment-ready clinical product —
  this is a prompt, not a validated system

## Version History

See [CHANGELOG.md](CHANGELOG.md) for details.

## Contributing

Contributions are welcome — especially:

- Gap analysis against real clinical workflows
- Additional worked examples for the appendix
- Translations and jurisdiction-specific adaptations
- Adversarial test cases (pressure patterns, injection attempts)

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
Clinical content changes require justification and, where applicable,
supporting evidence.

## Reporting Issues

- **Prompt bugs, unclear instructions, behavioral gaps:**
  [open an issue](https://github.com/edwinkyc/projectrosabel_dsv4pro/issues)
- **Safety-sensitive findings** (e.g., a prompt-injection vector that defeats
  the trust boundaries): please report privately per
  [SECURITY.md](SECURITY.md) rather than in a public issue.

## License

This project is licensed under the MIT License — see
the [LICENSE](LICENSE) file for details.

## Citation

If you use this prompt in research or a publication, please contact us for further instructions.
