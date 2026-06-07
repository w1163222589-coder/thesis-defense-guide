---
name: thesis-defense-guide
description: "Create thesis/dissertation defense preparation guides for any discipline (sciences, engineering, social science, humanities, law, the arts) by detecting the thesis's research paradigm and adapting its standards. Runs an adversarial, evaluator-agnostic weakness audit of the thesis and slides (Three Lenses + Devil's-Advocate dimensions + severity), reverse-engineers the likely committee questions from those weaknesses, drafts bounded anti-overclaiming oral answers, scores defense readiness (0-100), and ships risk-ordered rehearsal output (day-of one-pager + per-evaluator battle cards + full Word manual). Also researches committee members to re-weight and personalize questions. Use when the user asks to prepare for a thesis defense, dissertation defense, viva, proposal/midterm/pre-defense, committee Q&A, likely reviewer questions, evaluator-specific questions, thesis weak points, risk analysis, mock defense, oral answer scripts, or a polished defense manual. Before working, require three inputs: the user's thesis or defense materials, the committee/evaluator list, and the specific school/university/program context."
metadata:
  version: "0.5.0"
  last_updated: "2026-06-07"
---

# Thesis Defense Guide

Produce a rehearsal-ready defense package by, in order: (1) auditing the thesis and slides for weaknesses **independently of who is on the committee**, (2) reverse-engineering the questions a committee derives from those weaknesses, (3) coaching bounded, speakable answers that never overclaim, (4) researching evaluators to re-weight and personalize, and (5) shipping risk-ordered output led by a day-of one-pager and a 0–100 readiness score.

## Required Inputs

Do not start substantive research or drafting until all three are present:

1. The thesis or defense materials (PDF, DOCX, PPTX, Markdown, text, or a folder of drafts/slides).
2. The committee/evaluator list (names required; prefer title, department/team, role).
3. The specific institution context (school/university required; prefer college, program/discipline, lab, defense language).

If anything is missing, ask only for the missing item(s):
> Please provide the thesis file, the committee member names, and the specific school/program context before I build the guide.

## Optional Context (capture only if it changes the guide)

