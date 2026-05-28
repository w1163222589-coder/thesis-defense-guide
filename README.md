# Thesis Defense Guide Skill

A Codex skill for creating thesis and dissertation defense preparation guides.

It researches committee members, maps evaluator interests to the user's thesis, identifies risky thesis claims, and produces practical Q&A rehearsal materials with stage-aware defense strategy and anti-overclaiming guardrails.

## What It Produces

- evaluator profiles and evidence notes
- thesis fact sheet
- thesis risk radar
- claim calibration table
- evaluator-thesis mapping matrix
- committee-specific likely questions
- 10/30/60-second oral answer scripts
- chain follow-up scripts
- personalized red-line phrases
- polished Word `.docx` output from Markdown

## Required Inputs

Before generating a guide, the skill requires:

1. the user's thesis or defense materials,
2. the committee/evaluator list,
3. the specific school, university, college, or program context.

## Installation

Copy this folder into your Codex skills directory:

```text
C:\Users\<you>\.codex\skills\thesis-defense-guide
```

Restart Codex after installing the skill.

## Word Output

The bundled converter can turn a generated Markdown guide into a styled Word document:

```powershell
python scripts\markdown_to_docx.py --input defense-guide.md --output defense-guide.docx --title "Thesis Defense Q&A Guide"
```
