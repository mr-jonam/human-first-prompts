# Human-First Prompts — project map

- Stack/build: Markdown-only content repository; no build step or dependencies.
- Entrypoint: `README.md`; Italian overview in `README.it.md`.
- Prompt library: `prompts/*.md`, grouped by real-life domain.
- Model-specific guidance: `models/README.md`; base prompts remain provider-neutral.
- Reusable authoring format: `templates/prompt-canvas.md`.
- Tests: run the documented PowerShell checks and `git diff --check`.
- Config: `.github/FUNDING.yml`, issue forms, and pull request template.
- CI: intentionally absent; avoid recurring GitHub Actions usage for static content.
- License: CC BY 4.0 for repository content. See `LICENSE-DECISION.md` and `NOTICE`.
- Attribution: reuse must credit `https://github.com/mr-jonam/human-first-prompts` and note changes.
- Contributions: prompts must be original or have documented compatible provenance.
- Style: model-neutral, practical, concise, and explicit about assumptions and human review.
- Safety: high-impact outputs are drafts; never present AI output as professional approval.
- QA/testing: prompts support preparation and analysis, not release sign-off or specialist replacement.

## Useful commands

```powershell
rg "^## [0-9]+\." prompts | Measure-Object
rg "Human check" prompts
git diff --check
```
