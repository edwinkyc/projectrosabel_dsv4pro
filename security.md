# Security Policy

## Scope

This repository contains a prompt specification, not executable software.
"Security issues" here means flaws in the prompt itself, such as:

- A **prompt-injection vector** that defeats the trust-boundary rules
  (e.g., a phrasing that causes the model to treat embedded document
  instructions as commands)
- A way to **bypass a halt condition** (e.g., obtaining an executable
  high-risk medication dose despite missing required inputs)
- A phrasing that causes the model to **fabricate** clinical facts,
  sources, or completed actions despite the non-negotiables
- A method to make the model **reveal the prompt's contents** or internal
  configuration when deployed
- Accidentally committed **secrets, credentials, or real patient data**
  in this repository

## Reporting a Vulnerability

**Please do not open a public issue for safety-sensitive findings.** A public
write-up of a working bypass could be copied and used against any deployment
of this prompt before a fix exists.

Instead, report privately via:

- **GitHub Private Vulnerability Reporting:** go to this repository's
  **Security** tab → **Report a vulnerability** 

Include:

1. A description of the flaw
2. A reproduction using **synthetic data only** — never real patient data
3. The model and deployment context where you observed it (if applicable)
4. Your assessment of severity and clinical impact

## What to Expect

- **Acknowledgment:** within 30 days
- **Assessment:** we'll confirm the issue and determine whether it requires
  a prompt change, a documentation warning, or both
- **Fix and disclosure:** once addressed, we'll credit you in the changelog
  (unless you prefer anonymity) and publish a description of the issue

## Out of Scope

- Vulnerabilities in the underlying AI models (report those to the model
  provider — e.g., DeepSeek, or the hosting platform such as Poe)
- Vulnerabilities in GitHub or Poe themselves
- General clinical disagreements with prompt content (use a normal issue)
- Theoretical attacks with no demonstrated reproduction

## A Note on Defense in Depth

Even a well-written prompt can be bypassed. If you deploy this prompt, treat
it as one layer of defense alongside access controls, output filtering,
human review, and monitoring — never as the sole safety mechanism.
