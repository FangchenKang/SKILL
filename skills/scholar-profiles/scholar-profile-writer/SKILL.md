---
name: scholar-profile-writer
description: Write or clean Chinese profiles of scholars in political science, public administration, law, sociology, and related social sciences. Use when the user provides biographical source text, OCR output, web notes, or raw excerpts and wants a concise or complete scholar profile covering career history, academic focus, representative works, concepts, projects, honors, and achievements, especially when they request "提取文字", "完整提取文字", "总结学者履历", "学术侧重面", "成就", or "不要小标题".
---

# Scholar Profile Writer

## Core Goal

Turn raw material about social science scholars into polished Chinese prose that preserves verifiable career facts, academic emphases, and achievements. Put the scholar's academic views, problem consciousness, original concepts, explanatory frameworks, and intellectual contributions at the center. Publications, projects, and honors are supporting evidence, not the main structure. Match the user's requested level of compression: if they ask for "完整提取文字" or "只提取文字", clean and reorganize the source with minimal compression; if they ask for "总结", condense while retaining the most important facts.

## Argument-First Synthesis

- Explain what the scholar argues, proposes, revises, or reveals. Prefer sentences like "他/她提出...", "他/她认为...", "其研究揭示...", "其贡献在于..." over sentences that only say "发表了...".
- Cluster publications by the academic view they support. Do not march through papers one by one unless the user explicitly requests a bibliography.
- For each major research direction, identify the underlying question, the scholar's answer, and the contribution to the field.
- Use representative works as evidence in parentheses or short clauses after summarizing the view. Example: "围绕基层水环境治理，她将河长制理解为跨部门协同与技术嵌入共同塑造的治理机制，相关成果包括《大国治水》和关于‘互联网+河长制’的系列论文。"
- If the source gives many article titles but few explicit conclusions, infer cautiously from titles, abstracts, and reliable source descriptions; mark it as a synthesis of the research focus rather than an unsupported claim.

## Output Shape

- Start each scholar with the scholar's name on its own line.
- Use continuous paragraphs, not invented section headings.
- Do not add headings such as "生平经历", "学术贡献", "研究方向", "主要成就", "教育培训", or numbered subsection titles unless the user explicitly asks for them.
- For multiple scholars, separate profiles with one blank line. Keep the same format for every scholar.
- Write in formal, fluent Chinese suitable for academic publicity, encyclopedia notes, or scholar profile files.
- Prefer clear chronological and thematic flow: basic identity and positions first, research fields and publication record next, then major themes, representative works, concepts, projects, awards, and social or disciplinary influence.
- In the academic contribution paragraphs, organize by ideas and research problems, not by publication chronology.

## Extraction Rules

- Remove source labels and workflow chatter such as "行政学人", "提取文字", "完整提取文字", "（一）", "在学术研究方面" when they only function as headings.
- Keep names, birth year and place, institutions, current and former posts, doctoral supervisor status, journal roles, association roles, policy advisory roles, projects, awards, publication titles, press names, years, journal names, and cited concepts.
- Preserve important quantitative claims from the source, such as "发表论文 90 余篇", "转载 20 余次", "主持国家社会科学基金重大项目", unless they are duplicated or visibly inconsistent.
- Preserve representative works with Chinese book-title marks. Keep publication year and publisher when provided.
- Preserve distinctive concepts and frameworks in quotation marks, such as "政府间网络治理", "政治性馈赠", "田野政治学", "用户友好型政府".
- If a source contains long lists of publications or honors, extract the academic views behind those works and cite only the representative or high-signal items. Summarize the rest as evidence of sustained work in that area unless the user asked for a full bibliography.
- If information is missing, omit it. Do not invent birth years, positions, awards, publication counts, or scholarly influence.

## Writing Rules

- Avoid evaluative embellishment beyond the source. Phrases like "产生重要影响" are acceptable only when supported by the source.
- Use the scholar's name or surname plus professional title for clarity; avoid overusing "该学者".
- Convert obvious OCR or spacing artifacts into clean Chinese typography, but do not silently change substantive facts.
- Merge heading fragments into sentences. For example, change "在政府应急管理方面。其研究经历了..." to "在政府应急管理方面，其研究经历了..."。
- When source material uses "一是、二是、三是" to organize contributions, either keep that structure inside a paragraph or rewrite it as flowing prose; do not turn it into visible subheadings.
- Keep political and institutional terms exact, especially names of Party, state, ministry, university, journal, fund, and award entities.
- Avoid publication-list prose such as "其论文包括A、B、C、D". Replace it with analytical prose such as "围绕某问题，他/她从A机制、B条件和C后果三个方面解释了..." and mention only the most representative works.
- Do not equate journal rank, publication count, or project level with academic contribution. Use them after explaining the contribution, not before it.
- Make each academic paragraph answer at least one of these questions: What concept did the scholar propose? What mechanism did they explain? What conventional view did they revise? What Chinese experience did they theorize? What policy or governance problem did they clarify?

## Fact Handling

- Treat the user's provided text as the main source.
- If the user asks for the latest/current status, or asks you to supplement missing facts about a living scholar, verify with reliable current sources before adding new information.
- When sources conflict, state the uncertainty briefly or use only the fact that can be supported by the provided material.
- Do not include citations or source notes unless the user asks for them.

## Final Check

Before answering, check that the output:

- contains the scholar name;
- has no invented section headings;
- covers履历、学术侧重面、代表性成果与成就;
- explains the scholar's main academic views instead of merely listing papers;
- uses representative publications and projects as evidence for those views;
- preserves the strongest concrete evidence from the source;
- is not a bullet list unless the user explicitly requested bullets;
- does not add unsupported biographical or academic claims.
