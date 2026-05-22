# Las 56 Empresas Públicas de Bolivia — Diagnóstico Fiscal

**Versión v1.0** · revisión continua · publicado 2026-05-21
**Sitio público:** https://romer288.github.io/empresas-publicas-bolivia/
**Issues / corrección de datos:** https://github.com/romer288/empresas-publicas-bolivia/issues

Diagnóstico fiscal y operativo de las 56 empresas públicas bolivianas, basado en sus estados financieros 2023-2025 publicados oficialmente, datos del Sistema de Gestión Pública (SIGEP) y la Ley del PGE 2026.

> **Audiencia primaria:** ciudadanos, periodistas, técnicos del Estado, políticos. Lenguaje plain-Spanish, no técnico. Para audiencia técnica/académica ver pestaña de Metodología.

---

## 📖 Por dónde empezar

1. **[Cómo leer este estudio](10_como_leer.html)** — qué dice y qué NO dice. **Leer primero.**
2. **[Resumen Ejecutivo](08_resumen_ejecutivo.html)** — 60-90 segundos: las 9 preguntas + el escándalo + la proyección 2026.
3. **[Resumen General](00_resumen_general.html)** — drill-down completo de las 9 preguntas, empresa por empresa.
4. **[Por Empresa Individual](04_por_empresa.html)** — fichas de las 56 empresas, una por una.
5. **[Dataset CSV descargable](empresas_publicas_bolivia_dataset.csv)** — 56 filas, 28 columnas, para auditar los datos sin pasar por la interpretación.

---

## 📄 Páginas del sitio

| Página | Contenido |
|---|---|
| [📖 10_como_leer.html](10_como_leer.html) | Página de aterrizaje: qué dice y qué NO dice el estudio, cómo distinguir hechos de inferencias, framework de las 3 preguntas (salud × función × acción). |
| [08_resumen_ejecutivo.html](08_resumen_ejecutivo.html) | Vista de 60-90 segundos: las 9 preguntas agregadas, maquillaje contable, las gigantes, marco legal de tocabilidad, proyección 2026 sistema + forecast empresa por empresa de las 10 más grandes. |
| [00_resumen_general.html](00_resumen_general.html) | Las 9 preguntas con drill-down: cada bucket clickeable muestra las empresas con sus cifras concretas. Vista **sin subsidios** (operativa). |
| [07_resumen_general_con_subsidios.html](07_resumen_general_con_subsidios.html) | Misma estructura que el general pero **incluyendo** subsidios y transferencias del Estado en los cálculos (vista contable). |
| [01_por_arquetipo.html](01_por_arquetipo.html) | Empresas agrupadas por arquetipo: Defuncto, Colapso, Zombie, Capital Agotado, Trampa de Cobranza, Bajo Desempeño, Comercialmente Sano, Distrés Mixto, Datos Insuficientes. |
| [02_por_recomendacion.html](02_por_recomendacion.html) | Empresas agrupadas por verbo de acción: Cerrar, Liquidar, Reestructurar, Recapitalizar, Privatizar, Mantener, Diagnóstico Específico. |
| [03_matriz.html](03_matriz.html) | Matriz visual 5 funciones × 6 niveles de salud = 30 celdas. Cada empresa cae en una celda según el marco legal de tocabilidad. |
| [04_por_empresa.html](04_por_empresa.html) | Tarjeta por cada una de las 56 empresas con link a la ficha completa. |
| [05_metodologia.html](05_metodologia.html) | Fórmulas exactas de las 9 preguntas, fuentes PCSP/SIGEP, régimen cambiario, BCB implícito, M9b reexpresado, decisiones controvertibles documentadas. |
| [09_costo_estudio.html](09_costo_estudio.html) | Cuánto habría costado al ciudadano que una consultora hiciera este estudio (4 escenarios: think tank/universidad · consultora local BO · Big4 BO · top-tier internacional). |
| **56 fichas individuales** | Una por empresa, formato `{code}_{SIGLA}.html` (ej: `0513_YPFB.html`). |

---

## 🧠 Metodología — las 9 preguntas

Cada empresa se evalúa con 9 preguntas, cada una con métrica ancla y fórmula auditable. Detalle completo en la [pestaña de Metodología](05_metodologia.html).

| # | Pregunta | Métrica ancla |
|---|---|---|
| 1 | ¿Está vendiendo más o menos cada año? | M7 (Δ op_revenue 3y) |
| 1 (parte 2) | ¿Cobra a tiempo? | M3 / AR ratio |
| 2 | ¿La ganancia se convierte en plata? | Op-EBITDA bottom-up vs cash neto SIGEP |
| 3 | ¿Está legalmente solvente? | M9b (pérdidas reexpresadas / capital reexpresado) |
| 4 | ¿Depende del Estado? | M17_v5 = (TGN + Rec.Específicos) / Op_Revenue |
| 5 | ¿Cuánto le cuesta al Estado? | Monto SIGEP + estimación BCB implícito |
| 6 | ¿El dinero del Estado rinde? | M15 (ROIC) |
| 7 | ¿Productividad operacional? | Δ gasto puro − Δ op_revenue (pp) |
| 8 | ¿Liquidez / meses de supervivencia? | M2 + Op-EBITDA mensual |
| 9 | ¿En qué gasta? ¿Hay señales irregulares? | Subpartidas SIGEP nivel 4 + banderas rojas |

