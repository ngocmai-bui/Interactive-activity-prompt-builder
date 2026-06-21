# Interactive Activity Prompt Builder

A vibecoded prompt repository that helps language teachers generate structured, SLA-informed prompts for creating gamified or interactive classroom activities — built as part of an MA research project on AI-assisted language teaching tool design.

## What it does

Instead of typing a vague request directly into an AI chatbot ("make me a grammar game"), this tool guides a teacher through a structured decision process:

1. **Learner Profile** — CEFR level, topic, target language structure, lesson phase, and class format
2. **Pedagogical & Activity Design** — the tool recommends compatible combinations of SLA principles (e.g. Focus on Form, Output Hypothesis, Comprehensible Input) and classroom activity types (e.g. Information Gap, Role-Play), filtering out combinations that are structurally or theoretically incompatible
3. **Prompt Generation** — all inputs are assembled into a single, clearly organised prompt the teacher copies and pastes into Claude to generate a ready-to-use, teacher-led classroom activity

The tool does not generate the activity itself — it generates a **better prompt**, so that AI tools produce activities that are pedagogically sound, not just technically functional.

## Why this exists

Teachers can now build interactive learning materials with AI without programming knowledge, but the pedagogical quality of what they build depends entirely on the quality of their prompts. A teacher confident with AI tools but without deep SLA training may not know, for example, that "Interaction Hypothesis" requires a responsive partner and cannot be meaningfully combined with a single-player game mechanic. This tool externalises that theoretical knowledge into the interface itself, so teachers don't need to already know it to use it correctly.

## How it was built

This tool was built entirely through vibecoding — describing functionality in plain English to Claude and iterating on the generated code, with no manual programming. The build went through several iterations, documented in the accompanying development log:

- An initial version allowed free selection of any SLA principle with any activity, which testing revealed could produce theoretically incoherent combinations (e.g. a principle requiring interaction paired with a solo activity).
- This was replaced with a constraint-based recommendation engine: a hard filter excludes activities structurally incompatible with the selected class format, and the remaining options are scored and ranked, with a manual override still available.
- A bug found during testing (the engine recommending pair/group-only activities for an individual-format profile) led to format and skill compatibility being treated as hard constraints rather than soft scoring bonuses.

Every prompt, output, and design decision is recorded in the development log.

## Tech

Single self-contained HTML file — no build process, no dependencies, no server. Open it in any browser.

## Academic context

Built for Strand 3 (Prompt Repositories & Teacher Training), *Digital Linguistics in Action*, MA Digital Linguistics, TU Chemnitz, SoSe 2026.
