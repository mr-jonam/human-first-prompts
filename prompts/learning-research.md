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
