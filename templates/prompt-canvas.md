# Human-First Prompt Canvas

Replace every bracketed field. Remove lines that do not serve the task.

```text
GOAL
Help me [observable outcome]. The result will be used by [audience] for [decision or action].

CONTEXT
- Situation: [what is happening]
- Inputs I can provide: [facts, notes, files, links]
- Constraints: [time, budget, tone, policy, tools]
- Out of scope: [what the model must not do]

EVIDENCE RULES
- Treat only my supplied material and cited sources as facts.
- Label inferences and assumptions.
- If essential information is missing, ask up to [number] focused questions before drafting.
- Do not invent quotations, measurements, citations, test results, or user feedback.

TASK
1. [analysis or transformation]
2. [challenge, comparison, or verification]
3. [draft the usable result]

OUTPUT
Return:
1. [format and length]
2. Assumptions and unknowns
3. Risks or counterarguments
4. The next human verification step

QUALITY BAR
Before answering, check that the result is specific, internally consistent, traceable to the inputs, and usable by the stated audience.
```

## Human check

Confirm that the prompt contains no secrets or unnecessary personal data. After generation, verify claims against primary evidence and decide whether a qualified reviewer is needed.
