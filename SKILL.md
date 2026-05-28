---
name: thesis-defense-guide
description: "Create thesis/dissertation defense preparation guides by researching committee members, mapping their research interests to the user's thesis, adapting to the defense stage, and producing practical rehearsal materials with anti-overclaiming guardrails. Use when the user asks to prepare for a thesis defense, dissertation defense, viva, proposal defense, midterm defense, pre-defense, committee Q&A, likely reviewer questions, evaluator-specific questions, risk analysis, oral answer scripts, or a polished Word/PDF defense manual. Before working, require three inputs: the user's thesis or defense materials, the committee/evaluator list, and the specific school/university/college/program context."
---

# Thesis Defense Guide

Use this skill to produce a committee-by-committee defense manual: evaluator profiles, thesis risk radar, evaluator-thesis mapping matrix, stage-aware likely pressure questions, question intent, oral answer scripts, bonus points, chain follow-ups, personalized red-line phrases, anti-overclaiming guardrails, rehearsal controls, and a polished `.docx` guide.

## Required Inputs

Do not start substantive research or drafting until these three inputs are present:

1. The user's thesis or defense materials.
   - Accept PDF, DOCX, PPTX, Markdown, text, or a folder containing drafts/slides.
2. The committee/evaluator list.
   - Require names. Prefer title, department/team, and role if available.
3. The specific institution context.
   - Require school/university name; prefer college, program/discipline, team/lab, and defense language.

If anything is missing, ask a concise question for only the missing item(s). Example:

> Please provide the thesis file, the committee member names, and the specific school/college context before I build the guide.

## Optional Context To Capture

After the required inputs are present, ask for optional context only when it would materially change the guide. Do not block work if the user cannot provide it.

- Defense stage: proposal, midterm, pre-defense, final defense, viva, or committee review.
- Defense language and expected tone: Chinese, English, bilingual, formal, concise, or conversational.
- Time limits: presentation length, Q&A length, slide count, and whether there is a strict chair.
- Relationship context: same lab, cross-team, external examiner, industry evaluator, known friendly/challenging member.
- Known weak points: the student's own worries, prior feedback, rejected claims, missing experiments, or advisor warnings.
- Output preference: Markdown, Word, PDF, or a short rehearsal sheet in addition to the full manual.

## Workflow

### 1. Intake And Scope

- Confirm the thesis file(s), committee names, and school context.
- Identify whether the output should be Markdown, Word, PDF, or all of them.
- Capture optional context when useful, especially defense stage, language, time limits, known weak points, and relationship context.
- If the defense stage is unknown, infer a conservative default from the user's words; otherwise use final defense/viva assumptions and state that assumption in the guide.
- Apply stage-specific emphasis:
  - Proposal defense: emphasize problem value, research gap, feasibility, technical route, expected contribution, risk control, and whether the scope is realistic.
  - Midterm defense: emphasize progress against plan, completed evidence, unfinished work, timeline risk, methodological corrections, and whether the remaining work can be finished.
  - Pre-defense: emphasize thesis structure, contribution clarity, experiment completeness, missing comparisons, claim wording, publication/format issues, and committee-ready revisions.
  - Final defense or viva: emphasize contribution boundary, evidence credibility, novelty, limitations, academic rigor, reproducibility, and whether conclusions are overstated.
  - Committee review without a live defense: emphasize written evidence, source traceability, argument structure, compliance, and reviewer objections that must be answered in writing.
- Choose a practical research depth. Use a standard public-source pass by default; do a deeper bibliographic pass only when the user asks for exhaustive evaluator research.
- If the user asks for Word, plan to produce both a source `.md` and a polished `.docx`.

### 2. Read The Thesis

- Extract the thesis title, abstract, contributions, methods, experiments, limitations, and future work.
- Preserve the user's actual technical claims. Do not invent claims to make answers sound stronger.
- Create a compact thesis fact sheet with: core problem, claimed contribution, method, evidence, main limitation, and safest one-sentence positioning.
- Identify claim-evidence mismatches. For every central claim, note what evidence supports it, what evidence is missing, and how narrowly the student can defend it.
- Flag high-risk thesis boundaries, such as:
  - no real-world experiment,
  - ideal assumptions,
  - missing ablations,
  - missing fairness comparisons,
  - heuristic optimization without proof,
  - limited data/model scope.
