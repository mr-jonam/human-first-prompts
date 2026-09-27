<div align="center">

# Human-First Prompts

### Stop asking AI. Start briefing it.

**A practical, model-neutral prompt collection that makes assumptions visible, outputs reviewable, and human judgment non-negotiable.**

[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-7c3aed.svg)](LICENSE)
[![100 original prompts](https://img.shields.io/badge/prompts-100-0ea5e9.svg)](#browse-the-library)
[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-22c55e.svg)](CONTRIBUTING.md)
[![Sponsor](https://img.shields.io/badge/support-the%20project-f97316.svg)](#support-the-project)

[Browse](#browse-the-library) · [Model adapters](models/README.md) · [Use the canvas](templates/prompt-canvas.md) · [Contribute](CONTRIBUTING.md) · [Italiano](README.it.md)

</div>

---

Most prompt libraries optimize for volume. This one optimizes for **better decisions after the answer arrives**.

Every prompt gives the model enough context to be useful, asks it to expose uncertainty, and ends with a human checkpoint. Copy it, replace the `[brackets]`, and keep only what survives your review.

> AI can draft, challenge, organize, and simulate. It cannot own your goals, verify reality on its own, or accept responsibility for the result.

## The CLEAR pattern

Each prompt uses a compact briefing pattern you can reuse anywhere:

| Letter | Ask for | Why it matters |
|---|---|---|
| **C** | Context | The situation, audience, and available inputs |
| **L** | Limits | Boundaries, risks, tone, time, and non-goals |
| **E** | Evidence | Sources, facts, and what must not be invented |
| **A** | Answer shape | A concrete format you can inspect and reuse |
| **R** | Review | Assumptions, weak points, and the next human check |

## Browse the library

| Collection | What it helps you do | Prompts |
|---|---|---:|
| [Personal life](prompts/personal-life.md) | Plan time, travel, meals, purchases, home issues, privacy, and habits | 10 |
| [Creative studio](prompts/creative-studio.md) | Develop concepts, images, stories, names, episodes, and critique | 10 |
| [Work & career](prompts/work-career.md) | Prepare meetings, applications, interviews, growth, offers, and onboarding | 10 |
| [Communication & decisions](prompts/communication-decisions.md) | Write sensitive messages, feedback, negotiations, summaries, and updates | 10 |
| [Learning & research](prompts/learning-research.md) | Build learning paths, research questions, source reviews, and recall practice | 10 |
| [Writing & content](prompts/writing-content.md) | Brief, draft, edit, simplify, teach, present, and localize responsibly | 10 |
| [Marketing & sales](prompts/marketing-sales.md) | Position, research, publish, reach out, sell, and experiment ethically | 10 |
| [Business & operations](prompts/business-operations.md) | Improve SOPs, projects, risks, vendors, support, capacity, and reporting | 10 |
| [Development](prompts/development.md) | Clarify features, debug, review, design contracts, migrate, and document | 10 |
| [QA & testing](prompts/qa-testing.md) | Frame risks, prepare evidence, plan specialist testing, and report limits | 10 |

**100 original prompts across 10 focused collections.** Broad enough to be useful, curated enough to remain reviewable.

## Quick start

1. Choose the prompt closest to your real outcome.
2. Replace every `[placeholder]`; delete irrelevant instructions.
3. Optionally append one [model adapter](models/README.md) for ChatGPT, Claude, Gemini, Copilot, Perplexity, Grok, Mistral, or DeepSeek.
4. Paste your source material, run the prompt, then complete the **Human check**.

For a prompt of your own, start from the [Prompt Canvas](templates/prompt-canvas.md).

## What makes these prompts different

- **Model-neutral:** one prompt works across providers; small adapters improve fit without duplicated content.
- **Reviewable:** outputs have a requested structure, not an unbounded wall of text.
- **Evidence-aware:** prompts separate supplied facts, inferences, and unknowns.
- **Human-in-the-loop:** consequential decisions stay with the person accountable for them.
- **Clean-room authored:** the prompts were written for this repository, not copied from the reference libraries listed below.

## Responsible use

Treat generated material as a draft. Verify dates, names, calculations, citations, security claims, and anything that affects people or money. Health, legal, financial, hiring, security, accessibility, and compliance decisions require qualified review.

The QA collection deliberately stops before professional sign-off. It can improve preparation and surface questions; a qualified tester still needs to inspect the product, evidence, environment, and business risk.

## Contribute a prompt people will keep using

We welcome original prompts, translations, field-tested improvements, and clearer human checks. Read [CONTRIBUTING.md](CONTRIBUTING.md), use the proposal form, and explain what changed when refining an existing prompt.

Forks and adaptations are welcome under [CC BY 4.0](LICENSE). When sharing, credit **Human-First Prompts** with a link to this repository and indicate your changes. A ready-to-paste attribution is in [NOTICE](NOTICE).

## Support the project

If this library saves you time, help keep it open and maintained:

- [GitHub Sponsors](https://github.com/sponsors/mr-jonam)
- [Ko-fi](https://ko-fi.com/mrjonam)
- [Buy Me a Coffee](https://www.buymeacoffee.com/mrjonam)
- [PayPal](https://www.paypal.me/manorollo)

You can also help for free: **star the repo, share one prompt that worked, or contribute a better human check.**

[Share on LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fgithub.com%2Fmr-jonam%2Fhuman-first-prompts) · [Share on X](https://twitter.com/intent/tweet?text=Useful%20AI%20prompts%20with%20human%20judgment%20built%20in&url=https%3A%2F%2Fgithub.com%2Fmr-jonam%2Fhuman-first-prompts)

## Research references

The information architecture was informed by the public browsing experiences of [Techpresso AI Academy](https://academy.techpresso.co/prompts), [The Prompt Collection](https://github.com/luongnv89/prompts), [aiprompts.run](https://aiprompts.run/), and [Prompt Collections](https://promptcollections.com/). The provider adapters use current official documentation linked in the [model guide](models/README.md). No prompt text was copied. See [RESEARCH-NOTES.md](RESEARCH-NOTES.md) for the clean-room review.

## License and provenance

Repository content is © 2026 `mr-jonam` and licensed under [Creative Commons Attribution 4.0 International](LICENSE). See [LICENSE-DECISION.md](LICENSE-DECISION.md), [NOTICE](NOTICE), and [PROVENANCE.md](PROVENANCE.md).

This repository provides educational material, not professional advice. No warranty is given.
