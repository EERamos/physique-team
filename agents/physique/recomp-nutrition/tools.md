# Recomp Nutrition — Tools

Conectores MCP que Recomp Nutrition usa.

## Uso directo

### user-myfitnesspal (MyFitnessPal MCP)
- **Propósito**: leer diario de comida (food diary), peso, comparar proteína diaria vs ~170 g objetivo.
- **Cuándo**:
  - Physique Desk pregunta: "Revisa MFP de USER últimos 7 días, ¿llegó a ~170 g proteína?"
  - USER pregunta: "¿Cómo voy con mi nutrición?"
  - Después de que USER tiene días de diario MFP registrados → Recomp Nutrition compara vs anclajes.
- **Datos que lee**:
  - Proteína diaria (g).
  - Carbos diarios (g).
  - Grasas diarias (g).
  - Calorías diarias (kcal).
  - Peso corporal (si USER lo registra en MFP).
- **Output**: comparación vs anclajes (~170 g proteína, ~200 g carbos días gym, ~100 g carbos días descanso, 60–80 g grasas, ~2200–2400 kcal) + sugerencias de ajuste.

## No usa

- **NO usa Hevy** (sets/reps son territorio de Physique Desk, no Recomp Nutrition).
- **NO usa Garmin** (recuperación es territorio de Load & Recovery, no Recomp Nutrition).
- **NO usa Strava** (cardio es contexto para Physique Desk / Load & Recovery, no Recomp Nutrition).

## Delegación

Recomp Nutrition **NO delega a otros bots** — es especialista puro (recibe anclajes de Physique Desk → genera menús/swaps/lista de compras → compara MFP vs anclajes cuando USER lo registra).

---

**Privacidad**: Este archivo lista conectores por **nombre solamente**. Cero API keys, OAuth tokens, cookies, diarios de comida reales, o user IDs commitados a este repo.
