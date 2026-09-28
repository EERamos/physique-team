# Pending Connections

This document tracks two **live MCP connections** that are fully designed and configured but waiting on user action or first logs before they can be actively used by the Physique Team bots.

## 1. Hevy MCP: Routine Template Upload

**Status**: MCP connected live ✓  
**Pending**: User request to upload A/B/C + core templates

### What's ready
- Hevy MCP connector is authenticated and operational
- A/B/C training split is fully designed in Physique Desk (upper/lower/full-body)
- Core routine templates are documented in Physique Desk context
- System is designed in `docs/SOP.md` and `docs/CONNECTORS.md`

### What's needed
- User says: "upload A/B/C to Hevy" or "create Hevy templates"
- Physique Desk will then use Hevy MCP to create routine templates with:
  - A: Upper body (bench, rows, OHP, etc.)
  - B: Lower body (squat, RDL, leg press, etc.)
  - C: Full-body (compound movements)
  - Core: accessory core work

### Next step after upload
- Physique Desk can read Hevy workout logs (sets/reps/weight)
- Progression feedback becomes automatic ("great job, ready to add 5 lbs next A day")
- Weekly tracker integrates real volume data

---

## 2. MyFitnessPal MCP: Nutrition Loop Closure

**Status**: MCP connected live ✓  
**Pending**: Real diary days from user

### What's ready
- MyFitnessPal MCP connector is authenticated and operational
- Macro anchors are defined: ~170 g protein floor, gym carbs 120–150 g, rest ~100 g
- Recomp Nutrition is designed to compare diary vs protein target
- System is designed in `docs/SOP.md` and `docs/CONNECTORS.md`

### What's needed
- User logs food in MyFitnessPal (at least 2–3 days for meaningful feedback)
- Real weight/body metrics logged in MFP

### Next step after first logs
- Recomp Nutrition can compare actual intake vs ~170 g protein anchor
- Identifies gaps: "yesterday you logged 140 g, here are 3 ways to close the 30 g gap"
- Portion micro-adjustments based on weight/waist trends
- Shopping lists become personalized to user's actual eating patterns

---

## Why these are NOT forgotten

Both connections are:
1. ✅ **Already live** (MCP servers authenticated and responding)
2. ✅ **Fully designed** (bot personas, SOP, connector map all reference them)
3. ✅ **Waiting on user action** (not a technical blocker, just need user to ask/log)
4. ✅ **Documented in multiple places** (SOP, CONNECTORS, this file)

This file exists to make sure **no one forgets** these two eventual connections when reviewing the Physique Team system. They are not "someday maybe" — they are "as soon as user asks/logs, flip the switch."

---

**Last updated**: 2026-09-28
