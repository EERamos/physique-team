# Prompt 05: Progresión (sobrecarga progresiva)

**Objetivo**: Establecer reglas claras de cuándo y cómo subir peso, reps, o volumen en el entrenamiento para garantizar ganancias de fuerza y músculo.

## Inputs

- **Plan de entrenamiento A/B/C** (del Prompt 02): ejercicios, sets/reps actuales.
- **Experiencia** (del Prompt 01): novato/intermedio/avanzado.

## Principio fundamental: sobrecarga progresiva

**Músculo crece** cuando se le da estímulo mayor que el anterior. Formas de progresar:
1. Más peso (más común).
2. Más reps en el mismo rango.
3. Más sets (aumentar volumen).
4. Mejor técnica / rango de movimiento.
5. Menos descanso entre sets (avanzado).

## Estrategia: double progression

**Rango objetivo**: ejemplo 3×8–12 (3 sets, 8–12 reps).

### Paso 1: sube reps
- Sesión 1: 3×8 con 60 kg.
- Sesión 2: intenta 3×9 con 60 kg.
- Sesión 3: intenta 3×10 con 60 kg.
- Sesión 4: intenta 3×11 con 60 kg.
- Sesión 5: 3×12 con 60 kg → **alcanzaste tope del rango**.

### Paso 2: sube peso, baja reps
- Sesión 6: sube a 62.5 kg (o 65 kg si saltos de 5 kg) → probablemente 3×8–9 con nuevo peso.
- Sesión 7+: repite ciclo (sube reps hasta 3×12, luego sube peso).

## Reglas prácticas

### Cuándo subir peso
- **Completaste todas las series en el tope del rango** (ej: 3×12) con técnica correcta.
- **Dos sesiones consecutivas** en el tope (para estar seguro).

### Cuánto subir peso
- **Ejercicios upper body** (press banca, press militar, remo): 2.5 kg.
- **Ejercicios lower body** (sentadilla, peso muerto rumano, prensa): 5 kg.
- **Aislamiento** (curls, tríceps, lateral raises): 1–2.5 kg.

### Si no puedes completar reps
- **Estancado 2 sesiones** (ej: siempre 3×8 con 60 kg, nunca 3×9) → considera:
  - Descarga (reduce peso 10% una semana).
  - Micro-ajuste (sube solo 1.25 kg en lugar de 2.5 kg).
  - Cambio de ejercicio (ej: press banca con barra → press banca con mancuernas).
  - Revisa recuperación (Load & Recovery puede indicar fatiga alta).

### Si técnica se degrada
- **No subas peso** hasta que técnica sea correcta en todas las reps.
- Mejor 3×10 con técnica perfecta que 3×12 con técnica mala.

## Tracking de progresión (Hevy MCP)

Physique Desk usa **Hevy MCP** para:
- Leer último registro de ejercicio (peso × reps).
- Comparar con sesión anterior.
- Dar feedback: "Subiste de 60 kg × 10 a 60 kg × 12 → próxima sesión intenta 62.5 kg".

**Pendiente**: USER necesita registrar sets/reps en Hevy para que este ciclo funcione. Mientras tanto, Physique Desk da reglas generales.

## Progresión según experiencia

- **Novato** (< 1 año): progresión lineal simple cada 1–2 semanas (sube peso cuando alcanzas tope del rango).
- **Intermedio** (1–3 años): double progression (reps primero, luego peso); progresión cada 2–4 semanas.
- **Avanzado** (> 3 años): periodización (fases de volumen, intensidad, descarga); progresión cada 4–8 semanas.

Para recomposición, **intermedio** es suficiente — no necesitas periodización compleja.

## Descarga (deload)

Cada **6–8 semanas** o cuando **Load & Recovery da semáforo rojo**:
- Reduce peso 40–50% (o reduce sets de 3 a 2).
- Mantén técnica perfecta, reps en rango bajo (6–8 en lugar de 10–12).
- Propósito: recuperación del sistema nervioso, articulaciones, tendones.

## Salida

Después de este prompt, genera **reglas de progresión documentadas**:

```
Progresión para USER:
1. Rango 3×8–12 en la mayoría de ejercicios.
2. Double progression: sube reps hasta 3×12, luego sube peso 2.5–5 kg (upper 2.5 kg, lower 5 kg).
3. Si estancado 2 sesiones → descarga o micro-ajuste.
4. Si técnica se degrada → NO subir peso.
5. Descarga cada 6–8 semanas o cuando Load & Recovery da semáforo rojo.
6. Tracking en Hevy (pendiente: USER registra sets/reps).
```

Estas reglas alimentan **Prompt 06 (Tracker semanal)** y **Prompt 07 (Recuperación)**.

---

**Privacidad**: Ejemplos de progresión son genéricos (60 kg, 62.5 kg, etc.). No commitear pesos específicos de USER al repo público.
