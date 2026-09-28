# Prompt 07: Recuperación

**Objetivo**: Integrar datos de recuperación (vía Load & Recovery bot + Garmin Connect MCP) en el plan de entrenamiento y nutrición para evitar sobreentrenamiento y optimizar ganancias.

## Inputs

- **Plan de entrenamiento A/B/C** (del Prompt 02): división, volumen, frecuencia.
- **Reglas de progresión** (del Prompt 05): double progression, descarga.
- **Tracker semanal** (del Prompt 06): peso, cintura, progresión de ejercicios.

## Delegación a Load & Recovery

Physique Desk **NO lee Garmin directamente** — delega 100% a **Load & Recovery** bot.

### Flujo semanal (domingo ~9:11 America/Mexico_City)

1. **Load & Recovery** revisa Garmin Connect MCP:
   - Sueño (horas promedio, calidad, deep/REM).
   - Pasos (actividad diaria).
   - HRV (heart rate variability — indicador de recuperación del sistema nervioso).
   - Body battery (métrica Garmin de energía disponible).
   - Estrés (nivel de estrés fisiológico).
   - Preparación (readiness score Garmin).
   - Actividades registradas (cardio, fuerza — duración solamente, NO sets/reps).
   - Training status (productive/maintaining/overreaching/detraining).

2. **Load & Recovery** genera **semáforo + 1–3 ajustes**:
   - **Verde**: todo bien, mantén plan actual.
   - **Amarillo**: 1–2 ajustes ligeros (ej: baja 1–2 sets, agrega 20 min LISS, prioriza sueño).
   - **Rojo**: 2–3 ajustes fuertes (ej: descarga, quita 1 día de gym, cardio solo, duerme más).

3. **Physique Desk** recibe semáforo + ajustes y actualiza plan semanal:
   - Verde → no cambio.
   - Amarillo → aplica ajustes (reduce volumen ligeramente, agrega LISS).
   - Rojo → descarga (reduce peso 40–50%, o quita 1 día de gym, solo cardio LISS).

## Interpretación de métricas de recuperación

### Sueño
- **Objetivo**: 7–8 hrs/noche.
- **Problema**: < 6.5 hrs promedio → recuperación insuficiente → más riesgo de estancamiento o lesión.
- **Ajuste**: si sueño es corto, baja volumen (1–2 sets menos) o agrega día de descanso.

### HRV (heart rate variability)
- **Objetivo**: estable o subiendo vs baseline personal.
- **Problema**: HRV baja -10% o más vs baseline → sistema nervioso fatigado.
- **Ajuste**: descarga (reduce peso o volumen), agrega LISS (recuperación activa), prioriza sueño.

### Body battery (Garmin)
- **Objetivo**: llega a 100 cada noche.
- **Problema**: no llega a 100 (se queda en 60–80) → no recuperas completamente entre días.
- **Ajuste**: duerme más, reduce estrés, agrega día de descanso.

### Training status (Garmin)
- **Productive**: entrenando bien, recuperando bien.
- **Maintaining**: volumen bajo o intensidad baja → puedes entrenar más.
- **Overreaching**: volumen/intensidad muy alto sin recuperación → descarga necesaria.
- **Detraining**: no has entrenado suficiente → retoma plan.

## Ajustes típicos según semáforo

### Verde (todo bien)
- **No cambio** en plan.
- Continúa progresión normal (double progression, sube peso cuando alcanzas tope del rango).

### Amarillo (fatiga ligera)
- **Baja 1–2 sets** en ejercicios principales (ej: 3×10 → 2×10).
- **Agrega 20 min LISS** post-entrenamiento (caminata inclinada, bici suave) → recuperación activa.
- **Prioriza sueño** (intenta 7.5–8 hrs esta semana).
- **Mantén progresión** (no bajes peso, solo reduce volumen temporalmente).

### Rojo (fatiga alta)
- **Descarga completa** (semana de descarga):
  - Reduce peso 40–50% (o reduce sets de 3 a 2).
  - Mantén técnica perfecta, reps en rango bajo (6–8).
- **O quita 1 día de gym** (ej: si plan era A-B-C-A, haz solo A-B-C esta semana).
- **O solo cardio LISS** esta semana (30–40 min caminata/bici, HR baja, no gym).
- **Prioriza sueño** (intenta 8+ hrs).
- **Revisa nutrición** (¿déficit muy agresivo? → considera subir calorías 100–200 kcal temporalmente).

## LISS (Low-Intensity Steady-State cardio)

**Propósito**: recuperación activa + déficit calórico adicional si es necesario.

**Cuándo usar**:
- Semáforo amarillo/rojo (recuperación activa).
- Quieres aumentar déficit sin agregar volumen de gym.
- Días de descanso (caminata 30 min, bici suave).

**Cómo**:
- Caminata inclinada 20–40 min (treadmill 3–4 mph, inclinación 5–10%).
- Bici estacionaria 30–40 min (HR zona 2, conversacional).
- Escaladora 15–20 min (pace suave).
- **NO** HIIT, sprints, o cardio intenso (eso agrega fatiga, no ayuda recuperación).

## Descarga programada (cada 6–8 semanas)

Aunque Load & Recovery no dé semáforo rojo, considera **descarga programada** cada 6–8 semanas:
- Reduce peso 40–50% una semana.
- O reduce frecuencia (3 días en lugar de 4).
- Propósito: recuperación preventiva (sistema nervioso, articulaciones, tendones).

## Salida

Después de este prompt, genera **sistema de recuperación integrado**:

```
Recuperación para USER:
1. Domingo ~9:11 America/Mexico_City: Load & Recovery revisa Garmin → semáforo + ajustes.
2. Verde → mantén plan.
3. Amarillo → baja 1–2 sets, agrega 20 min LISS, prioriza sueño.
4. Rojo → descarga (reduce peso 40–50% o quita 1 día gym), solo LISS, duerme 8+ hrs.
5. Descarga programada cada 6–8 semanas (preventiva).
6. LISS: caminata inclinada 20–40 min, bici 30–40 min (HR zona 2) — recuperación activa o déficit.
```

Esta integración de recuperación alimenta **Prompt 08 (Sistema completo)**.

---

**Privacidad**: No commitear datos reales de HRV, sueño, body battery, o training status de USER al repo público. Usa ejemplos genéricos.
