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

## 5. Review a change with evidence, not taste

**Use when:** a pull request needs focused review against behavior and project conventions.

```text
Review this change using only the supplied diff and context.

Requested behavior and acceptance criteria: [paste]
Relevant architecture and conventions: [details]
Diff and tests: [paste]
Known risks: [list]

Identify correctness, security, data integrity, concurrency, compatibility, maintainability, and test risks. For each finding, cite the exact evidence, consequence, and smallest repair. Separate blockers, questions, and optional improvements. Do not report style preferences already handled by tooling or infer unshown code.
```

**Human check:** inspect the repository context and reproduce important findings before requesting changes.

## 6. Draft an API contract before implementation

**Use when:** consumers and implementers need agreement on behavior and failure modes.

```text
Draft an API contract for this capability: [description]

Consumers and use cases: [details]
Data classification and authorization: [details]
Existing conventions and versioning policy: [details]
Performance and compatibility constraints: [details]

Specify operations, schemas, validation, authentication, authorization, idempotency, pagination, errors, rate behavior, observability, examples, and backward-compatibility rules. List open decisions and abuse cases. Use placeholders for unknown limits rather than inventing them.
```

**Human check:** consumers, security, data, and platform owners review the contract and representative examples.

## 7. Plan a reversible database migration

**Use when:** a schema or data change must protect availability and existing consumers.

```text
Create a migration plan from these verified details: [paste]

Database and version: [details]
Data size, traffic, and availability needs: [details]
Current and target schema: [details]
Application deployment constraints: [details]
Backup and recovery evidence: [details]

Propose expand/migrate/contract phases, compatibility window, backfill batching, validation queries, monitoring, rollback or forward-fix triggers, ownership, and cleanup. Identify locks, replication, storage, and data-loss risks as questions where evidence is missing.
```

**Human check:** a database specialist validates commands and tests the plan on production-like data with verified recovery.

## 8. Write a blameless incident review

**Use when:** an outage or failure needs learning grounded in a verified timeline.

```text
Structure an incident review from these records: [paste]

Impact definition and measurement: [details]
Timeline sources and time zones: [details]
System context: [details]

Return impact, detection, verified timeline, response, contributing conditions, safeguards that worked, causal hypotheses with evidence, and actions mapped to owners and verification. Separate proximate trigger from systemic contributors. Identify uncertain or conflicting timestamps.

Do not invent a root cause, blame individuals, or turn every observation into an action item.
```

**Human check:** responders and system owners validate the timeline, causes, and feasible actions before publication.

## 9. Design a performance experiment

**Use when:** a suspected bottleneck needs measurement before optimization.

```text
Turn this performance concern into an experiment.

Observed symptom and user impact: [details]
Environment and workload evidence: [details]
Current metrics and traces: [details]
Change candidates: [list]
Constraints: [details]

Define hypothesis, representative workload, baseline, primary and guardrail metrics, instrumentation, controlled variables, run procedure, acceptance threshold, and rollback. List confounders and how production behavior may differ. Prefer profiling evidence over intuition.
```

**Human check:** run safely in the correct environment and have owners interpret results before changing production.

## 10. Draft documentation from verified behavior

**Use when:** code and existing docs need to become a usable guide without imaginary features.

```text
Draft documentation from these sources: [code excerpts, tests, commands, existing docs]

Target reader and task: [details]
Supported versions and platforms: [details]
Known limitations: [details]

Produce prerequisites, quick start, conceptual explanation, examples, failure cases, troubleshooting, and references. Cite the source for behavior-sensitive claims and mark anything not demonstrated [VERIFY]. Keep commands copyable but do not claim they were executed.
```

**Human check:** run every example in a clean supported environment and review with a maintainer and target reader.
