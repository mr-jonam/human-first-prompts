# Research Notes

**Review date:** 2026-09-27
**Method:** public-page review of information architecture, positioning, usage flow, contribution model, and licensing. Prompt text was not imported into this repository.

## Observed patterns

| Reference | Useful public pattern | Gap this project addresses |
|---|---|---|
| [Techpresso AI Academy](https://academy.techpresso.co/prompts) | Large category/subcategory catalog; cards explain what a prompt does; broad career, business, writing, development, and lifestyle coverage | Volume can make selection difficult; Human-First Prompts uses fewer outcome-based entries with explicit review steps |
| [The Prompt Collection](https://github.com/luongnv89/prompts) / [site](https://the-prompt-collection.github.io/) | Repository-backed categories, contribution path, system context, search-oriented website | This repository stays dependency-free and makes provenance and human checks part of each prompt |
| [aiprompts.run](https://aiprompts.run/) | Fast search, model launch links, many categories, CC BY 4.0 attribution model | This repository favors editorial depth and transparent uncertainty over database size |
| [Prompt Collections](https://promptcollections.com/) | Job-oriented packs, tested positioning, variables, and a playground | This repository is fully open, model-neutral, and designed for adaptation through Git |

The expansion review also considered the supplied screenshots of public category listings. They showed especially deep coverage in career communication, marketing, branding, social channels, content, and business work. Those themes informed broader outcome coverage, while all wording, prompt structure, safety limits, and human checks were newly authored here.

## Clean-room rules used

- Categories and general use cases are ideas, not copied expression.
- Every prompt was authored specifically for this repository from a user outcome and the CLEAR pattern.
- No source prompt was copied, translated, or mechanically paraphrased.
- Reference brands, logos, screenshots, datasets, and site code are not included.
- Contributions must document any third-party material and its compatible license.

## Editorial direction

The collection deliberately emphasizes:

1. a concrete decision or action after the AI response;
2. supplied evidence over confident completion;
3. assumptions and unknowns as first-class output;
4. small, reviewable formats;
5. professional escalation for high-impact domains;
6. restrained QA support that improves preparation but leaves testing and sign-off to specialists.

## Model adapter sources

Provider guidance was reviewed separately from the reference libraries so the core prompts could remain portable:

- [OpenAI prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering)
- [Anthropic prompting best practices](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables)
- [Google Gemini prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Microsoft Learn: effective Copilot prompts](https://learn.microsoft.com/en-us/training/modules/write-effective-prompts-do-more-prompting/)
- Official developer-documentation entry points for [Perplexity](https://docs.perplexity.ai/), [xAI](https://docs.x.ai/), [Mistral](https://docs.mistral.ai/), and [DeepSeek](https://api-docs.deepseek.com/)

The resulting adapters describe interaction patterns, not rankings or guaranteed capabilities. Product features, privacy controls, model names, and availability must be checked in the selected interface.