Defense stage (proposal/midterm/pre-defense/final/viva/written review); language and tone; time limits (talk length, Q&A length, slide count, strict chair?); relationship context (same lab, cross-team, external/industry examiner); known weak points (the student's worries, advisor warnings, prior rejected claims); **prior-year questions from the same lab/committee** (high-signal — ask for these); output preference.

---

## IRON RULES (apply throughout; re-read at every stage transition)

- **IR-0 Paradigm-adaptive.** Detect the thesis's paradigm at Stage 0 (`references/discipline-profiles.md`) and judge evidence, rigor, and questions by *that paradigm's* standards. Never apply experiment-style expectations (baselines, ablations, reproducibility, p-values) to interpretive, doctrinal, or creative work — or vice-versa.
- **IR-1 Generator/evaluator split.** The weakness audit (Stage 1) is committed **before** any answer is written. The attacker voice and the answer voice are different passes. See `references/weakness-audit-framework.md`.
- **IR-2 Read-only ledger.** Later stages may cite Weakness Ledger IDs but never soften, merge, or delete them. An answer must not claim a logged weakness is gone.
- **IR-3 Weakness-first questions.** Every predicted question traces to a weakness (or the universal backbone). Never drop a CRITICAL weakness because no evaluator obviously "owns" it.
- **IR-4 No overclaim.** Never sell simulation as real-world proof, correlation as causation, a narrow result as universal, or future work as a finished contribution. Prefer bounded verbs.
- **IR-5 No fabrication (anti-leakage).** Cite a concrete location for every weakness; mark true gaps as `[MATERIAL GAP]`. Never invent an evaluator's papers, students, or "the question Prof. X will ask" without evidence. Separate confirmed facts from inference and label evidence strength (High/Med/Low).
- **IR-6 Honest over kind.** Surface exposure plainly; a careful concession beats an inflated defense. Frame the readiness tier as *where to prepare*, not a verdict.

---

## Roles (named passes; keep them separated)

| Role | Job | Detail file |
|---|---|---|
| Thesis Weakness Auditor | adversarial, evaluator-agnostic audit of thesis **and slides** → Weakness Ledger | `references/weakness-audit-framework.md`, `references/ppt-audit-checklist.md` |
| Evaluator Profiler | research each evaluator, evidence-graded, gaps flagged, panel verified | `references/evaluator-research-protocol.md` |
| Threat Mapper | weakness × evaluator; re-weight question backbone | this file, Stage 3 |
| Question Generator | weaknesses → questions, escalation ladder, Top-10 | `references/question-generation-rules.md` |
| Answer Coach | bounded layered answers, stance by severity | `references/answer-coaching-framework.md` |
| Mock-Defense Examiner | interactive drill; attack-intensity-preserving; scores answers and escalates | `references/mock-defense-protocol.md` |
| Synthesizer / Prioritizer | readiness score + risk-tiered output + one-pager | `references/readiness-rubric.md`, `references/manual-structure.md` |

**All roles read `references/discipline-profiles.md`** for the detected paradigm's lens — what counts as evidence, the evaluator archetypes, and the rigor standard for that field.

---

## Workflow

### Stage 0 — Intake & paradigm detection
Confirm the three inputs. **Detect the research paradigm** (empirical-quant / empirical-qual / theoretical-formal / textual-interpretive / doctrinal-normative / design-creative / mixed) via `references/discipline-profiles.md`, and load its lens (evidence standards, evaluator archetypes, rigor definition). State the detected paradigm and invite correction ("Detected paradigm: …; tell me if this is wrong"). Capture time budget, known weak points, prior-year questions, and whether the defense uses slides. Decide output set (one-pager always; Word if asked). **Checkpoint:** confirm paradigm, scope, and evaluator list before deep work.

### Stage 1 — Weakness audit  ★ keystone, evaluator-blind
Run `references/weakness-audit-framework.md` on the thesis **and** slides. Produce the **Weakness Ledger** (severity-ranked, location-cited, read-only). Do NOT look at the committee list yet (IR-2/W2). Do NOT write any answers (IR-1/W3).
**1.5 Self-check:** run the framework's calibration footer; lead with the single most dangerous flaw.

For PDFs use local PDF tooling; for PPTX/DOCX use appropriate extraction. If the defense uses slides, audit them with `references/ppt-audit-checklist.md` (pacing, per-slide overclaim, stop-risk slides, figure readability, spoken-vs-written consistency, backup slides) and merge slide weaknesses into the Weakness Ledger; skip this if there are no slides (common in humanities/law vivas).

### Stage 2 — Evaluator research
Run `references/evaluator-research-protocol.md`: a paradigm-appropriate source hierarchy (official page → discipline index → recent themes), evidence grading **High/Med/Low**, the anti-fabrication discipline (IR-5), and **panel verification** — cross-check the committee against the thesis's official record (cover page / notice), and identify the **supervisor** (who usually does not cross-examine their own student).
**2.5 Verification gate:** before any evaluator claim enters the guide, confirm it is sourced or downgrade it; thin (Low / not-found) members are treated by paradigm **archetype**, never by invented specifics.

### Stage 3 — Threat mapping
Map each weakness to the evaluator *type* most likely to raise it (methodology / domain / application / adversarial). Where High/Med-confidence research binds a real person to a type, re-weight their questions up. Keep the matrix short; detail goes to evaluator sections.

### Stage 4 — Question generation
Run `references/question-generation-rules.md`: weaknesses → questions, 3-level escalation ladder (+ a "cornered" turn for CRITICALs), evaluator-type tags, stage-aware emphasis. Output the **Top-10 Most Dangerous Questions**.

### Stage 5 — Answer coaching
Run `references/answer-coaching-framework.md`: 4-move answers, layered 10/30/60-second, stance by severity (CRITICAL→concede+redirect, MAJOR→qualify, MINOR→defend), claim calibration table, thesis-specific red-line phrases. Honor the ledger (IR-2).

### Stage 6 — Mock defense (interactive; recommended)
Run `references/mock-defense-protocol.md`: a live drill where the simulated examiner **keeps attack intensity** — scores each answer 1–5, escalates the ladder on ≤3, never concedes on persistence alone, and switches persona to the assigned evaluator. Exam mode (hard) vs coach mode (Socratic). Log fumbles, feed them back into Top-10 ranking and the D6 readiness score, and debrief with model answers.

### Stage 7 — Synthesis, scoring & output
Score readiness with `references/readiness-rubric.md` (0–100 + tier + Top-3 exposures). Assemble the risk-ordered tiers below. **Checkpoint:** confirm before generating the heavy Word manual.

### Re-entry
After the thesis/PPT is revised, re-run **Stage 1.5 + Stage 6 only** (re-review): did the fixes close the logged weaknesses? Re-score and show the delta.

---

## Output organization (ship by risk, not by completeness)

Default first deliverable is **Tier A**. Generate lower tiers on request or when time allows.

- **Tier A — Day-of one-pager:** thesis one-sentence positioning; readiness score + Top-3 exposures; **Top-10 dangerous questions** with 30-second answers; 3 CRITICAL concession lines.
- **Tier B — Per-evaluator battle cards:** evidence-graded profile + that evaluator's 3–5 signature questions + answers + the one trap to avoid. Begin each with a `【潜在关切点】 / Potential concern` callout.
- **Tier C — Weakness radar & calibration:** severity-ranked Weakness Ledger + claim calibration table + stance per weakness.
- **Tier D — Mock-defense log:** drill transcripts; fumbles and re-prioritization.
- **Tier E — Full Word manual:** the complete by-evaluator manual per `references/manual-structure.md` and `references/style-rubric.md`.

Use the labels the converter highlights: `【潜在关切点】 ▶ 问题意图 ▶ 10秒回答 ▶ 30秒回答 ▶ 60秒回答 ▶ 加分点 ▶ 若被追问 老师： 你：`.

## Word output

If the user wants Word: write the Markdown source first, then run the converter, then validate the `.docx` is a non-empty OpenXML package.

```powershell
python "scripts/markdown_to_docx.py" --input "defense-guide.md" --output "defense-guide.docx" --title "Thesis Defense Q&A Guide"
```
(Locate the script from the loaded skill path; `$CODEX_HOME/skills/thesis-defense-guide/scripts/...` if set.)

## Quality bar (summary; detail in the reference files)

Lead with the single most dangerous question. Questions must feel committee-specific and stage-specific, and must trace to weaknesses. Answers must be speakable in their stated time, concede real limits, and never overclaim. Evaluator claims must be labeled by evidence strength. The readiness score must be consistent with the number of CRITICAL weaknesses. The one-pager must be usable under real pressure.

## Bundled resources

- `references/discipline-profiles.md` — paradigm-adaptive lens (6 families) that makes the skill work for any discipline; read first at Stage 0.
- `references/weakness-audit-framework.md` — Three Lenses + Devil's-Advocate dimensions + severity → Weakness Ledger (Stage 1).
- `references/ppt-audit-checklist.md` — slide-level audit: per-slide overclaim, stop-risk slides, backup slides (Stage 1).
- `references/evaluator-research-protocol.md` — paradigm-appropriate evaluator research, evidence grading, panel verification (Stage 2).
- `references/question-generation-rules.md` — weakness→question engine, escalation ladder, Top-10 (Stage 4).
- `references/answer-coaching-framework.md` — 4-move bounded answers, stance by severity, anti-overclaim (Stage 5).
- `references/mock-defense-protocol.md` — interactive, attack-intensity-preserving examiner; 1–5 scoring, escalation, drill log (Stage 6).
- `references/readiness-rubric.md` — 0–100 readiness score + tiers (Stage 7).
- `references/manual-structure.md` — full by-evaluator manual structure (Tier E).
- `references/style-rubric.md` — style/quality rubric and highlight labels.
- `scripts/markdown_to_docx.py` — Markdown → styled `.docx`.
