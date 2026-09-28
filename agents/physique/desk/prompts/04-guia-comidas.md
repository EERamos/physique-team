# Prompt 04: Guía de comidas

**Objetivo**: Estructurar las comidas diarias (timing, pre/post-gym, número de comidas) dentro de los anclajes de macros. Delega menús concretos a **Recomp Nutrition**.

## Inputs

- **Anclajes de macros** (del Prompt 03): proteína ~170 g, carbos días gym 120–150 g almidón cocido, carbos días descanso ~100 g, grasas 60–80 g, calorías ~2200–2400.
- **Timing de entrenamiento**: típicamente tarde/noche (6–8 PM para USER).

## Estructura de comidas (ejemplo)

### Días de gym (entrenamiento tarde/noche)

#### Desayuno (~8–9 AM)
- Proteína: huevos, whey, o yogurt griego.
- Carbos: avena, fruta, o pan integral (moderado).
- Grasas: aguacate, nueces, o yema de huevo.
- **Ejemplo**: 3 huevos revueltos + 1 taza avena + 1 plátano + 10 almendras.

#### Comida (~1–2 PM)
- Proteína: pollo, res, pescado, o legumbres.
- Carbos: arroz, papa, o camote (porción moderada).
- Grasas: aceite de oliva, aguacate.
- Verduras: ensalada, brócoli, espinacas.
- **Ejemplo**: 150 g pechuga de pollo + 1 taza arroz cocido + ensalada + 1 cdita aceite de oliva.

#### Pre-entrenamiento (~4–5 PM, 1–2 hrs antes de gym)
- Carbos: 120–150 g almidón cocido (arroz, papa, pasta).
- Proteína: algo ligero (puede ser parte de la comida anterior extendida).
- **Ejemplo**: 1.5 tazas arroz blanco cocido + 100 g pechuga de pollo.

#### Post-entrenamiento (~8–9 PM, después de gym)
- Proteína: whey + comida con proteína.
- Carbos: fruta, o algo de almidón si aún falta para cerrar 120–150 g.
- **Ejemplo**: 1 scoop whey + 1 plátano + 150 g yogurt griego.

#### Cena (~10 PM, si tiene hambre)
- Proteína: huevos, atún, o queso cottage.
- Grasas: aguacate, nueces.
- Verduras.
- Carbos: bajo (ya se llenó pre/post-gym).
- **Ejemplo**: tortilla de 2 huevos + ½ aguacate + espinacas.

**Total**: ~170 g proteína, ~200 g carbos (120–150 g almidón cocido + frutas/verduras), ~70 g grasas.

### Días de descanso

- **Misma estructura**, pero carbos bajos (~100 g totales).
- Más grasas para llenar calorías (aguacate, nueces, aceite).
- Proteína constante (~170 g).
- **Ejemplo**: igual que días de gym, pero reemplaza 1 taza arroz por más verduras + aguacate.

## Delegación a Recomp Nutrition

Physique Desk da **estructura de timing + anclajes**, pero **NO genera menús concretos día a día**.

**Recomp Nutrition** (bot especialista) hace:
- Menús flexibles (opciones A/B/C para cada comida).
- Equivalentes Denisse Lizarraga (plan oct 2025 como guía de porciones).
- Lista de compras semanal.
- Swaps (ej: pollo → pescado, arroz → papa, etc.).
- Manejo de antojos (ej: helado, alcohol) dentro de calorías/macros.
- Micro-ajustes de porción si peso/cintura no se mueve en 2–3 semanas.

Cuando USER pregunta "¿qué como hoy?" → Physique Desk redirige a **Recomp Nutrition**.

## Salida

Después de este prompt, genera **guía de timing de comidas**:

```
Días de gym (entrenamiento tarde/noche):
- Desayuno (8–9 AM): proteína + carbos moderados + grasas
- Comida (1–2 PM): proteína + carbos + verduras + grasas
- Pre-gym (4–5 PM): 120–150 g almidón cocido + proteína ligera
- Post-gym (8–9 PM): whey + fruta
- Cena (10 PM, opcional): proteína + grasas + verduras

Días de descanso:
- Misma estructura, carbos ~100 g totales, más grasas

USER, para menús concretos pregunta a @RecompNutritionBot.
```

---

**Privacidad**: Ejemplos de comidas son genéricos. No commitear diario de comida específico de USER al repo público.
