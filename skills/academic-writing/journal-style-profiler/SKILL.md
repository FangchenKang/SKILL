---
name: journal-style-profiler
description: Build and apply a target academic journal writing-style profile from 10 to 20 representative papers. Use when the user wants Codex to analyze a journal's academic expression habits, generate journal_style_profile.md, review a manuscript against that profile, or rewrite sections to better fit a target journal's abstract, introduction, literature review, theory/framework, empirical/case, and conclusion conventions.
---

# Journal Style Profiler

## Overview

Use this skill to infer the academic expression habits of a target journal and apply them to manuscript revision. Treat journal style as a set of writing decisions: how a problem is posed, how concepts are placed, how arguments advance, how evidence enters theory, and how conclusions control their claims.

Do not reduce journal style to surface markers such as word frequency, sentence length, favorite transition words, or generic "academic tone." Record those only as secondary signals when they reveal deeper argumentative habits.

## Decision Flow

1. If the user provides 10 to 20 representative papers, build a corpus map first.
2. If the user provides fewer than 10 papers, proceed only as a provisional profile and state the limitation.
3. If the user provides only a target journal name, locate accessible representative papers when possible; otherwise ask the user for papers or permission to make a clearly provisional profile.
4. If the user provides `journal_style_profile.md` and a draft, review the draft against the profile instead of rebuilding the corpus.
5. If the user asks to revise, preserve the manuscript's core argument, evidence, terms, and contribution unless they explicitly ask for restructuring.

## Core Workflow

### 1. Build the Corpus Map

Read the sample papers as a journal corpus, not as isolated articles. Prefer 10 to 20 recent papers from the last 3 to 5 years, with topic, method, and article type close to the user's manuscript.

For each paper, record metadata and style observations. Use `references/extraction_matrix.md` when the task requires a systematic profile or when the corpus is mixed.

Track at least these dimensions:

- Research problem and problem escalation.
- Abstract sequence and contribution statement.
- Introduction route from phenomenon, policy, theory, contradiction, history, or case.
- Literature review organization and gap construction.
- Concept placement and theoretical framework movement.
- Case, data, or empirical narration.
- Mechanism explanation and argumentative rhythm.
- Conclusion boundary and claim restraint.
- Language habits that express academic logic, not merely surface phrasing.

### 2. Synthesize Journal-Level Habits

Distinguish three layers:

- Disciplinary norm: broad expectations of the field.
- Journal convention: recurring habits across the target journal corpus.
- Article-level variation: one author's wording, topic, or method-specific preference.

Emphasize journal convention. Do not label a habit as journal style unless it appears across multiple papers or is strongly tied to the journal's repeated article types.

Use confidence levels:

- High: 10 to 20 recent, relevant papers with consistent patterns.
- Medium: adequate corpus but mixed in topic, method, or period.
- Low: fewer than 10 papers, old papers, weak topical proximity, or heavy dependence on a small author group.

### 3. Generate `journal_style_profile.md`

Write the profile as an operational guide for drafting and revision, not as a literature review of the journal. Use `references/profile_template.md` for the required structure.

The profile must cover:

- Overall journal style.
- Abstract writing pattern.
- Introduction problematization.
- Literature review organization.
- Concept and theoretical framework pattern.
- Case, data, or empirical writing pattern.
- Mechanism explanation.
- Conclusion pattern and judgment boundary.
- Language and expression rules.
- Common mismatches to avoid.
- Revision checklist.

### 4. Review a Draft Against the Profile

When reviewing a manuscript, do not give generic academic writing advice. Tie every comment to the target journal profile.

Use four required diagnostic categories:

- Places that fit the target journal style.
- Places that do not fit.
- Sentences, paragraphs, or sections that need rewriting.
- Revised versions.

For Chinese manuscripts, use the user's requested headings when appropriate: `符合该期刊文风的地方`, `不符合的地方`, `需要改写的句段`, and `改写后的版本`.

Use `references/review_template.md` when the user asks for a reusable review file such as `journal_style_review.md`.

### 5. Revise the Manuscript

Revise in this priority order:

1. Sharpen the research problem so it becomes an academic question, not only a topic or policy importance claim.
2. Stabilize core concepts and place them in relation to literature, theory, local institutional experience, or empirical material.
3. Adjust the argumentative rhythm from problem to concept, concept to framework, framework to evidence, and evidence to contribution.
4. Make evidence do analytical work through process reconstruction, mechanism explanation, causal interpretation, typology, or conceptual refinement.
5. Control the conclusion so claims stay within the demonstrated evidence.

## Chinese Social Science Guidance

For Chinese social science, public administration, political science, sociology, law, and policy journals, pay special attention to problem awareness, concept placement, mechanism process, institutional detail, and restrained policy language.

Convert policy vocabulary into analytical vocabulary. A manuscript may begin from policy or governance practice, but it should not stop at social significance. The review should ask what academic puzzle the phenomenon creates, which concept or mechanism the article clarifies, and how empirical material changes or supports the theoretical claim.

## Guardrails

Do not fabricate a journal profile. If the corpus is insufficient, say so and mark the profile provisional.

Do not imitate or reproduce copyrighted sentences from published papers. Extract patterns, conventions, and argumentative moves. Use only short excerpts when necessary for diagnosis.

Do not erase the author's judgment. A profile guides revision; it does not replace the manuscript's research question, evidence, or theoretical position.

Do not overfit to one highly visible article, special issue, famous author, or method-specific template. Mark method-specific patterns separately.

## References

- Read `references/extraction_matrix.md` when building the corpus map or deciding whether an observed pattern is journal-level style.
- Read `references/profile_template.md` before generating `journal_style_profile.md`.
- Read `references/review_template.md` before generating `journal_style_review.md` or rewriting paragraphs from a draft.
