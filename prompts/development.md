# Development

Prompts for software work that emphasize repository evidence, minimal change, and verification.

## 1. Turn a feature idea into testable boundaries

**Use when:** a request is clear in spirit but ambiguous in behavior.

```text
Act as a software analyst. Clarify this feature before implementation:
[feature request]

Users and permissions: [details]
Current behavior or system context: [details]
Known constraints: [platform, compatibility, performance, policy]
Out of scope: [details]

Return:
1. The user outcome in one sentence
2. Observable acceptance examples using Given / When / Then
3. Edge cases grouped by input, state, timing, permissions, and failure
4. Data and integration assumptions
5. Non-functional risks
6. The smallest releasable slice
7. Up to five questions that materially change the implementation

Do not invent existing APIs, schemas, or product rules. Mark every inference and challenge requirements that cannot be verified by a user or test.
```

**Human check:** review acceptance examples with product, engineering, and QA before estimating or coding.

## 2. Investigate a bug with competing hypotheses

**Use when:** you have symptoms and evidence but no confirmed root cause.

```text
Help me investigate this software defect.

Observed behavior: [exact symptom]
Expected behavior and source: [requirement or baseline]
Reproduction steps: [steps]
Environment and version: [details]
Recent changes: [details]
Logs, traces, screenshots, or code excerpts: [paste]

Create a ranked hypothesis table with: hypothesis, evidence for, evidence against, cheapest discriminating test, and expected observation. Separate symptom, trigger, contributing conditions, and root cause. Recommend the next single diagnostic action with the best information gain.

Do not claim a root cause from correlation. Do not invent log lines, code paths, or successful tests. If sensitive data appears, tell me to redact it before continuing.
```

**Human check:** reproduce or falsify the leading hypothesis in a controlled environment before changing code.

## 3. Draft an architecture decision record with reversibility

**Use when:** choosing among technical approaches with lasting trade-offs.

```text
Prepare an architecture decision record for: [decision].

System context: [components, load, team, lifecycle]
Forces and constraints: [list]
Options already considered: [list]
Evidence available: [benchmarks, incidents, docs]
Unknowns: [list]

For each option evaluate fit, operational burden, security, failure modes, migration cost, vendor dependence, team capability, and reversibility. Use ranges rather than fake precision. Recommend an option only if the evidence supports it.

Output: context, decision drivers, options, decision, consequences, rejected alternatives, validation plan, rollback or exit plan, and review trigger. List assumptions separately and cite authoritative documentation when browsing.
```

**Human check:** require review by the people who will operate, secure, and migrate the system—not only those building it.

## 4. Plan a minimal, safe code change

**Use when:** implementing a fix in an unfamiliar or active codebase.

```text
Using the repository evidence I provide, plan the smallest safe change for:
[requested change]

Relevant files or symbols: [paste paths and excerpts]
Current tests: [details]
Compatibility constraints: [details]
Changes already in the working tree: [details]

Trace the current behavior from entrypoint to side effects. Identify the invariant that must change and those that must remain. Propose:
1. Files to modify and why
2. A minimal implementation sequence
3. One failing-before / passing-after behavioral test
4. Regression risks
5. A rollback plan

Prefer existing patterns. Do not propose broad refactors unless the requested behavior cannot be isolated. Never assume an unshown function or dependency exists; ask for the specific missing evidence.
```

**Human check:** inspect the actual diff, run the relevant test, and review unrelated working-tree changes before committing.
