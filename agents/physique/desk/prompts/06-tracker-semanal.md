# Prompt 06: Tracker semanal

**Objetivo**: Establecer sistema de seguimiento semanal para medir progreso de recomposición corporal (peso, cintura, fotos, progresión de ejercicios).

## Inputs

- **Anclajes de macros** (del Prompt 03): calorías ~2200–2400, proteína ~170 g, carbos ciclados.
- **Reglas de progresión** (del Prompt 05): double progression, cuándo subir peso.
- **Objetivo** (del Prompt 01): recomposición (ganar músculo + perder grasa).

## Métricas clave

### 1. Peso corporal

**Cuándo**: lunes AM, en ayunas, post-baño (para consistencia).

**Cómo interpretar**:
- **Tendencia semanal** importa más que día a día (agua, comida, sal afectan peso diario).
- Promedia peso de lunes los últimos 3–4 lunes → esa es la tendencia.

**Objetivos según fase**:
- **Recomposición**: peso estable o baja **muy lento** (0.25–0.5 kg/mes).
- **Cut**: baja 0.5–1% peso corporal/semana (ej: USER ~75 kg → 0.4–0.75 kg/semana).
- **Bulk**: sube 0.25–0.5 kg/semana.

**Ajustes**:
- Si peso no se mueve en 2–3 semanas Y objetivo es cut → baja calorías 100–200 kcal (Recomp Nutrition ajusta porciones).
- Si peso baja muy rápido (> 1%/semana) → sube calorías 100–200 kcal.
- Si peso sube muy rápido (> 0.5 kg/semana en recomp) → revisa calorías.

### 2. Cintura (perímetro abdominal)

**Cuándo**: lunes AM, post-baño, antes de comer.

**Cómo medir**:
- Cinta métrica al nivel del ombligo (no la parte más angosta de la cintura).
- Sin apretar (cinta debe tocar piel pero no comprimir).
- Exhala normal (no succionar estómago, no inhalar profundo).

**Cómo interpretar**:
- **Cintura baja** = perdiendo grasa abdominal (incluso si peso estable → recomposición exitosa).
- **Cintura sube** = ganando grasa (incluso si peso estable → revisa calorías o estrés/cortisol).
- Cintura es **mejor indicador que peso** para recomposición.

**Objetivos**:
- Recomposición: cintura baja 0.5–1 cm/mes.
- Cut: cintura baja 1–2 cm/mes.
- Bulk: cintura estable o sube **muy lento** (si sube > 1 cm/mes → probablemente ganando mucha grasa).

### 3. Fotos (opcional, pero útil)

**Cuándo**: cada 2–4 semanas, lunes AM (misma hora que peso/cintura).

**Cómo**:
- Frente, espalda, lado (perfil).
- Misma iluminación (baño con luz cenital).
- Misma pose (brazos a los lados, relajado).
- Misma distancia de cámara.

**Cómo interpretar**:
- Compara fotos de **hace 4–8 semanas** (no semana a semana — cambios son demasiado sutiles).
- Fíjate en: definición abdominal, tamaño de hombros/brazos, glúteos, piernas.

### 4. Progresión de ejercicios (Hevy MCP)

**Cuándo**: después de cada sesión de gym (USER registra en Hevy).

**Qué trackear** (ejercicios clave):
- **Sentadilla**: peso × reps (ej: 80 kg × 10).
- **Press banca**: peso × reps.
- **Peso muerto rumano**: peso × reps.
- **Hip thrust**: peso × reps.
- **Remo con barra**: peso × reps.

**Cómo interpretar**:
- **Progresión lineal** (peso o reps sube cada 1–3 semanas) = músculo está creciendo, fuerza subiendo.
- **Estancado 3–4 semanas** = revisa recuperación (Load & Recovery), considera descarga, o ajusta volumen.
- **Regresión** (peso baja) = probablemente fatiga alta (Load & Recovery) o déficit muy agresivo (revisa calorías).

**Cuando USER use Hevy**: progresión de ejercicios se lee automáticamente de Hevy MCP. Mientras tanto, Physique Desk pregunta "¿subiste peso/reps esta semana?".

## Revisión semanal (domingo o lunes)

Physique Desk revisa:
1. **Peso/cintura** lunes AM → tendencia.
2. **Progresión de ejercicios** (Hevy) → ¿subió peso/reps esta semana?
3. **Semáforo de Load & Recovery** (domingo ~9:11 America/Mexico_City) → ¿verde/amarillo/rojo?
4. **Adherencia a nutrición** (via Recomp Nutrition si USER usa MFP) → ¿llegó a ~170 g proteína mayoría de días?

**Salida**:
- "Esta semana: peso estable, cintura -0.5 cm, sentadilla subió de 80 kg × 10 a 80 kg × 12 (próxima sesión intenta 82.5 kg). Load & Recovery: semáforo verde. Nutrición: proteína promedio 165 g (objetivo ~170 g) — intenta agregar 1 scoop whey o 100 g pechuga más."

## Salida

Después de este prompt, genera **sistema de tracker semanal documentado**:

```
Tracker semanal para USER:
1. Peso corporal: lunes AM, ayunas, post-baño → tendencia (promedio últimos 3–4 lunes).
2. Cintura: lunes AM, ombligo, sin apretar → -0.5–1 cm/mes objetivo.
3. Fotos: cada 2–4 semanas (frente/espalda/lado, misma iluminación).
4. Progresión ejercicios: Hevy (sentadilla, press banca, peso muerto rumano, hip thrust, remo).
5. Revisión domingo/lunes: peso/cintura + progresión + semáforo Load & Recovery + adherencia nutrición.
```

Este tracker alimenta **Prompt 07 (Recuperación)** y **Prompt 08 (Sistema completo)**.

---

**Privacidad**: No commitear peso real, cintura específica, o fotos de USER al repo público. Usa placeholders genéricos en ejemplos.
