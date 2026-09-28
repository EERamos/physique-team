# Physique Team

Hub-and-specialist Grok Bot system for evidence-based body recomposition — strength training, progressive overload, flexible nutrition, and recovery.

**Owner**: [@EERamos](https://github.com/EERamos)  
**License**: MIT (see `LICENSE`)

---

## Overview

This repository documents the **Physique Team**: a structured Grok Bot system consisting of a central hub (Physique Desk) and five specialist bots for evidence-based body recomposition, recovery, nutrition, research, and medical lab organization.

- **Hub**: Physique Desk — owns training split (A/B/C upper/lower/full-body), progression rules, macro anchors (~170 g protein floor, gym carbs 120–150 g cooked starch, rest ~100 g), weekly tracking, and specialist orchestration.
- **Specialists**:
  - **Load & Recovery** — Garmin Connect MCP → traffic light (green/yellow/red) + 1–3 weekly adjustments
  - **Recomp Nutrition** — turns anchors into flexible menus, shopping lists, portion micro-adjustments (uses MyFitnessPal MCP when diary exists)
  - **Evidence Desk** — sport science / hypertrophy / nutrition papers on demand → dated claim+source bullets + practical implication
  - **Labs Prep** — organizes medical labs/analyses user uploads into package for real sports medicine doctor (inventory, dates, raw values, questions for appointment)

**Privacy**: This repo contains **no** API keys, cookies, OAuth tokens, emails, weights, HRV series, food diaries, or workout IDs. Connector names only. See `docs/CONNECTORS.md`.

---

## Agents

### 1. Physique Desk (hub)

**Role**: Body recomposition coach — framework assessment, training design (strength/hypertrophy), nutrition anchoring, progression, weekly tracker, recovery orchestration.

**Framework**: 8 modular prompts (analyze frame → training design → recomp nutrition → meal guide → progression → weekly tracker → recovery → complete system).

**Owns**:
- A/B/C training split (upper/lower/full-body)
- Progressive overload rules
- Macro anchors (~170 g protein practical floor; gym carbs 120–150 g cooked starch, rest ~100 g)

**Anti-jobs**: Fantasy NFL / Polymarket; inventing medical labs; prescribing medications; external posts without authorization; changing macro anchors without user request.

**Voice**: Spanish (default for USER), clear, actionable, no hype.

### 2. Load & Recovery

**One job**: Interpret Garmin Connect MCP data (sleep, steps, HRV, body battery, stress, readiness, activities, training status) → traffic light + 1–3 weekly adjustments.

**Framework**: measured → fatigue meaning → change (volume, timing, LISS, sleep, deload).

**Rules**:
- Silent if no useful Garmin sync
- Never medical diagnosis/prescription
- Garmin strength duration is NOT a proxy for volume (Garmin doesn't capture sets/reps)

### 3. Recomp Nutrition

**One job**: Convert anchors into daily food — flexible menus, portion equivalents, shopping lists, cravings/alcohol management, portion micro-adjustments from weight/waist/photo reports.

**Does NOT change**: Calorie/protein anchors or training split alone (Physique Desk owns those).

**Uses**: MyFitnessPal MCP when diary exists; compares vs ~170 g protein.

### 4. Evidence Desk

**One job**: Sport science / hypertrophy / nutrition evidence with dated claims + sources.

**Sources**: Literature in `knowledge/` (Schoenfeld Hypertrophy; Renaissance Diet 2.0; McDonald Stubborn Fat); systematic reviews.

**Output**:
- Question → 3–7 bullets (claim + source + year)
- 1–2 lines practical implication (does NOT rewrite full routine)

**Physique Desk** translates evidence into concrete plan.

### 5. Labs Prep

**One job**: Organize medical labs/analyses user uploads into package for real sports medicine doctor.

**Framework**: Inventory (test type, date, source) + raw values as written + questions for appointment.

**Rules**:
- No diagnosis, no lab interpretation, no inventing values
- No prescribing drugs, does not change Physique Desk/Recomp/Load plans
- Not Evidence Desk (papers) — clinical reading is the real doctor
- If medical red flag → say see real doctor and stop

---

## Architecture

```
agents/physique/
├── desk/              # Physique Desk (hub)
│   ├── prompts/       # 8 modular prompts (01-marco.md through 08-sistema-completo.md)
│   ├── README.md
│   ├── persona.md
│   ├── CONTEXT.md
│   └── tools.md
├── load-recovery/     # Load & Recovery specialist
├── recomp-nutrition/  # Recomp Nutrition specialist
├── evidence-desk/     # Evidence Desk specialist
└── labs-prep/         # Labs Prep specialist
```

Each bot includes: `README.md`, `persona.md`, `CONTEXT.md`, `tools.md`.

---

## Standard Operating Procedure

Full workflow documented in `docs/SOP.md`:

### Roles
- **User**: Logs gym in Hevy (when ready), food in MyFitnessPal, wears Garmin, uploads labs when needed.
- **Physique Desk**: Hub — split, progression, macro anchors.
- **Load & Recovery**: Garmin → traffic light + 1–3 adjustments.
- **Recomp Nutrition**: Menus/swaps within anchors; MFP vs protein.
- **Evidence Desk**: Papers on demand.
- **Labs Prep**: Organizes medical labs for doctor appointment.
- **Chief**: General triage only (NOT recomp owner).

### Cadence
- **Weekly**: Sunday ~9:11 America/Mexico_City — Garmin review (routine lives in Physique Desk).
- **On-demand**: "What today?", daily menu, fatigue check, evidence questions.
- **After Hevy log**: Progression feedback from Desk.
- **After MFP diary days**: Gap analysis from Recomp Nutrition.

### Data Sources (no double-counting)

| Data | Primary Source |
|------|----------------|
| Sets/reps (strength) | **Hevy** |
| Cardio/outdoor | **Strava** or **Garmin** (not both for same effort) |
| Recovery (sleep, HRV, body battery) | **Garmin** |
| Food/weight | **MyFitnessPal** |

---

## Connectors

See `docs/CONNECTORS.md` for full connector map (names only — no secrets).

---

## Knowledge Base

The `knowledge/` directory contains actionable book summaries and literature synthesis for Evidence Desk:

- **`literature-index.md`** — entry point to all knowledge files
- **`schoenfeld-hypertrophy.md`** — Science and Development of Muscle Hypertrophy (Schoenfeld 2020)
- **`renaissance-diet-2.md`** — Renaissance Diet 2.0 (Israetel et al. 2020)
- **`stubborn-fat-mcdonald.md`** — The Stubborn Fat Solution (McDonald 2008)
- **`recomp-synthesis.md`** — Body recomposition synthesis
- **`deep-research-evidence-base.md`** — Comprehensive evidence synthesis

**Note**: No full book PDFs (copyright respect). Only actionable summaries and citations.

---

## Privacy

This public repository contains **zero**:
- API keys, cookies, OAuth tokens
- Email addresses, phone numbers
- Real weight series, HRV dumps, food diaries
- Live account workout IDs

Uses example placeholders where necessary (`USER`, `~170 g protein`, `afternoon gym`).

---

## Documentation

- **`docs/SOP.md`** — Complete workflow and cadence
- **`docs/CONNECTORS.md`** — Connector map, no secrets
- **`docs/PERSONA_VS_CODE.md`** — Persona (live Grok) vs this repo (versioned)
- **`knowledge/`** — Literature summaries (Schoenfeld, Renaissance Diet 2.0, McDonald, etc.)
- **`agents/physique/<bot>/`** — README, persona, context, tools per bot

---

**Last updated**: 2026-09-28
