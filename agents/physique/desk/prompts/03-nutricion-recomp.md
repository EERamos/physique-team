# Prompt 03: Nutrición para recomposición

**Objetivo**: Establecer anclajes de calorías y macros para recomposición corporal (ganar músculo + perder grasa simultáneamente, o mantenimiento + recomposición lenta).

## Inputs

- **Marco** (del Prompt 01): peso actual aproximado, altura, objetivo (recomposición/bulk/cut).
- **Plan de entrenamiento** (del Prompt 02): días de gym por semana, intensidad.

## Principios de recomposición

1. **Calorías**: ligero déficit (~10–15% debajo de mantenimiento) o mantenimiento exacto.
   - Mantenimiento ≈ peso_kg × 30–35 (activo) o peso_kg × 33 (promedio).
   - Ejemplo: USER ~75 kg → mantenimiento ~2400–2600 kcal → recomp ~2200–2400 kcal.

2. **Proteína**: 1.6–2.2 g/kg peso corporal → **~170 g proteína/día** como piso práctico para USER.
   - Esto asegura síntesis muscular + saciedad.
   - Fuentes: pollo, res, pescado, huevo, whey, legumbres.

3. **Carbohidratos**: ciclado según día de entrenamiento.
   - **Días de gym**: 120–150 g almidón cocido (arroz blanco, papa, camote, pasta) pre/post-entrenamiento.
   - **Días de descanso**: ~100 g carbos totales (frutas, verduras, algo de almidón si es necesario).
   - Timing: mayoría de carbos alrededor del entrenamiento (2–3 hrs antes + post).

4. **Grasas**: llenar resto de calorías.
   - ~0.8–1.2 g/kg peso corporal (60–90 g para USER ~75 kg).
   - Fuentes: aguacate, aceite de oliva, nueces, almendras, yema de huevo.

5. **Timing** (importancia secundaria vs calorías/macros totales, pero útil):
   - Pre-entrenamiento (1–2 hrs antes): carbos + algo de proteína.
   - Post-entrenamiento: proteína + carbos (puede ser whey + fruta/arroz).
   - Resto del día: proteína en cada comida, grasas + verduras.

## Anclajes para USER (ejemplo)

```
Proteína: ~170 g/día
Carbos días de gym: 120–150 g almidón cocido (pre/post-gym) + verduras/frutas (~200 g carbos totales)
Carbos días de descanso: ~100 g carbos totales (frutas, verduras, algo de almidón)
Grasas: 60–80 g/día (aguacate, aceite, nueces, yema)
Calorías: ~2200–2400 kcal/día (ajustable según peso/cintura tendencia)
```

## Delegación a Recomp Nutrition

Physique Desk **NO genera menús concretos** — establece anclajes y delega a **Recomp Nutrition** (Prompt 04) para:
- Menús diarios flexibles.
- Equivalentes Denisse Lizarraga (plan oct 2025 como guía de porciones).
- Lista de compras.
- Manejo de antojos/alcohol.
- Micro-ajustes de porción desde reportes de peso/cintura.

## Salida

Después de este prompt, genera **anclajes de macros/calorías** documentados:

```
Anclajes para recomposición:
- Proteína: [X g/día]
- Carbos días gym: [Y g almidón cocido] pre/post + verduras
- Carbos días descanso: [Z g totales]
- Grasas: [W g/día]
- Calorías: [rango kcal/día]
```

Estos anclajes alimentan **Prompt 04 (Guía de comidas)** y **Prompt 06 (Tracker semanal)**.

---

**Privacidad**: No commitear peso específico, calorías exactas calculadas, o metas personales de USER al repo público. Usa rangos o placeholders genéricos en ejemplos (~170 g proteína está OK como piso práctico público).
