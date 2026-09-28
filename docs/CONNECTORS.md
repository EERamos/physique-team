# Connectors Map

This document lists the MCP connectors used by the Physique Team bots **by name only**. No API keys, OAuth tokens, cookies, or user-specific identifiers are stored in this repository.

## Connector overview

| Connector name | Used by | Purpose | Notes |
|----------------|---------|---------|-------|
| `user-garmin` (Garmin MCP) | Load & Recovery | Sleep, steps, HRV, body battery, stress, readiness, activities, training status | Sunday weekly check ~9:11 America/Mexico_City |
| `user-strava` / Strava MCP | Load & Recovery (secondary), Physique Desk | Cardio/outdoor activities | Do not double-count with Garmin for same activity |
| `user-myfitnesspal` / mfp-mcp | Recomp Nutrition | Food diary, weight tracking | Compares daily protein vs ~170 g anchor |
| `user-hevy` / hevy-mcp | Physique Desk | Strength sets/reps | Pending: upload A/B/C + core routines when user asks |

## Connector-bot matrix

### Physique Desk (hub)
- **Primary**: `user-hevy` (sets/reps for progression tracking).
- **Secondary**: `user-strava` (cardio context when relevant).
- **Does NOT directly read**: Garmin (delegates to Load & Recovery), MyFitnessPal (delegates to Recomp Nutrition).

### Load & Recovery
- **Primary**: `user-garmin` (all recovery metrics).
- **Secondary**: `user-strava` (cardio/outdoor activities if not already in Garmin).
- **Output**: Traffic light (green/yellow/red) + 1–3 weekly adjustments → sent to Physique Desk.

### Recomp Nutrition
- **Primary**: `user-myfitnesspal` (food diary, weight).
- **Does NOT change**: Macro anchors or training split (Physique Desk owns those).
- **Output**: Flexible menus, shopping lists, portion micro-adjustments.

### Evidence Desk
- **No live data connectors**.
- Purely paper/research lookup (Schoenfeld, Renaissance Diet 2.0, McDonald, systematic reviews).

## Important notes

### Hevy ↔ Garmin limitation
- **Hevy does NOT natively sync from Garmin** (confirmed by Hevy documentation).
- Community tools exist for **Hevy → Garmin** (push workouts from Hevy to Garmin), but NOT for **Garmin → Hevy** (import sets/reps from Garmin into Hevy).
- Therefore: User must log strength sets/reps **manually in Hevy** (or via Hevy app during workout).
- Garmin captures workout **duration** for strength sessions, but duration is **NOT a proxy for volume** (does not include sets/reps/weight).

### No double-counting
- **Cardio/outdoor**: Log in **either** Strava **or** Garmin, not both for the same activity.
- **Strength**: Log in **Hevy** (Garmin duration is NOT used for volume tracking).
- **Recovery**: Always **Garmin**.
- **Food/weight**: Always **MyFitnessPal**.

## Authentication (not in this repo)

All connectors require OAuth or API key authentication. Authentication happens in the live Grok Bot platform or MCP server configuration. **This repo contains zero credentials**.

If you are setting up your own Physique Team clone:
1. Follow MCP connector documentation for each service.
2. Grant connector access to the relevant Grok Bots.
3. **Never commit** API keys, tokens, or user-specific identifiers to version control.

## Pending connector work (TODO)

- **Hevy routine upload**: User needs to say "upload A/B/C to Hevy" → bot uses Hevy MCP to create routine templates.
- **First real logs**: Once user logs strength in Hevy and food in MFP, close-the-loop feedback from bots becomes possible.

---

**Last updated**: 2026-09-28 (initial scaffold)
