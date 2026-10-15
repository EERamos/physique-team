# Load & Recovery — Tools

Conectores MCP que Load & Recovery usa.

## Uso directo

### user-garmin (Garmin Connect MCP)
- **Propósito**: leer sueño, pasos, HRV, body battery, estrés, preparación (readiness), actividades, training status.
- **Cuándo**: domingo ~9:11 America/Mexico_City (revisión semanal) o cuando Physique Desk/USER preguntan.
- **Datos que lee**:
  - Sueño: horas, calidad (deep/REM/light), consistencia.
  - Pasos: promedio diario última semana.
  - HRV (heart rate variability): vs baseline personal.
  - Body battery: score 0–100, cuántas noches llega a 100.
  - Estrés: nivel fisiológico (bajo/medio/alto).
  - Preparación (readiness): score Garmin agregado.
  - Actividades: cardio/fuerza registrados (duración solamente, NO sets/reps).
  - Training status: productive/maintaining/overreaching/detraining.
- **Output**: semáforo (verde/amarillo/rojo) + 1–3 ajustes concretos.

### user-strava (Strava MCP) — secundario
- **Propósito**: leer actividades de cardio/outdoor (correr, ciclismo, caminata) si no están ya en Garmin.
- **Cuándo**: solo si USER usa Strava para cardio intencional (ej: correr, ciclismo) y no está duplicado en Garmin.
- **Nota**: **no doble-conteo** con Garmin (si actividad ya está en Garmin, no leer de Strava).

## No usa

- **NO usa Hevy** (sets/reps viven ahí, pero Load & Recovery no interpreta volumen de fuerza directamente — solo duración de workout en Garmin, que NO es proxy de volumen).
- **NO usa MyFitnessPal** (nutrición es territorio de Recomp Nutrition, no Load & Recovery).

## Delegación

Load & Recovery **NO delega a otros bots** — es especialista puro (recibe pregunta de Physique Desk → lee Garmin → responde semáforo + ajustes).

---

**Privacidad**: Este archivo lista conectores por **nombre solamente**. Cero API keys, OAuth tokens, cookies, o user IDs commitados a este repo.
