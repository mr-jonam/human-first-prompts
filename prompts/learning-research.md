# Learning & Research

Prompts for learning efficiently without confusing fluent output with reliable knowledge.

## 1. Build an 80/20 learning path with proof of skill

**Use when:** starting a topic and needing a practical route through it.

```text
Design a learning path for [topic] aimed at [real-world outcome].

My current level: [what I can already do]
Available time: [hours per week and duration]
Preferred learning modes: [reading, practice, video, mentoring]
Tools or access constraints: [details]

Identify the small set of concepts and skills that unlock most practical progress. Organize them into milestones with prerequisites. For each milestone provide:
- what to understand
- a small task that proves the skill
- a common misconception
- a retrieval or reflection question
- a primary or authoritative resource type to seek

Separate fundamentals from optional depth. Do not invent course titles or links; when browsing, verify current sources and dates.
```

**Human check:** test the path by attempting the first proof task; revise based on actual difficulty, not the model's estimate.

## 2. Use a Socratic tutor that does not reveal everything

**Use when:** you want to learn by reasoning rather than receiving a polished answer.

```text
Tutor me on [topic] through questions and short feedback.

My level: [level]
The problem or concept: [details]
What I have tried: [attempt]

Rules:
- Ask one question at a time.
- Start by checking my mental model, not vocabulary.
- Give the smallest useful hint after an error.
- Ask me to predict before explaining.
- Every three turns, summarize what I can now do and one remaining gap.
- Do not provide the full solution unless I explicitly ask after making an attempt.
- If my answer reveals a prerequisite gap, step back and test it.

Begin with one diagnostic question.
```

**Human check:** solve a new problem without the chat; recognition during tutoring is not proof of independent skill.

## 3. Triangulate claims across sources

**Use when:** researching a question where sources may disagree or age quickly.

```text
Research this question: [question].

Scope: [geography, dates, population, definitions]
Decision this research informs: [decision]
Required source types: [primary data, official guidance, peer-reviewed work]

When browsing is available, prioritize primary and current sources. For every important claim provide a direct link, publication date, and access date. Build a claim table with supporting evidence, contradicting evidence, source limitations, and confidence.

Clearly separate:
- directly reported facts
- calculations you performed, including formula
- synthesis across sources
- your inference or opinion

Do not cite a search snippet as evidence. If sources use different definitions, do not average them or present them as equivalent. End with unresolved questions and what evidence would answer them.
```

**Human check:** open the key sources and verify that each citation supports the sentence attached to it.

## 4. Run a teach-back exam on your own notes

**Use when:** checking whether you understand material well enough to explain and apply it.

```text
Create a teach-back exam using only these notes:
[paste notes]

Target capability: [what I should be able to explain or do]
Difficulty: [introductory / working / advanced]

Generate:
1. Three explain-in-your-own-words questions
2. Two comparison questions
3. Two application scenarios with incomplete information
4. One misconception-detection question
5. One question that the notes cannot answer

Ask the questions one at a time and wait for my response. Score against an explicit rubric: accuracy, mechanism, transfer, and uncertainty awareness. Quote the relevant note section when correcting me. Never add outside facts without labeling them.
```

**Human check:** revisit the original source for any correction; your notes and the model may share the same omission.

## 5. Turn a broad interest into a researchable question

**Use when:** a topic is too wide or vague for useful investigation.

```text
Help me refine this topic into researchable questions: [topic]

Purpose and audience: [details]
Time, access, and method constraints: [details]
What I already believe and why: [details]

Propose questions with defined concepts, population or context, comparison, evidence type, and scope. Explain feasibility, value, bias risks, and what each question cannot establish. Include descriptive, comparative, and exploratory alternatives without pretending they are equivalent.
```

**Human check:** review the final question with a domain or methods expert before collecting consequential evidence.

## 6. Build a reading plan around disagreements

**Use when:** learning a field requires more than a list of popular books or articles.

```text
Design a reading plan for [topic].

My current level and goal: [details]
Time available: [details]
Sources already known: [list]
Access or language constraints: [details]

Organize foundational concepts, major schools or disagreements, current reviews, primary sources, and applied examples. For each slot, state selection criteria rather than inventing a citation. If browsing is available, provide verifiable links, dates, and source types. Add reflection questions and stop points for synthesis.
```

**Human check:** verify every reference in a library catalogue, publisher, DOI registry, or original source.

## 7. Build a concept map with contested links

**Use when:** notes contain many terms but their relationships remain unclear.

```text
Create a concept map from these notes: [paste]

Learning objective: [details]

List core concepts, concise definitions grounded in the notes, prerequisite links, causal claims, examples, counterexamples, and contested relationships. Mark each link as stated, inferred, or uncertain. Then propose a visual hierarchy and five questions that test the weakest connections.

Do not add domain facts unless clearly labeled as outside knowledge.
```

**Human check:** compare inferred relationships with authoritative sources or an instructor.

## 8. Create a spaced review plan that tests retrieval

**Use when:** you want durable recall without endlessly rereading.

```text
Turn this syllabus or note set into a [duration] review plan: [paste]

Assessment or real-world use: [details]
Available sessions and dates: [details]
Strong and weak areas: [details]

Schedule short retrieval sessions with interleaving, cumulative review, and application. Generate question types and answer-checking criteria, not just summaries. Adapt intervals to performance and include a recovery plan for missed sessions.

Do not claim an optimal universal schedule or hide topics that remain weak.
```

**Human check:** grade from original sources and adjust the plan using actual recall, not familiarity.

## 9. Compare competing frameworks fairly

**Use when:** two or more approaches are being discussed as rivals or universal solutions.

```text
Compare these frameworks using the supplied sources: [frameworks and sources]

Decision or learning context: [details]
Evaluation criteria: [list]

For each framework, describe purpose, assumptions, mechanisms, evidence base, boundary conditions, strengths, criticisms, and typical misuse. Use the same criteria for all. Identify complementarity, genuine incompatibility, and evidence gaps. Do not select a winner unless the context and criteria support one.
```

**Human check:** verify contested claims in primary or high-quality review sources and invite a knowledgeable critic.

## 10. Facilitate a study-group session

**Use when:** a group needs active learning rather than serial summaries.

```text
Create a [minutes]-minute study-group plan.

Material and learning goals: [details]
Participant level and group size: [details]
Preparation completed: [details]
Accessibility or participation needs: [details]

Include an opening retrieval check, rotating explanation, worked example, disagreement or misconception activity, application problem, and closing reflection. Provide facilitator questions, timeboxes, and a method to surface uncertainty without embarrassment.
```

**Human check:** adapt pacing and participation based on the group, and correct content against the original material.
