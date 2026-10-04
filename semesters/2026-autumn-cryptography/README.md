# 2026 Autumn Semester · Vol. 1: Codes, Communications & Computation

> Core question: **How do you keep a secret — and create trust — when the enemy is watching?**
> Journal storyline: frequency analysis → Enigma → Turing → RSA → TLS.
> Full 16-week plan, weekly reading tasks & links, workshop scripts and the Toolkit manual: see [`weekly-plan.md`](weekly-plan.md) (Chinese for now).

## 16-week overview

| Wk | Seminar topic | Deliverables | Owners |
|----|---------------|--------------|--------|
| 1 | Launch + Caesar cipher workshop | Role confirmation sheet; repo tour; one Caesar message per member | All |
| 2 | Caesar's Gallic dispatches (c. 58 BCE) | Essay #1; master timeline draft | S1, V |
| 3 | Al-Kindi & frequency analysis (9th c.) | Essay #2; Toolkit B1 draft; frequency-breaking micro-workshop | S2, K |
| 4 | 1586: the Babington Plot (Mary, Queen of Scots) | Essay #3; Source P1 (al-Kindi excerpt); Problem 1 | S1, T, N |
| 5 | Sunzi Suanjing & the Chinese Remainder Theorem | Essay #4; Toolkit B2 draft | S2, K |
| 6 | 1914: the radio plain-text disasters | Essay #5; Source P2; Problem 2 | S1, T, N |
| 7 | 1939: Poland hands over the Enigma breaks | Essay #6; Feature §1–2 draft | S2, Editor |
| 8 | May 1941: the U-110 capture + "human bombe" game | Essay #7; Toolkit B3; Problem 3 | S1, K, N |
| 9 | Ultra: decoded, but you can't always act | Essay #8; Case C2; Feature §3–4 | S2, Editor |
| 10 | 1976–77: the public-key revolution (DH handshake demo) | Sources P3 & P4 excerpts; Toolkit B4; Feature §5–7 | All, T, K |
| 11 | Peer review (language and logic only) | Revised essays/toolkits | All |
| 12 | Teacher feedback on the Feature | Pre-final Feature revision | Editor + teacher |
| 13 | Compile journal PDF / launch slides | Vol. 1 draft | Editor, V |
| 14 | Fact & formula check (against source cards) | Final figures + errata | Editor, V |
| 15 | Launch-day rehearsal (20 min) | Published PDF | All |
| 16 | Publication; vote for next volume | Archive; 100-word reflection | All |

## Seven roles (signed off in Week 1)

| Code | Role & duties |
|------|---------------|
| E (Editor-in-chief) | Feature essay, final edit, problem-set review, bibliography, finished PDF |
| S1 (Narrator) | Essays #1, #3, #5, #7 |
| S2 (Narrator) | Essays #2, #4, #6, #8 |
| K (Toolkit author) | Toolkits B1–B4 (AS maths only) |
| T (Sources) | Primary-source translation + annotation (P1–P4) |
| N (Problem narrator) | "Historical hook" notes for Problems 1–3 |
| V (Visual editor) | Cover, diagrams, timeline |

## Folder guide

| Folder | Contents |
|--------|----------|
| `weeks/week-NN-*/` | Per-week agenda, notes, deliverables (`outputs/`) |
| `journal/essays/` | Historical essays |
| `journal/toolkits/` | Toolkits B1–B4 |
| `journal/feature/` | Feature: guide, `drafts/` → `final/` |
| `journal/figures/` · `problems.md` · `sources.md` | Figures, problem page, bibliography |
| `readings/` | Primary-source PDFs (DH 1976, RSA 1978, Bletchley worksheets) + reading list |
| `materials/` | Workshop props (cipher wheel) and the Cipher Challenge ciphertext archive |

## Semester rules

1. Drafts go to `weeks/week-NN-*/outputs/` first (naming: see `docs/writing-guide.md`); only revised finals enter `journal/`.
2. Week 11 peer review = open a Pull Request for each draft; comments fix language and logic only.
3. Spoiler red line: the official Cipher Challenge solution report and answer sheet are **never committed** — kept offline by the editor and the supervising teacher only.
4. Every draft ends with Sources (at least one primary account + one main textbook reference).
5. Week 14 fact check follows the source notes in `weekly-plan.md` Section 2 line by line; the "Coventry myth" must be stated per Hinsley's conclusion.
6. Only week folders that have already happened are pushed (`.gitignore` allowlist; add next week's `!` line after each meeting).
