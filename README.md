# Adrian's portfolio

## [Power BI---Performance Analyst Dashboard](https://adedllanes23.github.io/Adrian-portfolio/)

**Resumen rápido**  
Dashboard interactivo de desempeño (Plant Co.) que permite analizar Valores YTD, comparación YTD vs PYTD, beneficio bruto (GP%) y segmentación por país, producto, cuenta y temporalidad. El reporte está pensado para equipos comerciales y de operaciones que necesiten priorizar inventario, promociones y acciones de mejora de margen.

---

## Contexto  
Una compañía de plantas y productos asociados buscaba visibilidad clara de su desempeño 2023 para:
- Identificar regiones y cuentas que arrastran pérdidas frente al año anterior.
- Detectar meses con variaciones significativas en Valor.
- Priorizar acciones para mejorar margen (GP%) sin sacrificar volumen.

---

## Objetivo  
Proveer un **dashboard operativo** que responda en tiempo real a preguntas como:
- ¿En qué países o cuentas estamos perdiendo ritmo respecto al año anterior?
- ¿Qué meses y líneas de producto impulsan o reducen el Valor YTD?
- ¿Qué cuentas con alto Valor requieren intervención para mejorar GP%?

---

## Herramientas usadas  
- **Power BI Desktop**: diseño de reporte, DAX para medidas clave (YTD, PYTD, Cantidad, Ventas, Beneficio neto, medidas de titulos dinámicos).   
- **Excel**: limpieza inicial, validación y exploración de base de datos.   
- **Git / GitHub**: versionado y publicación (GitHub Pages para portfolio).

---

## Visual principal
![Portada del dashboard](./assets/dashboard_cover.png)

(visual que muestra: KPI cards: YTD, YTD vs PYTD, S_PYTD, GP% — Treemap por países, Waterfall por mes de YTD vs PYTD, Stacked bar por producto y scatter GP% vs Value con filtros interactivos)

---

## Hallazgos clave (resumido y accionable)
- **Quantity YTD positivo pero marginal**: `YTD (2023) = 555.66K` y `YTD vs PYTD = +17.05K` — crecimiento neto modesto respecto al año anterior.  
- **Concentración de pérdidas en países específicos**: China (-9.76K) y France (-9.36K) aparecen entre las mayores caídas de Quantity YTD vs PYTD; requieren diagnóstico inmediato.  
- **Picos estacionales**: Febrero, julio y octubre del año 2023 tienen un bache notable con respecto al año pasado en Ventas.
- **Productos**: las categorías **Landscape / Outdoor** sostienen gran parte del Valor en meses pico; revisar disponibilidad de inventario por producto.  
- **Oportunidad de margen en cuentas grandes**: el scatter muestra cuentas con **alto Value y GP% por debajo del umbral (~40%)** — hay espacio para acciones de pricing / renegociación de condiciones.  
- **Segmentos que mejoran vs que retroceden**: aunque el neto es positivo, la variación está impulsada por pocos meses/países; el crecimiento no es homogéneo.

---

## Impacto recomendado (prioridades — corto/medio plazo)
1. **Investigación rápida en China y France** — asignar un owner para:
   - Revisar promociones aplicadas y su efecto en margen.
   - Verificar problemas logísticos o descuentos no autorizados.
2. **Reasignación táctica de inventario** a regiones con crecimiento (aprovechar el pico en abril), anticipar suministro para próximos picos estacionales.  
3. **Programa de mejora de margen en cuentas clave**:
   - Identificar top-20 cuentas por Value y negociar condiciones / revisar costos.
   - Implementar alertas semanales para cuentas con GP% < 40% y Value > umbral.  

---

## Archivos del proyecto (qué subir al repo)
- `project-powerbi-performance/README.md` (este archivo – Project Cover)  
- `project-powerbi-performance/detailed-report.md` (metodología, DAX, queries y limitaciones)  
- `project-powerbi-performance/pbix/Plant_Performance_Dashboard.pbix` *(archivo Power BI — opcional: usar Git LFS o Releases)*  
- `project-powerbi-performance/sample_data/plant_sales_sample.csv` (dataset reducido reproducible)  
- `project-powerbi-performance/sql/queries.sql` (scripts de extracción y transformaciones)  
- `project-powerbi-performance/assets/dashboard_cover.png` (imagen estática para portada)  
- `project-powerbi-performance/assets/interaction.gif` (GIF corto que muestra filtros / drill-down)

---

## Nota sobre reproducibilidad y privacidad
- He incluido un `sample_data/` reducido y anonimizado para que el análisis sea reproducible y sin PII.  
- Si subes el `.pbix` real, usa **Git LFS** o sube el `.pbix` como **release** para no inflar el historial Git.


