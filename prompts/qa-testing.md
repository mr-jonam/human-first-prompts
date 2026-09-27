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

## 5. Prepare a testability review

**Use when:** a design should expose controllability and observability gaps before test execution.

```text
Facilitate a preliminary testability review for specialist validation.

Feature and architecture evidence: [details]
States, dependencies, and data: [details]
Current logs, metrics, flags, and test interfaces: [details]
Environment constraints: [details]

Map inputs, states, outputs, side effects, clocks, randomness, external dependencies, and failure injection. Identify where behavior cannot be controlled or observed and questions for design owners. Suggest low-cost seams or telemetry improvements, including privacy and security constraints.

Do not claim the system is testable from documentation alone.
```

**Human check:** QA and engineering specialists inspect the implementation and environment before accepting changes.

## 6. Propose regression scope from change evidence

**Use when:** a change needs risk-informed regression discussion, not an automatically trusted test list.

```text
Draft a regression-scope proposal.

Change diff or technical summary: [paste]
User and business flows: [details]
Dependencies, data, configuration, and deployment path: [details]
Defect history and existing coverage evidence: [details]
Time and environment constraints: [details]

Trace changed components to plausible direct, indirect, integration, operational, and rollback impacts. Rank areas using an explicit scale and show evidence. Propose coverage layers, exclusions, and triggers for expanding scope. Mark all inferred dependencies for confirmation.
```

**Human check:** a tester reviews the actual change graph, product risk, and prior evidence before setting scope.

## 7. Prepare an API testing workshop

**Use when:** an API change needs shared questions across behavior, data, and operations.

```text
Create a workshop guide for API testing.

Contract and examples: [paste]
Consumers and workflows: [details]
Authentication and authorization model: [details]
Data and operational constraints: [details]

Generate questions across schema validation, boundaries, state transitions, idempotency, concurrency, pagination, errors, permissions, privacy, compatibility, rate behavior, observability, and dependency failure. Map each question to required evidence and an accountable expert. Avoid producing assumed expected results.
```

**Human check:** API, security, data, operations, and QA specialists turn validated risks into executable tests.

## 8. Prepare an accessibility testing conversation

**Use when:** a team needs to plan accessibility evidence with qualified participation.

```text
Draft an accessibility test-planning brief.

Product, platforms, and user journeys: [details]
Target standards and organizational policy: [details]
Components and assistive-technology support claims: [details]
Existing audit and user-research evidence: [details]

Map critical journeys to keyboard, focus, semantics, names, states, contrast, resizing, motion, errors, timing, screen-reader, voice, and cognitive-access questions. Separate automated checks, expert manual evaluation, and research with disabled users. List environment and evidence needs.

Do not claim compliance from a checklist or automated tool.
```

**Human check:** accessibility specialists and disabled users, compensated appropriately, validate behavior and impact.

## 9. Surface non-functional risks before testing

**Use when:** reliability, performance, security, recovery, or compatibility may dominate feature correctness.

```text
Facilitate a non-functional risk review.

System purpose, users, architecture, and change: [details]
Service objectives and policies: [details]
Traffic, data, threat, device, and dependency evidence: [details]
Incident history: [details]

Identify risk questions for performance, capacity, resilience, recovery, security, privacy, compatibility, accessibility, maintainability, and operability. For each, state potential impact, trigger, evidence needed, specialist owner, and what a credible experiment would need. Do not generate thresholds not provided by owners.
```

**Human check:** domain specialists select methods, environments, tools, and acceptance criteria.

## 10. Synthesize a test report without declaring quality

**Use when:** executed checks and observations need a transparent report for decision-makers.

```text
Organize this verified test evidence into a report: [paste]

Scope and build: [details]
Coverage model and exclusions: [details]
Environment and data: [details]
Defect and risk policy: [details]

Return objective, executed scope, evidence links, results, defects, coverage limitations, environment differences, unresolved risks, and recommended next investigations. Distinguish not tested, blocked, failed, and passed. Tie conclusions to dated evidence and preserve contradictory results.

Do not calculate a universal quality score, infer unexecuted coverage, or make the release decision.
```

**Human check:** a qualified tester verifies the report, while accountable stakeholders decide whether the remaining risk is acceptable.
