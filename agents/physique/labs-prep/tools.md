# Labs Prep — Tools

Conectores y herramientas que Labs Prep usa.

## Uso directo

### Archivos subidos por usuario
- **Propósito**: USER sube PDFs, imágenes, o documentos de labs desde laboratorios clínicos.
- **Cuándo**: USER dice "organiza mis labs" o sube archivos directamente en conversación.
- **Lectura**: Labs Prep lee texto/valores de documentos usando capacidades de lectura de documentos de Grok (OCR si es imagen/PDF escaneado, parsing si es PDF con texto).

## NO usa

- **NO hay conector clínico en vivo** (no API de laboratorio, no integración con sistemas médicos).
- **NO usa Garmin MCP** (Garmin no tiene labs clínicos — eso es Load & Recovery).
- **NO usa MyFitnessPal MCP** (MFP tiene peso, no labs clínicos).
- **NO usa Hevy MCP** (Hevy tiene entrenamiento, no labs clínicos).
- **NO usa Evidence Desk** (Evidence Desk busca papers, no organiza labs reales).

## Privacidad

- Este archivo lista capacidades por **nombre solamente**.
- **Cero API keys de servicios médicos** (este bot no se conecta a sistemas de laboratorios clínicos en vivo).
- **Cero valores reales de labs** commitados a este repo.

---

**Nota de privacidad**: Labs reales viven en archivos subidos por USER en conversación en vivo con el bot, nunca en este repo público.
