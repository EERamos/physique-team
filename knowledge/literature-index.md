# Physique Team — Literature Index

Actionable summaries only (no long verbatim quotes). Full commercial book PDFs are **not** in this repo (copyright).

| # | Title | Author(s) | Year | Why it matters for recomp | KB file |
|---|--------|-----------|-----|------------------------------|------------|
| 1 | *Science and Development of Muscle Hypertrophy* | Brad Schoenfeld | 2016 | Mechanisms; volume/frequency/load/failure; selection; periodization; hypertrophy nutrition. Base for **training + progression**. | `schoenfeld-hypertrophy.md` |
| 2 | *The Renaissance Diet 2.0* | Israetel, Davis, Case, Hoffmann (RP) | ~2019–20 | Diet pyramid, kcal/macros, timing, cut/maint/bulk, tracking, adherence/hunger. Base for **nutrition + meal guide + tracker**. | `renaissance-diet-2.md` |
| 3 | *The Stubborn Fat Solution* | Lyle McDonald | 2008 | Regional physiology (α2/β2, blood flow); when special tactics vs normal deficit. Advanced lean-out only. | `stubborn-fat-mcdonald.md` |

## Evidence briefs (systematic reviews and consensus statements)

Topic files compiled 2026-10-13 from meta-analyses, systematic reviews and IOC/ISSN/ACSM consensus statements. Each file lists its primary sources with DOI and marks what was not checked against the original (see **Conventions** below).

| Topic | Primary sources | Used by | KB file |
|---|---|---|---|
| Training load monitoring: ACWR and 10% rule under dispute, sRPE, subjective measures | Maupin 2020; Schwellnus 2016 (IOC); Saw 2016; Haddad 2017 | Load & Recovery, Desk | `load-monitoring.md` |
| Sleep and post-exercise recovery techniques | Craven 2022; Dupuy 2018; Schwellnus 2016 (IOC) | Load & Recovery, Desk | `sleep-recovery.md` |
| Concurrent training: interference, order, separation | Petré 2021; Schumann 2022; Eddens 2018; Currier 2026 (ACSM) | Desk, Evidence Desk | `concurrent-training.md` |
| Body-fat measurement error by method, how to track change | Kasper 2021; Aragon 2017 (ISSN) | Desk (frame, tracker), Recomp Nutrition | `body-fat-measurement.md` |
| Relative Energy Deficiency in Sport (REDs) in men | Mountjoy 2023 (IOC), from notes | Desk, Recomp Nutrition | `energy-deficiency-reds.md` |
| Supplements with evidence and hydration | Maughan 2018 (IOC); Guest 2021 (ISSN) | Evidence Desk, Recomp Nutrition | `supplements-hydration.md` |
| Red flags: stop and refer to a doctor | Mountjoy 2023; Schwellnus 2022; Hew-Butler 2017; ACSM; ESC | All bots, Labs Prep | `medical-red-flags.md` |

## Operational synthesis

- `recomp-synthesis.md` — decision rules for the 8-prompt system (frame → training → nutrition → meals → progression → tracker → recovery → complete).
- `deep-research-evidence-base.md` — integrated brief + IF/THEN rules (evidence refresh ~2026).

## Use by Desk prompt

1. **Frame** — recomp vs cut vs lean gain (`recomp-synthesis` + RD2)
2. **Training** — Schoenfeld
3. **Recomp nutrition** — RD2
4. **Meal guide** — RD2
5. **Progression** — Schoenfeld + volume landmarks
6. **Tracker** — RD2 + `body-fat-measurement.md`
7. **Recovery** — Schoenfeld + RD2 adherence/hunger + `sleep-recovery.md` + `load-monitoring.md`
8. **Complete system** — `recomp-synthesis.md`

## Evidence Desk

Prefer dated claim + source + year bullets from these summaries; Physique Desk translates into the live plan.

## Conventions

How the bots read and cite this folder. Applies to every file in `knowledge/`.

- **Two speeds.** Day-to-day questions ("can I eat this?", "swap this exercise?") are answered from the live plan and general criteria, in two or three lines, without opening `knowledge/`. Open a KB file only when: building or changing the plan; a number, dose or range is needed that is not in the plan; the question is about a supplement; there is a symptom; or USER says "verify it".
- **Open only the file that applies.** Enter through this index, then read the one file the question needs. Cite it in one line.
- **Citation marks.** A citation with author and year and no mark was checked against the original. "(nota)" means it comes from research notes and was not checked: say so when you use it.
- **Not in the KB, no number.** If the KB does not cover it, say "not in the knowledge base" and do not invent the figure, dose or source.
- **Same method only.** Body-fat percentage is compared only against the same method and the same conditions. Never trend a BIA scale reading against a DXA scan. See `body-fat-measurement.md`.
- **Red flags win.** If a question touches anything in `medical-red-flags.md`, stop and refer. Do not adjust the plan to cover a warning sign.