- Enforce anti-overclaiming rules:
  - Do not present simulations as real-world deployment evidence.
  - Do not present correlation, trend, or case observation as causality.
  - Do not present a small or local experiment as universal effectiveness.
  - Do not present a proposed extension or future work as an already completed contribution.
  - Do not hide missing baselines, missing ablations, limited datasets, unverified assumptions, or failed/negative results.
  - Do not convert weak evidence into confident language just to make the student sound stronger.
  - If the thesis is weak on a point, give a controlled concession plus a defensible boundary, not a forced justification.
- Produce a thesis risk radar table with:
  - risk or vulnerable claim;
  - evidence currently available in the thesis;
  - why a committee member may challenge it;
  - likely evaluator(s);
  - safest stance: defend, qualify, concede, or redirect;
  - safer wording the student can use aloud.

For PDFs, use the local PDF skill/tooling when available. For PPTX/DOCX, use appropriate local extraction tools.

### 3. Research Each Evaluator

Browse current public sources when researching real people. Use official institution pages first, then papers, lab/team pages, institutional repositories, student thesis lists, Google Scholar/Crossref/IEEE/ACM/MDPI/Springer pages, and conference pages as needed.

For each evaluator, collect:

- official title, department/team, email/page if public;
- confirmed research directions;
- recent journal/conference paper themes;
- student thesis/dissertation themes when publicly available;
- recurring methods, datasets, systems, and metrics;
- likely evaluation style inferred from confirmed work.

Keep attribution disciplined:

- Separate "officially confirmed" from "inferred from paper themes".
- Never invent student theses or publications.
- If student theses are not publicly found, say so.
- Include source links in the final guide or appendix.
- Mark evidence strength for profile claims:
  - High: official homepage/CV/lab page or directly verified publication record.
  - Medium: repeated themes across recent papers, projects, or student outputs.
  - Low: field-adjacent inference that is plausible but not directly confirmed.

### 4. Map Evaluators To The Thesis

For each evaluator, connect their work to the user's thesis:

- What part of the thesis they will understand deeply.
- What assumptions they may challenge.
- What adjacent method they may compare against.
- What "identity pressure" may arise if the user is from a different lab/team.
- What answer stance is safest: defend, qualify, concede, or redirect to future work.
- Create an evaluator-thesis mapping matrix with columns for evaluator, research attention, thesis chapter/claim they may inspect, likely pressure point, evidence strength, and recommended answer stance.
- Keep the matrix short enough to review before the defense; put detailed evidence in evaluator sections or the appendix.
- Adjust the pressure point by defense stage. For example, a proposal evaluator may ask "Why is this route feasible?", while a final-defense evaluator may ask "What evidence proves this conclusion under your stated assumptions?"

### 5. Write The Manual By Evaluator

Organize the guide primarily by committee member. For each evaluator, use this structure:

1. Evaluator profile card.
   - Name / title.
   - Confirmed core research directions.
   - Representative work or recent themes.
   - Student thesis themes if publicly found.
   - Evidence strength and source notes.
2. Potential concern callout.
   - Write a short paragraph beginning with `【Potential concern】` or `【潜在关切点】`.
   - Explain why this evaluator may challenge the user's thesis.
3. Stage-aware high-probability questions.
   - Make the same evaluator's questions fit the defense stage.
   - For proposal defense, focus questions on research value, novelty, feasibility, route selection, and expected validation.
   - For midterm defense, focus questions on actual progress, incomplete work, feasibility of finishing, risk mitigation, and whether the method has changed.
   - For pre-defense, focus questions on thesis structure, missing evidence, contribution phrasing, experiment completeness, and revision priorities.
   - For final defense/viva, focus questions on evidence credibility, contribution boundary, limitation handling, theoretical or empirical rigor, and generalization.
   - For every question, include:
     - `▶ Question intent` / `▶ 问题意图`
     - `▶ Reference answer` / `▶ 参考回答`
     - `▶ 10-second answer` / `▶ 10秒回答` when a short reply is useful
     - `▶ 30-second answer` / `▶ 30秒回答` for the normal spoken answer
     - `▶ 60-second answer` / `▶ 60秒回答` when the issue is complex
     - `▶ Bonus point` / `▶ 加分点` when useful
     - `▶ If challenged further` / `▶ 若被追问` when useful
