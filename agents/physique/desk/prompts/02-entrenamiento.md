# Prompt 02: Diseño de entrenamiento

**Objetivo**: Crear división de entrenamiento A/B/C (upper/lower/full-body) con selección de ejercicios, sets/reps, y frecuencia semanal.

## Inputs

- **Marco** (del Prompt 01): experiencia, disponibilidad (días/semana, minutos/sesión), restricciones, objetivo.

## Diseño base: A/B/C

### Frecuencia recomendada

- **3 días/semana**: A-descanso-B-descanso-C-descanso-descanso (ejemplo: lun-mier-vier).
- **4 días/semana**: A-B-descanso-C-A-descanso-descanso (hitting algunos grupos 2×/semana).
- **5+ días/semana**: considera A-B-C-A-B-descanso-descanso (cada grupo 2×/semana).

### A: Upper (tren superior)

**Objetivo**: pecho, espalda, hombros, brazos.

- Press banca (o variante inclinado/mancuernas) — 3×8–12
- Remo con barra (o mancuernas/cable) — 3×8–12
- Press militar (o press Arnold/mancuernas) — 3×8–12
- Jalones (o dominadas si puede) — 3×10–15
- Facepulls (cable, banda, o reverso en máquina) — 3×15–20
- Curls bíceps (barra/mancuernas) — 2×10–15
- Tríceps (extensiones/fondos/pushdowns) — 2×10–15

**Volumen total**: ~19 sets tren superior.

### B: Lower (tren inferior)

**Objetivo**: cuádriceps, glúteos, femorales, pantorrillas.

- Sentadilla (barra/frontal/goblet) — 3×8–12
- Peso muerto rumano (o convencional si técnica es buena) — 3×8–12
- Prensa de piernas (o zancadas con mancuernas) — 3×10–15
- Curl nórdico (o femoral en máquina) — 3×8–12
- Pantorrillas (parado/sentado) — 3×12–20

**Volumen total**: ~15 sets tren inferior.

### C: Full-body (cuerpo completo + énfasis glúteos/core)

**Objetivo**: balance, movimientos que A/B no priorizaron, énfasis glúteos.

- Hip thrust (barra o Smith) — 4×10–15
- Press inclinado (o mancuernas) — 3×10–15
- Remo (o jalón, lo que no hiciste en A) — 3×10–15
- Zancadas búlgaras (o split squats) — 3×10–15 por pierna
- Lateral raises (hombro lateral, mancuernas/cable) — 3×12–20
- Abs/core (planks, pallof press, crunch cable) — 3×15–20 o tiempo

**Volumen total**: ~19 sets cuerpo completo + glúteos/core.

## Ajustes según experiencia

- **Novato** (< 1 año): enfatiza técnica, rango 8–12 reps, progresión lineal simple (sube peso cada 1–2 semanas).
- **Intermedio** (1–3 años): rango 6–15 reps según ejercicio (compound 6–10, aislamiento 10–15), progresión double (reps primero, luego peso).
- **Avanzado** (> 3 años): puede agregar sets, drop sets, tempo, periodización — pero no necesario para recomposición básica.

## Ajustes según restricciones

- **Hombro lesionado**: evita press militar vertical, usa variantes neutrales (mancuernas, press Arnold); reduce peso en press banca.
- **Rodilla lesionada**: evita sentadilla profunda, usa sentadilla parcial o prensa de piernas; evita saltos.
- **Espalda baja**: evita peso muerto convencional, usa rumano con peso ligero; enfatiza core.

## Salida

Después de este prompt, genera **plan de entrenamiento A/B/C completo** con:
- Ejercicios específicos (barras/mancuernas/máquinas).
- Sets × reps.
- Orden de ejecución (compound primero, aislamiento después).
- Frecuencia semanal (ejemplo calendario).

Este plan alimenta **Prompt 05 (Progresión)** y **Prompt 07 (Recuperación)**.

---

**Privacidad**: Ejemplos de restricciones son genéricos. No commitear lesiones médicas específicas de USER al repo público.
