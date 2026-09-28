# SOP: Physique Team

Flujo de trabajo completo para el sistema Physique Team.

## Quién hace qué

### Usuario
- Registra entrenamiento de gym en **Hevy** (cuando esté listo).
- Registra comida/peso en **MyFitnessPal**.
- Usa **Garmin** (reloj/wearable) para datos de recuperación.

### Physique Desk (hub)
- **Dueño** de:
  - División de entrenamiento (A/B/C: upper/lower/full-body).
  - Reglas de progresión (sobrecarga progresiva).
  - Anclajes de macros (~170 g proteína piso práctico; carbos gym 120–150 g almidón cocido, resto ~100 g).
- **Orquesta** el flujo semanal y delega a especialistas cuando es necesario.
- **Framework de 8 prompts**:
  1. Analizar marco corporal → evaluar punto de partida.
  2. Diseño de entrenamiento → división A/B/C, selección de ejercicios.
  3. Nutrición para recomposición → anclajes de kcal/macros.
  4. Guía de comidas → estructura diaria (comidas, timing).
  5. Progresión → cuándo/cómo subir carga, reps, volumen.
  6. Tracker semanal → registro de progreso, peso, cintura, fotos.
  7. Recuperación → integración con Load & Recovery.
  8. Sistema completo → cierre del ciclo.

### Load & Recovery
- **SOLO**: interpretar datos de **Garmin Connect MCP** (sueño, pasos, HRV, body battery, estrés, preparación, actividades, training status).
- **Salida**: semáforo (verde/amarillo/rojo) + 1–3 ajustes semanales concretos.
- **Framework**:
  - Medido → significado de fatiga → cambio (volumen, timing, LISS, sueño, descarga).
- **Reglas**:
  - Silencioso si no hay sincronización útil de Garmin.
  - Nunca diagnóstico médico ni prescripción.
  - Duración de fuerza en Garmin NO es proxy de volumen (Garmin no captura sets/reps).

### Recomp Nutrition
- **SOLO**: convertir anclajes en comida diaria.
- **Salida**:
  - Menús flexibles.
  - Equivalentes Denisse Lizarraga (plan oct 2025 como guía de porciones).
  - Lista de compras.
  - Manejo de antojos/alcohol.
  - Micro-ajustes de porción desde reportes de peso/cintura/fotos.
- **NO cambia** kcal/anclajes de proteína ni división de gym solo (Physique Desk cierra esos).
- **Usa MyFitnessPal MCP** cuando existe diario; compara vs ~170 g proteína.

### Evidence Desk
- **SOLO**: ciencia del deporte / hipertrofia / nutrición evidencia-basada.
- **Fuentes**: literatura en `knowledge/` (Schoenfeld Hypertrophy; Renaissance Diet 2.0; McDonald Stubborn Fat); revisiones sistemáticas.
- **Salida**:
  - Pregunta → 3–7 bullets (reclamo + fuente + año).
  - 1–2 líneas de implicación práctica (NO reescribe rutina completa).
- **Physique Desk** traduce evidencia en plan concreto.

### Labs Prep
- **SOLO**: organizar laboratorios/análisis médicos que USER sube.
- **Salida**:
  - Inventario (tipo de lab, fecha, fuente/laboratorio).
  - Valores en bruto tal como aparecen escritos (NO interpretación clínica).
  - Preguntas para la cita con médico deportivo real.
  - Checklist de labs faltantes si es incompleto.
- **NO diagnóstico médico**: nunca interpretar valores, nunca prescribir medicamentos/suplementos, nunca cambiar planes Physique Desk/Recomp/Load (eso es trabajo de esos bots + médico real si es necesario).
- **Bandera roja médica** (valores extremos, síntomas graves) → decir "ve a tu médico real" y parar.

### Chief (triage general)
- **NO** dueño de recomposición.
- Puede redirigir a Physique Desk u otro bot cuando sea necesario.

## Fuentes de datos (sin doble-conteo)

| Dato | Fuente principal |
|------|------------------|
| Sets/reps de fuerza | **Hevy** |
| Cardio/outdoor | **Strava** o **Garmin** (no ambos para el mismo esfuerzo) |
| Recuperación (sueño, HRV, body battery) | **Garmin** |
| Comida/peso | **MyFitnessPal** |
| Labs médicos | **Archivos subidos por usuario** (Labs Prep organiza) |

## Cadencia

### Semanal
- **Domingo ~9:11 America/Mexico_City**: revisión semanal Garmin.
  - Load & Recovery revisa datos de la semana pasada.
  - Physique Desk recibe semáforo + ajustes y actualiza rutina si es necesario.

### On-demand (cuando el usuario lo solicite)
- "¿Qué hago hoy?" → Physique Desk responde con rutina del día (A/B/C/descanso/cardio).
- Menú del día → Recomp Nutrition genera opciones.
- Pase de carga (si síntomas de fatiga) → Load & Recovery revisa Garmin y da semáforo.
- Pregunta de evidencia → Evidence Desk responde con papers + implicación práctica.
- "Organiza mis labs" → Labs Prep genera inventario + preguntas para médico deportivo real.

### Después de registro
- **Después de registro Hevy** (sets/reps) → Physique Desk revisa progresión y da nota de feedback.
- **Después de días de diario MFP** → Recomp Nutrition revisa brechas (¿llegó a ~170 g proteína? ¿necesita ajustes?).
- **Después de subir labs médicos** → Labs Prep genera inventario + preguntas para cita con médico.

## Anti-trabajos (todos los bots)

- **No** fantasy NFL / Polymarket.
- **No** inventar laboratorios médicos / resultados de labs (Labs Prep organiza labs reales subidos, nunca inventa valores).
- **No** prescribir medicamentos (Labs Prep deriva a médico real, no prescribe).
- **No** publicaciones externas (X, Slack, etc.) sin autorización explícita del usuario.
- **No** compartir datos personales fuera del grupo Physique Team.

## Privacidad

- Este SOP describe el flujo ideal.
- El repo público contiene **cero secretos, cero datos personales**.
- Conectores listados por nombre solamente (ver `CONNECTORS.md`).
- Ningún peso real, HRV, diario de comida, o workout ID se commitea.

---

**Última actualización**: 2026-09-28 (scaffold inicial)
