# Labs Prep — Context

Marco genérico de organización de laboratorios médicos para consulta deportiva. **Sin valores reales de labs, sin PII de salud, sin nombres de pacientes/médicos reales** — solo placeholders (USER, médico deportivo real, Laboratorio X).

## Labs deportivos comunes

Lista de análisis clínicos típicos para deportistas / recomposición corporal (checklist de referencia — NO todos son necesarios para cada persona, el médico real decide):

### Hematología
- Hemograma completo (hemoglobina, hematocrito, leucocitos, plaquetas, diferencial).

### Perfil tiroideo
- TSH (hormona estimulante de tiroides).
- T4 libre (tiroxina libre).
- T3 libre (triyodotironina libre).
- Anticuerpos anti-TPO (si sospecha autoinmune).

### Perfil hormonal
- Testosterona total.
- Testosterona libre (calculada o medida directamente).
- SHBG (globulina fijadora de hormonas sexuales).
- Estradiol (E2).
- LH (hormona luteinizante), FSH (hormona folículo-estimulante) — si sospecha hipogonadismo.
- Cortisol AM (8–9 AM en ayunas).

### Vitaminas y minerales
- Vitamina D (25-OH).
- Vitamina B12.
- Hierro sérico.
- Ferritina.
- Magnesio.

### Perfil metabólico
- Glucosa en ayunas.
- Insulina en ayunas (si sospecha resistencia a insulina).
- HbA1c (hemoglobina glucosilada).
- Perfil lipídico (colesterol total, LDL, HDL, triglicéridos).

### Función renal
- Creatinina.
- BUN (nitrógeno ureico en sangre).
- Tasa de filtración glomerular estimada (eGFR).

### Función hepática
- ALT (alanina aminotransferasa).
- AST (aspartato aminotransferasa).
- Bilirrubina total.
- Fosfatasa alcalina.

### Otros (según caso)
- Proteína C reactiva (PCR) — inflamación.
- Homocisteína — riesgo cardiovascular.
- Ácido úrico — gota, función renal.

## Formato de inventario típico

**INVENTARIO DE LABS (fecha, laboratorio)**

| Análisis | Valor | Rango referencia (del lab) |
|----------|-------|----------------------------|
| Ejemplo: Hemoglobina | 15.2 g/dL | 13.5–17.5 g/dL |
| Ejemplo: TSH | 2.34 µIU/mL | 0.4–4.0 µIU/mL |
| ... | ... | ... |

**PREGUNTAS PARA TU MÉDICO**:
1. [Pregunta basada en labs presentes]
2. [Pregunta basada en labs presentes]
3. ...

## Banderas rojas (derivar a médico real inmediatamente)

Si USER menciona síntomas graves (no valores de labs, sino síntomas clínicos):
- Dolor de pecho / opresión torácica.
- Sangrado anormal (hematuria, sangre en heces, sangrado vaginal anormal).
- Pérdida de peso involuntaria rápida (>5% peso en 1 mes sin dieta).
- Fiebre persistente sin explicación.
- Fatiga extrema que impide actividades diarias.
- Palpitaciones severas / desmayos.

→ Decir "ve a tu médico real o urgencias ahora" y parar — no jugar a médico, no interpretar labs en esos casos.

## Privacidad

- Este `CONTEXT.md` contiene **solo marco genérico de labs deportivos comunes**.
- **Cero valores reales de labs de USER** (no commitear hemoglobina real, TSH real, testosterona real, etc.).
- **Cero nombres de laboratorios reales de USER** (usar placeholder "Laboratorio X").
- **Cero emails/teléfonos de médicos reales** (usar placeholder "médico deportivo real").

---

**Nota de privacidad**: Este archivo es **solo referencia de organización**. Labs reales viven en archivos subidos por USER en conversación en vivo, nunca en este repo público.