4. Chain follow-up script.
   - Make follow-ups progressively harder: concept check, assumption challenge, evidence challenge, limitation pressure, future-work or feasibility challenge.
5. Final defensive bottom line.

When there are five evaluators, create five major sections. Do not scatter one evaluator's questions across multiple global sections unless the user explicitly asks for a different format.

Recommended question-answer style:

- Use direct, speakable answers, not thesis prose.
- Include a safe first sentence.
- Admit real limitations clearly.
- Give a next-step research direction only after answering the question.
- Avoid overclaiming.
- Prefer bounded verbs and nouns: "indicates", "supports", "under this setting", "within the dataset", "in this thesis", "preliminary evidence", "future validation".
- Avoid absolute language unless the thesis truly proves it: "proves", "guarantees", "always", "fully solves", "optimal", "cannot fail", "real-world validated".
- Make each answer feel like something the student can say aloud in 20-60 seconds.
- Include a "bonus point" when a short extra sentence would impress the evaluator.
- Include a "if interrupted" short fallback for high-risk questions when useful.

### 6. Add Universal Defense Controls

After evaluator-specific sections, add a short universal section only if useful:

- answer templates for admitting limitations;
- personalized phrases not to say, based on the thesis claims and weak evidence;
- safer replacement wording for risky claims;
- a claim calibration table: original thesis wording, evidence level, risk of overclaiming, safer defense wording;
- final "if cornered" answer;
- a 30-second defense summary.
- a one-page rehearsal sheet with the thesis contribution, three controlled limitations, three safest answers, and the most likely evaluator-specific pressure points.

Keep this secondary to the evaluator sections.

### 7. Produce Word Output

If the user asks for Word, create a polished `.docx`.

- First write a Markdown source file.
- Then run `scripts/markdown_to_docx.py` to generate a styled Word file.
- Validate that the `.docx` is a valid zip/OpenXML package and non-empty.

Example:

```powershell
python "$env:CODEX_HOME/skills/thesis-defense-guide/scripts/markdown_to_docx.py" `
  --input "defense-guide.md" `
  --output "defense-guide.docx" `
  --title "Thesis Defense Q&A Guide"
```

If `$CODEX_HOME` is unset, use `C:/Users/<user>/.codex/skills/thesis-defense-guide/scripts/markdown_to_docx.py` or locate the skill folder from the loaded skill path.

## Quality Bar

The final guide should be useful under real defense pressure:

- The opening should include background and usage instructions, especially any cross-team/lab identity risk.
- The guide should explicitly state the assumed defense stage and adapt question emphasis to that stage.
- Include a thesis fact sheet, risk radar, and evaluator-thesis mapping matrix before the evaluator sections unless the user asks for a very short guide.
- Questions should feel like committee members are asking from their own research background.
- Questions should not be generic across stages; proposal, midterm, pre-defense, and final defense pressure should feel different.
- Every major evaluator section should start with a compact profile and a `【潜在关切点】` callout.
- Most questions should include a `▶ 问题意图` block before the answer.
- Answers should be concise enough to say aloud, with 10/30/60-second variants for high-risk questions.
- Include `▶ 加分点` where a one-sentence add-on can raise the answer quality.
- Chain follow-ups should get progressively harder.
- Weaknesses should be framed honestly, not hidden.
- The manual must not over-defend weak thesis claims. If evidence is thin, the answer should qualify, concede, or redirect instead of inflating the claim.
- Any claim stronger than the thesis evidence should be rewritten into safer, stage-appropriate language.
- Evidence-based claims about evaluators should be labeled or worded according to evidence strength.
- Red-line phrases should be customized to the thesis, not only generic.
- The Word document should be easy to skim during practice: clear sections, highlighted questions, answer boxes, and page breaks by evaluator.

## Bundled Resources

- `scripts/markdown_to_docx.py`: convert the generated Markdown manual into a styled `.docx`.
- `references/manual-structure.md`: detailed structure for evaluator-by-evaluator manuals.
- `references/style-rubric.md`: sample-informed style and quality rubric for defense manuals.
