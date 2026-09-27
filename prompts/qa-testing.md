# QA & Testing

These prompts help teams prepare evidence and questions. They do **not** execute tests, certify quality, approve a release, or replace a qualified QA/testing specialist.

## 1. Start a risk-based test conversation

**Use when:** a feature needs an initial risk map before a tester designs the approach.

```text
Act as a facilitator for a preliminary product-risk workshop, not as the final test authority.

Feature or change: [description]
Users and business outcome: [details]
Architecture and integrations we know: [details]
Data involved: [details]
Constraints and release context: [details]
Historical incidents or weak areas: [facts]

Identify plausible failure modes across user value, data, permissions, integration, timing, recovery, compatibility, accessibility, security, and operations. For each, explain the impact, triggering conditions, observable evidence, and what is still unknown. Rank only with an explicitly stated likelihood/impact scale.

Return a workshop-ready risk table plus questions for product, development, operations, security, accessibility, and QA. Do not invent system behavior, test coverage, or risk scores. End with items that require a specialist to inspect the actual product or architecture.
```

**Human check:** a QA/testing specialist and relevant domain owners must validate the risk model before it drives coverage or release decisions.

## 2. Turn raw observations into a reproducible bug report

**Use when:** you have notes, screenshots, or logs that need structure.

```text
Convert my raw defect notes into a precise draft bug report without adding facts.

Raw notes: [paste]
Requirement or expected-behavior source: [link or text]
Environment and build: [details]
Available evidence: [screenshots, video, logs, IDs]
Privacy or security constraints: [details]

Return:
- concise title describing behavior, condition, and impact
- preconditions
- minimal numbered reproduction steps
- observed result
- expected result tied to the supplied source
- reproducibility based only on supplied runs
- environment
- evidence inventory
- missing information and the next reproduction variation

Keep severity and priority separate; if I have not provided the team's definitions, leave both "to triage." Redact or flag secrets and personal data. Never infer root cause from the symptom.
```

**Human check:** reproduce the draft on the named build and let the triage group assign impact, urgency, and ownership.

## 3. Prepare an exploratory testing charter

**Use when:** a tester needs a starting charter, not generated test execution.

```text
Draft an exploratory testing charter for specialist review.

Product area and change: [details]
User or business risk to investigate: [risk]
Known architecture, data, and dependencies: [details]
Existing coverage and known gaps: [evidence]
Session timebox and environment: [details]

Use the structure "Explore [target] with [resources] to discover [information]." Add focused heuristics, data variations, state transitions, observability needs, and explicit exclusions. Suggest note-taking fields for setup, actions, observations, questions, and evidence.

Do not produce a huge generic test-case list. Do not claim coverage before execution. Keep the charter narrow enough for the timebox and list the assumptions a tester should challenge first.
```

**Human check:** the tester adapts the charter while learning, captures real evidence, and decides follow-up sessions based on findings.

## 4. Prepare a release-readiness evidence review

**Use when:** consolidating inputs before an accountable release conversation.

```text
Organize the supplied material into a release-readiness evidence pack. Do not make the release decision.

Release scope and excluded items: [details]
Acceptance evidence: [links or notes]
Test execution and coverage evidence: [links or notes]
Open defects and accepted risks: [list]
Operational, security, accessibility, and compliance inputs: [details]
Rollback or recovery evidence: [details]
Decision owners and policy: [details]

Build a table of claim, supporting evidence, owner, freshness, limitation, and status: supported / contradicted / missing. Highlight scope gaps, stale evidence, unowned risks, and claims based only on assertion. Summarize arguments for release, arguments for delay, and the smallest actions that reduce the largest uncertainty.

Do not convert missing evidence into a pass. Do not assign sign-off to the AI or imply that zero known defects means acceptable quality.
```

**Human check:** designated product, engineering, QA, security, operations, and business owners apply their actual policy and accept or reject the remaining risk.
