# Prompt 01: Analizar marco corporal

**Objetivo**: Evaluar el punto de partida de USER para diseño de entrenamiento y nutrición de recomposición corporal.

## Preguntas clave

1. **Estructura corporal**:
   - ¿Cuál es tu altura? (cm o pies/pulgadas)
   - ¿Cuál es tu peso actual aproximado? (solo para contexto — no commitear peso específico al repo)
   - ¿Cómo describirías tu tipo de cuerpo? (ectomorfo/mesomorfo/endomorfo, o simplemente "delgado"/"promedio"/"robusto")

2. **Experiencia de entrenamiento**:
   - ¿Has entrenado fuerza antes? ¿Cuánto tiempo? (novato < 1 año, intermedio 1–3 años, avanzado > 3 años)
   - ¿Conoces técnica de sentadilla, peso muerto, press banca? (básico/bueno/excelente)
   - ¿Qué ejercicios has hecho recientemente?

3. **Disponibilidad**:
   - ¿Cuántos días por semana puedes entrenar? (3, 4, 5, 6)
   - ¿Cuánto tiempo por sesión? (45 min, 60 min, 75+ min)
   - ¿Tienes acceso a gym comercial? (barras, mancuernas, máquinas, cables)
   - ¿Prefieres mañana/tarde/noche para entrenar?

4. **Restricciones**:
   - ¿Alguna lesión o dolor crónico? (hombro, rodilla, espalda baja, etc.)
   - ¿Ejercicios que debes evitar?

5. **Objetivo principal**:
   - Ganar músculo (bulk limpio)
   - Perder grasa (cut)
   - Recomposición (ganar músculo + perder grasa simultáneamente)
   - Mantenimiento + fuerza

## Salida

Después de estas preguntas, genera un **resumen del marco**:

```
USER tiene [altura], ~[rango de peso], tipo [descripción]. Experiencia [novato/intermedio/avanzado]. Puede entrenar [X días/semana], [Y minutos/sesión], acceso a [tipo de gym]. Prefiere entrenar [timing]. [Restricciones si existen]. Objetivo: [recomposición/bulk/cut].
```

Este resumen alimenta **Prompt 02 (Diseño de entrenamiento)** y **Prompt 03 (Nutrición para recomposición)**.

---

**Privacidad**: No commitear peso específico, altura exacta, o detalles médicos al repo público. Usa rangos o placeholders genéricos en ejemplos.