Score multidimensional 0-25+ → 6 niveles de salud (Buen Desempeño / Bajo Desempeño / Deteriorada Leve / Deteriorada Grave / Quebrada / Defuncta).

---

## 📊 Fuentes de datos

- **Estados financieros 2023-2025**: PDFs publicados oficialmente por las propias empresas (SEPEC/MEFP). Extraídos vía pipeline OCR multi-motor con consenso (Mistral, GPT-4 Vision, Gemini, Azure Document Intelligence).
- **Plan de Cuentas del Sector Público (PCSP)**: estructura contable obligatoria para empresas públicas — cuentas 1 (Activo), 2 (Pasivo), 3 (Patrimonio), 5 (Ingresos), 6 (Gastos).
- **SIGEP — Sistema de Gestión Pública**: transferencias TGN, transferencias Recursos Específicos, gasto por grupo, ingreso por tipo.
- **Ley del PGE 2026** (Ley de Modificaciones al Presupuesto General del Estado - Gestión 2026, firmada Presidente Paz, abril 2026): presupuesto autorizado por empresa.

**Para 2026**, el gobierno aún NO ha publicado la partida de ejecución presupuestaria por empresa. Las proyecciones 2026 son modelos con supuestos explícitos (subsidio combustibles eliminado vía decreto sucesor de DS 5503 abrogado, paralelo Bs 9,85-10,05 mayo 2026), NO son datos reales de ejecución.

---

## 🔬 Reproducibilidad

El reporte se genera con el script `60_build_citizen_reports.py` (parte del repositorio de extracción original). Para reproducir:

```bash
cd "Bolivian Companies/extraction"
python3 60_build_citizen_reports.py
# Output: output/citizen_reports/
```

Dependencias: `pandas`, `openpyxl`, `python` 3.10+. El pipeline upstream que produce el workbook financiero (`audit_metrics_v8.py` → `54_build_financial_metrics_v9.py` → `56_build_v9_by_bucket.py`) está documentado en `Bolivian Companies/extraction/docs/00_PIPELINE_ORDER.md`.

---

## ⚠️ Limitaciones conocidas

1. **5 empresas sin estados financieros 2025 publicados**: EPDEOR, EMAPAV, EMAVERDE, KALLPAWAWA, FCCCP-EPD. Para estas, el análisis usa SIGEP cuando existe y se marca confianza baja en el [dataset CSV](empresas_publicas_bolivia_dataset.csv).
2. **Subsidio cambiario BCB es estimación**: rango Bs 12-20 mil M (estimación central ~Bs 16 mil M). Depende de supuestos sobre volumen de USD entregados por BCB al oficial y promedio anual del paralelo durante 2025 (que varió entre Bs 9 y Bs 19).
3. **Recomendaciones son triage fiscal preliminar**: NO sustituyen auditoría legal, social ni sectorial. Cualquier acción administrativa (cierre, fusión, liquidación) requiere validación jurídica formal previa por abogado boliviano de derecho corporativo/público.
4. **No mide valor social ni impacto distributivo**: una empresa puede ser financieramente deficitaria y aun así cumplir una función social legítima. Este estudio mide sostenibilidad fiscal y operativa.
5. **Causas inferidas en las fichas son contexto interpretativo**: los datos son auditables hasta el PDF fuente; las causas son explicaciones operativas/sectoriales que pueden tener interpretaciones alternativas. Marcadas visualmente con caja "💡 Causas inferidas" en cada ficha.

---

## 📝 Cómo reportar errores o sugerir correcciones

**Issues en GitHub** (preferido): https://github.com/romer288/empresas-publicas-bolivia/issues

Cualquier ciudadano, periodista, académico, funcionario o representante de las empresas puede reportar:
- Errores de datos verificables contra PDFs oficiales.
- Errores de clasificación legal o funcional.
- Causas inferidas con explicación alternativa razonable.
- Inconsistencias internas.

Todas las correcciones se publicarán con registro público de cambios en commits del repositorio.

---

## 📜 Licencia y uso

Datos públicos extraídos de fuentes oficiales del Estado Boliviano. El análisis y código se publican como bien público — uso libre con atribución. Si se cita en prensa o análisis, idealmente con link a la fuente y al [dataset CSV](empresas_publicas_bolivia_dataset.csv) para que el lector pueda verificar.
