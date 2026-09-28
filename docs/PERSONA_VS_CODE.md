# Grok persona (live) vs this repo (versioned)

## Overview

This document clarifies the relationship between **live Grok Bot personas** (running in production on X/Grok) and **this versioned code repository**.

### Live Grok Bot personas

- **Where**: Grok Bot profiles on X (accessible via `@PhysiqueDesk`, `@LoadRecoveryBot`, etc. — exact handles may vary).
- **What**: The actual natural-language persona description, instructions, wake words, anti-jobs, voice guidelines, and MCP tool grants that Grok reads when a user interacts with the bot.
- **Who edits**: Eduardo E. Ramos (owner) or authorized collaborators via Grok Bot admin UI.
- **Versioning**: Not versioned by git. Changes to live persona happen in the Grok platform directly.
- **Privacy**: May contain **non-public memory**, **context**, or **tool configurations** that are NOT replicated in this public repo.

### This repo (agents/physique/*)

- **Where**: This public GitHub repository (`EERamos/physique-team`).
- **What**: Documentation, persona templates, SOP, connector map, and folder structure that **mirrors** the live system design in a shareable, privacy-safe format.
- **Who edits**: Eduardo E. Ramos via git commits (may accept PRs from collaborators).
- **Versioning**: Full git history.
- **Privacy**: **Zero secrets, zero personal health data**. All examples use placeholders (`USER`, `~170 g protein`, etc.).

## Why both?

### Separation of concerns

1. **Live bot = execution environment**  
   - Runs on Grok platform.
   - Has access to real MCP connectors (Garmin, MyFitnessPal, Hevy, Strava).
   - May store conversation memory, user preferences, real workout data.

2. **This repo = design + documentation**  
   - Clean, reusable reference.
   - Onboarding for future collaborators.
   - Public showcase of system architecture.
   - Testable templates for persona text (can copy-paste from `agents/physique/<bot>/persona.md` into Grok Bot admin).

### What lives where

| Artifact | Live bot | This repo |
|----------|----------|-----------|
| Persona description | ✅ Master version | ✅ Template (scrubbed PII) |
| Anti-jobs / wake words | ✅ Master version | ✅ Template |
| Voice guidelines | ✅ Master version | ✅ Template |
| MCP tool grants | ✅ Master config | ✅ Doc (`tools.md` — names only) |
| Generic context (e.g. "evening gym") | ✅ May exist | ✅ In `CONTEXT.md` |
| Specific health data (weight, HRV) | ✅ May exist | ❌ Never committed |
| API keys, OAuth tokens | ✅ Secured in Grok platform | ❌ Never committed |
| SOP / workflow | Implicit in persona | ✅ Explicit in `docs/SOP.md` |
| 8-prompt framework | ✅ Physique Desk owns | ✅ In `agents/physique/desk/prompts/` |

## Update workflow

### Scenario 1: Update persona description

1. **Draft** the change in `agents/physique/<bot>/persona.md` (this repo).
2. **Review** the change (git diff, PR if applicable).
3. **Apply** the change to the live Grok Bot admin UI.
4. **Commit** the change to this repo.

Order may vary (live-first or repo-first), but both should converge.

### Scenario 2: Update SOP or workflow

1. **Edit** `docs/SOP.md` in this repo.
2. **Commit** the change.
3. **Communicate** the change to live bots (if personas need updating to match new SOP).

### Scenario 3: Add a new bot

1. **Create** `agents/physique/<new-bot>/` folder in this repo (README, persona, CONTEXT, tools).
2. **Create** the live Grok Bot on X/Grok platform.
3. **Copy** persona template from repo → Grok Bot admin.
4. **Grant** MCP tools as documented in `tools.md`.
5. **Update** `docs/SOP.md` and root `README.md` to mention the new bot.

## Testing

- **Live bot testing**: Manual interaction on X/Grok.
- **Repo testing**: CI lint (if added), manual review of markdown, no secrets scanner (optional).

## Secrets / privacy

- **Live bots**: May have access to real OAuth tokens, API keys, personal health data. **NEVER** extract these into this repo.
- **This repo**: Public. Anyone can read it. Use placeholders only.

If a live bot's memory or context includes personal data (weight, workout IDs, food diary entries), **do not** copy that data into `CONTEXT.md` — use generic patterns only (e.g. "gym in evening", "sleep often short" — no specific HRV numbers).

## Questions?

- Owner: [@EERamos](https://github.com/EERamos)
- Issues: Open a GitHub issue in this repo.

---

**Last updated**: 2026-09-28 (initial scaffold)
