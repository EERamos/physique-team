# Physique Desk — Tools

Conectores MCP que Physique Desk usa o a los que delega.

## Uso directo

### user-hevy (Hevy MCP)
- **Propósito**: registrar y leer sets/reps de entrenamiento de fuerza.
- **Cuándo**: 
  - USER termina sesión de gym → Physique Desk lee progresión (peso × reps) y da feedback.
  - USER pide "sube rutinas A/B/C a Hevy" → Physique Desk crea templates de rutina.

### user-strava (Strava MCP) — secundario
- **Propósito**: leer actividades de cardio/outdoor (correr, ciclismo, caminata).
- **Cuándo**: USER registra cardio en Strava → Physique Desk puede ver volumen de cardio para contexto.
- **Nota**: no doble-conteo con Garmin (si actividad ya está en Garmin, no leer de Strava).

## Delegación a especialistas

### user-garmin (Garmin MCP) — via Load & Recovery
- **Propósito**: sueño, pasos, HRV, body battery, estrés, preparación, actividades, training status.
- **Cuándo**: domingo ~9:11 America/Mexico_City → Physique Desk pide a **Load & Recovery** que revise Garmin y dé semáforo + ajustes.
- **Physique Desk NO lee Garmin directamente** — delega 100% a Load & Recovery.

### user-myfitnesspal (MyFitnessPal MCP) — via Recomp Nutrition
- **Propósito**: diario de comida, peso, comparación proteína diaria vs ~170 g.
- **Cuándo**: USER pide menú, o tiene días de diario MFP → Physique Desk delega a **Recomp Nutrition**.
- **Physique Desk NO lee MFP directamente** — delega 100% a Recomp Nutrition.

## No usa

- Evidence Desk no tiene conectores de datos en vivo (solo papers/libros).
- Physique Desk no usa conectores de redes sociales, email, calendario (fuera de scope).

---

**Privacidad**: Este archivo lista conectores por **nombre solamente**. Cero API keys, OAuth tokens, cookies, o user IDs commitados a este repo.
