# Physique Team

Sistema de bots especialistas para recomposición corporal — versión pública del equipo Grok Bot de Eduardo E. Ramos.

## English

This repository scaffolds the **Physique Team**: a hub-and-specialist Grok Bot system for evidence-based body recomposition (strength training, progressive overload, flexible nutrition, recovery).

- **Hub**: Physique Desk — owns training split (A/B/C upper/lower/full-body), progression, macro anchors (~170 g protein, gym carbs 120–150 g, rest ~100 g), weekly tracker.
- **Specialists**:
  - Load & Recovery — Garmin Connect MCP → traffic light + 1–3 weekly adjustments.
  - Recomp Nutrition — turns anchors into flexible menus, shopping lists, portion micro-adjusts (uses MyFitnessPal MCP when diary exists).
  - Evidence Desk — sport science / hypertrophy / nutrition papers on demand (Schoenfeld, Renaissance Diet 2.0, McDonald, etc.) → dated claim+source bullets + practical implication.

**Privacy**: This repo contains **no** API keys, cookies, OAuth tokens, emails, weights, HRV series, food diaries, or workout IDs. Connector names only. See `docs/CONNECTORS.md`.

**Owner**: [@EERamos](https://github.com/EERamos)

---

## Español

Este repositorio documenta el **Physique Team**: sistema Grok Bot de coach hub + especialistas para recomposición corporal (entrenamiento de fuerza, sobrecarga progresiva, nutrición flexible, recuperación basada en evidencia).

### Agentes

#### 1. Physique Desk (hub)
- **Rol**: coach recomposición — evaluación de marco, entrenamiento (fuerza/hipertrofia), anclajes de nutrición, progresión, tracker semanal, orquestación de recuperación.
- **Framework**: 8 prompts (analizar marco → entrenamiento → nutrición recomp → guía de comidas → progresión → tracker → recuperación → sistema completo).
- **Anti-trabajos**: fantasy NFL / Polymarket; inventar laboratorios médicos; prescribir medicamentos; publicaciones externas sin autorización.
- **Voz**: español, claro, accionable, sin exageración.
- **Dueño de**: división A/B/C, reglas de progresión, anclajes de macros (~170 g proteína piso práctico; carbos gym 120–150 g almidón cocido, resto ~100 g).

#### 2. Load & Recovery
- **SOLO**: interpretar datos Garmin Connect MCP (sueño, pasos, HRV, body battery, estrés, preparación, actividades, training status) → semáforo + 1–3 ajustes semanales.
- **Framework**: medido → significado de fatiga → cambio (volumen, timing, LISS, sueño, descarga).
- Silencioso si no hay sincronización útil. Nunca diagnóstico/prescripción. Duración de fuerza en Garmin NO es proxy de volumen.

#### 3. Recomp Nutrition
- **SOLO**: convertir anclajes en comida diaria — menús flexibles, equivalentes Denisse Lizarraga (plan oct 2025 como guía de porciones), lista de compras, antojos/alcohol, micro-ajustes de porción desde reportes de peso/cintura/fotos.
- NO cambia kcal/anclajes de proteína ni división de gym solo (Physique Desk cierra esos).
- Usa MyFitnessPal MCP cuando existe diario; compara vs ~170 g proteína.

#### 4. Evidence Desk
- **SOLO**: ciencia del deporte / hipertrofia / evidencia de nutrición con reclamos fechados + fuentes (Schoenfeld Hypertrophy; Renaissance Diet 2.0; McDonald Stubborn Fat; revisiones).
- **Salida**: pregunta → 3–7 bullets reclamo+fuente+año → 1–2 líneas implicación práctica (no reescribe rutina completa).
- Physique Desk traduce en plan.
- **Literatura de referencia**: ver `knowledge/` para resúmenes accionables de libros clave (sin PDFs completos).

### Arquitectura

```
agents/physique/
├── desk/              # Physique Desk (hub)
├── load-recovery/     # Load & Recovery
├── recomp-nutrition/  # Recomp Nutrition
└── evidence-desk/     # Evidence Desk
```

Cada bot incluye: `README.md`, `persona.md`, `CONTEXT.md`, `tools.md`.  
Physique Desk incluye además `prompts/01-08.md` (framework de 8 prompts).

### SOP

Flujo documentado en `docs/SOP.md`:
- **Usuario**: registra gym en Hevy (cuando esté listo), comida en MFP, usa Garmin.
- **Physique Desk**: hub — división, progresión, anclajes de macros.
- **Load & Recovery**: Garmin → semáforo + 1–3 ajustes.
- **Recomp Nutrition**: menús/intercambios dentro de anclajes; MFP vs proteína.
- **Evidence Desk**: papers bajo demanda.
- **Chief**: triage general solamente.

**Cadencia**:
- Domingo ~9:11 America/Mexico_City: revisión semanal Garmin (la rutina vive en Physique Desk).
- On-demand: "¿qué hoy?", menú, pase de carga, evidencia.
- Después de registro Hevy → nota de progresión Desk.
- Después de días de diario MFP → brechas Recomp Nutrition.

### Conectores

Ver `docs/CONNECTORS.md` para mapa de conectores (solo nombres — sin secretos).

**Conexiones pendientes**: Hevy MCP y MyFitnessPal MCP están conectados en vivo, sistema diseñado, esperando acción del usuario / primeros logs. Ver `docs/PENDING_CONNECTIONS.md` para detalles.

### Privacidad

Este repositorio público contiene **cero**:
- Claves API, cookies, tokens OAuth
- Correos electrónicos, números de teléfono
- Series de peso real, volcados HRV, diarios de comida
- IDs de entrenamiento de cuentas en vivo

Usa placeholders de ejemplo donde sea necesario (`USER`, `~170 g proteína`, `gym tarde`).

### Licencia

MIT — ver `LICENSE`.

### Pendiente (TODO documentado, no inventado)

- Subir rutinas A/B/C + core a Hevy cuando el usuario lo solicite.
- Primeros registros reales Hevy/MFP para cerrar el ciclo.

---

## Documentación adicional

- `docs/SOP.md` — workflow completo.
- `docs/CONNECTORS.md` — mapa de conectores, sin secretos.
- `docs/PENDING_CONNECTIONS.md` — conexiones Hevy/MFP: live, diseñadas, esperando usuario.
- `docs/PERSONA_VS_CODE.md` — persona Grok (en vivo) vs este repo (versionado).
- `knowledge/` — resúmenes de literatura (Schoenfeld, Renaissance Diet 2.0, McDonald, etc.).
- `agents/physique/<bot>/` — README, persona, contexto, herramientas por bot.
