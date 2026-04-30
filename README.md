# Brennan & Hale Audio — MGMT 494BI Midterm Makeup Exam

**Live URL:** https://jazzjabu1939.github.io/bh-audio-makeup/
**Course:** MGMT 494BI: Business Policy & Strategy · Isenberg School of Management · UMass Amherst
**Access Code:** BH494

---

## Overview

A branching exam styled after the Hartwell case architecture. Students read the Brennan & Hale Audio case and navigate four strategic situations (Alpha through Delta). At each situation, they choose between two strategic paths — both defensible — then answer 5 MCQs testing their understanding of that path's logic.

**Total questions in bank:** 40 (8 paths × 5 questions)
**Questions answered per student:** 20 (1 path × 5 Qs × 4 situations)
**Scoring:** 5 points per correct answer = 100 points total
**Time limit:** 45 minutes (starts at Situation Alpha; timer visible in header)

---

## Branching Structure

| Situation | Path A | Path B |
|-----------|--------|--------|
| **Alpha** — Value Creation | The Craft Story | The Community Story |
| **Beta** — Channel Strategy | D2C Hybrid | Double Down on Dealers |
| **Gamma** — Brand Protection | Decline Apex | Accept Apex (with guardrails) |
| **Delta** — Five Forces | Audiophile $1,500+ | Connected Home $500+ |

There are **16 possible path combinations** (2⁴ = 16). All paths yield 20 questions and a 100-point exam. The choice of path is not graded — students are told this explicitly before each situation.

---

## Files

| File | Description |
|------|-------------|
| `index.html` | Complete exam — all 40 questions + branching UI |
| `ANSWER_KEY.md` | Full answer key with all choices and explanations |
| `ANSWER_KEY_SUMMARY.md` | Compact answer grid (8 paths × 5 Qs) + concept index |
| `audio/community-story.mp3` | Laura (ElevenLabs) narration — Alpha: Community Story path |
| `audio/double-down-dealers.mp3` | Laura narration — Beta: Double Down on Dealers path |
| `audio/accept-apex.mp3` | Laura narration — Gamma: Accept Apex path |
| `audio/connected-home.mp3` | Laura narration — Delta: Connected Home $500+ path |

> **Note:** Audio narrations are provided for the four "new" (non-original) paths only.
> The four original paths (Craft Story, D2C Hybrid, Decline Apex, Audiophile $1,500+)
> can be given audio narrations in a future update if desired.

---

## Setup Before Administering

1. **Google Form:** Create a Google Form with fields for Student ID, Session ID, Path Taken, Score, Percentage, and Answers. Copy the form URL into `index.html` under `const FORM_URL = "..."`. Also fill in the `FORM_ENTRY` field IDs.
2. **Access Code:** Currently `BH494` — change in `index.html` under `const ACCESS_CODE` if needed.
3. **Timer:** Currently 45 minutes. Change `const TIME_LIMIT_SECONDS = 45 * 60` if needed.

---

## Technical Notes

- Single-file app: no build step, no server required — GitHub Pages serves directly
- JS validates cleanly (`new Function(...)` test passes)
- Timer starts when student clicks "Begin Situation Alpha" from the case screen
- Each situation locks answers when student clicks "Confirm Answers & Continue" — no going back
- Results screen shows path taken (e.g., `Craft Story › D2C Hybrid › Decline Apex › Audiophile Segment ($1,500+)`)
- Google Form submission is no-op if `FORM_URL` is empty (console warning only)

---

## Question Authorship Notes

**Original paths** (tested in prior in-class exam): Craft Story, D2C Hybrid, Decline Apex, Audiophile $1,500+
- Questions Q1–Q20 carry over from the original linear exam. Vetted by Prof. Langenkamp.

**New opposite paths** (added in this build): Community Story, Double Down on Dealers, Accept Apex, Connected Home $500+
- 20 new questions written to match the depth and distractor style of the original 20.
- All distractors are paragraph-length and self-explain why they're wrong, naming the specific conceptual error.
- Concepts tested: value creation/capture, isolating mechanisms, activity-system complementarity, brand extension theory, signal-chain integrity, brand-protection mechanisms, Five Forces industry definition, buyer power, substitute pressure, rivalry.

---

*Built by Thea (OpenClaw) · April 30, 2026 · For Prof. Langenkamp · MGMT 494BI Fall 2026*
