# Load & Recovery — Context

Contexto genérico de interpretación de métricas Garmin para USER. **Sin datos personales específicos** (no HRV baseline real, no sleep series — solo frameworks de interpretación).

## Métricas Garmin: qué significan

### Sueño
- **Objetivo**: 7–8 hrs/noche (adulto activo).
- **Calidad**: Garmin mide deep sleep, REM sleep, light sleep, awake.
  - Deep sleep (sueño profundo): recuperación física, crecimiento muscular.
  - REM sleep: recuperación cognitiva, memoria.
  - **Problema**: < 6.5 hrs promedio → recuperación insuficiente → riesgo de estancamiento, lesión, burnout.
- **Consistencia**: acostarse/levantarse a la misma hora ayuda (ritmo circadiano).

### HRV (heart rate variability)
- **Qué es**: variabilidad del intervalo entre latidos cardíacos (milisegundos). Alta HRV = sistema nervioso parasimpático (descanso/recuperación) dominando. Baja HRV = simpático (estrés/fatiga) dominando.
- **Baseline personal**: cada persona tiene su HRV "normal" (puede ser 30 ms, 50 ms, 80 ms — varía mucho). Lo importante es **tendencia vs tu baseline**, no valor absoluto.
- **Interpretación**:
  - **+5% o más vs baseline**: recuperación excelente, sistema nervioso descansado.
  - **±5% vs baseline**: estable, normal.
  - **-5% a -10% vs baseline**: ligera fatiga, considera ajustes (baja volumen, agrega LISS, prioriza sueño).
  - **< -10% vs baseline**: fatiga alta, descarga necesaria.
- **Cuándo medir**: Garmin mide HRV durante sueño (promedio nocturno). No uses HRV en tiempo real durante el día (varía mucho).

### Body battery (Garmin métrica propietaria)
- **Qué es**: score 0–100 que estima energía disponible. Baja con actividad (gym, estrés, trabajo), sube con descanso (sueño, relajación).
- **Objetivo**: llega a 100 cada noche (recuperación completa).
- **Interpretación**:
  - **Llega a 100 mayoría de noches**: bien, recuperando completamente.
  - **Se queda en 80–95**: casi bien, pero no 100% — considera priorizar sueño o reducir volumen ligeramente.
  - **Se queda en < 80**: no recuperas completamente entre días → descarga necesaria.
- **Nota**: body battery es útil como indicador agregado, pero no reemplaza HRV o sueño (usa las tres métricas juntas).

### Estrés (Garmin)
- **Qué es**: Garmin usa HRV + heart rate para estimar nivel de estrés fisiológico (no psicológico — aunque están correlacionados).
- **Niveles**: bajo (azul), medio (amarillo), alto (rojo).
- **Interpretación**:
  - **Bajo–medio mayoría del día**: normal.
  - **Alto constantemente**: sistema nervioso fatigado, considera descanso o ajuste de volumen.
- **Nota**: picos de estrés durante gym son normales (entrenamiento intenso = estrés fisiológico temporal). Problema es estrés alto **fuera del gym** (indica falta de recuperación).

### Preparación (readiness score Garmin)
- **Qué es**: métrica agregada de sueño + HRV + body battery + training load. Garmin da score "ready to train" o "need rest".
- **Interpretación**: usa como check rápido, pero confía más en HRV + sueño + body battery individuales.

### Training status (Garmin)
- **Productive**: volumen + intensidad bien balanceados, recuperando bien → mantén plan.
- **Maintaining**: volumen o intensidad bajo → puedes entrenar más (pero para recomposición, "maintaining" puede estar bien si objetivo es no sobreentrenar).
- **Overreaching**: volumen/intensidad muy alto sin recuperación suficiente → descarga necesaria.
- **Detraining**: no has entrenado suficiente (1–2 semanas sin gym) → retoma plan.
- **Nota**: training status usa algoritmo Garmin basado en VO2max estimado + training load. Útil como indicador, pero no 100% preciso (usa en conjunto con HRV/sueño).

### Pasos
- **Objetivo**: ~8k–10k pasos/día (adulto activo).
- **Interpretación**:
  - **< 6k pasos/día promedio**: muy sedentario fuera del gym → considera agregar caminatas ligeras.
  - **6k–8k**: OK, pero puede mejorar.
  - **8k–10k+**: bien.
- **Nota**: pasos es indicador de actividad diaria (NEAT — non-exercise activity thermogenesis). Más pasos = más calorías quemadas fuera del gym.

## Ajustes típicos según datos

### Semáforo VERDE (continuar plan)
- Sueño ≥ 7 hrs.
- HRV estable o +5%.
- Body battery llega a 100.
- Training status: productive.
- **Ajustes**: ninguno.

### Semáforo AMARILLO (ajustes ligeros)
- Sueño 6.5–7 hrs.
- HRV -5% a -10%.
- Body battery llega a 80–95.
- Training status: productive (límite superior).
- **Ajustes**:
  1. Baja 1–2 sets en ejercicios principales.
  2. Agrega 20 min LISS post-gym (recuperación activa).
  3. Prioriza sueño (7.5–8 hrs).

### Semáforo ROJO (descarga o descanso)
- Sueño < 6.5 hrs.
- HRV < -10%.
- Body battery < 80.
- Training status: overreaching.
- **Ajustes**:
  1. Descarga (reduce peso 40–50%, 2×6–8 reps).
  2. O quita 1 día de gym.
  3. O solo LISS esta semana (30–40 min, no gym).
  4. Prioriza sueño (8+ hrs).
  5. Revisa nutrición (¿déficit muy agresivo?).

## Limitaciones de Garmin

### Duración de fuerza NO es volumen
- Garmin captura duración de workout (ej: 60 min en gym).
- **NO captura** sets/reps/peso (eso vive en Hevy).
- 60 min puede ser 10 sets o 25 sets — no hay forma de saber.
- **No uses** duración como proxy de volumen.

### Training status puede ser impreciso
- Training status usa VO2max estimado + algoritmos Garmin.
- Puede dar "detraining" si no hiciste cardio outdoor (Garmin prioriza cardio para VO2max).
- Usa training status como **uno de varios indicadores**, no como verdad absoluta.

### HRV baseline puede cambiar
- HRV baseline puede subir con mejora de fitness (sistema nervioso más fuerte).
- Compara siempre vs **baseline reciente** (últimas 2–4 semanas), no vs baseline de hace 6 meses.

---

**Privacidad**: Este `CONTEXT.md` contiene **solo frameworks genéricos**. No commitear HRV baseline real, sleep series, o body battery trends de USER al repo público.
