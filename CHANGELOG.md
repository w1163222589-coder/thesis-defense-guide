# Changelog

All notable changes to **Thesis Defense Guide**. This skill moved from a linear manual generator (v0.1.3) to an adversarial, paradigm-adaptive defense simulator (v0.5.0).

## [0.5.0] — 2026-06-07
### Added
- **Evaluator research protocol** (`references/evaluator-research-protocol.md`): paradigm-appropriate source hierarchy, evidence grading (High/Med/Low), an anti-fabrication verification gate, **committee-list/supervisor verification**, and a graceful "thin research → paradigm archetype" fallback.
### Changed
- Slimmed legacy `style-rubric.md` (160→47 lines) and `manual-structure.md`; methodology de-duplicated and pointed to the canonical framework files.
- `SKILL.md` → v0.5.0; Stage 2 now runs the research protocol.

## [0.4.0] — 2026-06-07
### Added
- **Discipline-adaptive layer** (`references/discipline-profiles.md`): six paradigm families (empirical-quant, empirical-qual, theoretical-formal, textual-interpretive, doctrinal-normative, design-creative) + a mixed handler. The skill now works for **any discipline**, not just STEM.
- IRON RULE **IR-0 (paradigm-adaptive)**; Stage 0 = paradigm detection.
### Changed
- Neutralized the engine files (weakness audit, readiness rubric, question rules) so "evidence" and "rigor" mean the right thing per field; removed STEM-only assumptions (baselines/ablations/p-values) from the universal layer. PPT audit made optional (humanities/law vivas).

## [0.3.0] — 2026-06-07
### Added
- **Mock-defense protocol** (`references/mock-defense-protocol.md`): interactive examiner with **Attack-Intensity-Preservation** — 1–5 answer scoring, escalation ladder, anti-sycophancy (no consecutive concessions, concession-rate tracking), persona switching, drill log.
- **PPT audit checklist** (`references/ppt-audit-checklist.md`): per-slide overclaim scan, "stop-risk" slides, figure readability, spoken-vs-written consistency, backup-slide planning.

## [0.2.0] — 2026-06-06 — Architecture overhaul
### Added
- **Generator/evaluator split** (the core fix): a standalone, evaluator-blind **Weakness Auditor** commits a read-only **Weakness Ledger** before any answer is written, so attacks aren't quietly softened.
- **Weakness→question reverse-engineering** with severity ranking and a **Top-10 most-dangerous** list (robust even when evaluator research is thin).
- **0–100 readiness score** with exposure tiers; **risk-tiered output** led by a day-of one-pager.
- New reference files: weakness-audit, question-generation, answer-coaching, readiness-rubric.
### Changed
- Anti-overclaiming converted from prose into **IRON RULES** + post-draft self-checks.
- `SKILL.md` rewritten lean (≈226→125 lines); detail pushed into `references/`.

## [0.1.3] — prior baseline
- Linear 3-phase manual generator: thesis intake & risk reading → committee research & mapping → manual generation.
- Thesis risk radar, claim calibration table, evaluator-thesis mapping matrix, stage-aware questions, 10/30/60-second oral answers, personalized red-line phrases, DOCX export.
