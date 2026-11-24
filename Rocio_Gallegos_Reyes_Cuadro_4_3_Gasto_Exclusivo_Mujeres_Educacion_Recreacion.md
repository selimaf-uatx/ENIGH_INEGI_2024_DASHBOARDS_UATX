### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 4.3 - PORCENTAJES DE GASTO EXCLUSIVO PARA MUJERES EN EDUCACIÓN, CULTURA Y RECREACIÓN

**Authors:** Rocío Gallegos Reyes  
**Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1SpfRoAr2fDNStOutn8g4Ff5dmJY10tOTNwkF7gRcbUU/edit?gid=1022311727#gid=1022311727)  
**Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/0/reporting/359781a5-7a65-499d-b4a2-de5c026db83a/page/cAEEG)  

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**  
   * Downloaded raw data table for Cuadro 4.3 analyzing the percentage of current monetary expenditure dedicated exclusively to women in education, culture, and recreation.  
   ![Original Table Screenshot](docs/screenshots/Cuadro_4_3_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**  
   * **`Rubro de gasto` (Expenditure Item - Qualitative Dimension):** Categorical breakdown of educational and recreational goods and services (basic/higher education, educational supplies, cultural items, and recreation services).  
   * **`Criterio de desagregación` (Disaggregation Criterion - Qualitative Dimension):** Classification grouping the analysis by locality size (`TAMAÑO DE LOCALIDAD`), household size (`TAMAÑO DE HOGAR`), and income deciles (`DECILES DE HOGARES SELECCIONADOS`).  
   * **`Categoria` (Category - Qualitative Dimension):** Specific demographic or socioeconomic segments within each criterion (e.g., `< 2,500` vs. `≥ 2,500` inhabitants, household member counts, and deciles I–X).  
   * **`Porcentaje de gasto` (Expenditure Percentage - Quantitative Metric):** Numerical indicator representing the percentage share of monetary spending allocated exclusively to women.  

3. **Tidy Data Transformation:**  
   * Normalized the original cross-tabulated matrix into a flat structure (`Tabla limpia`) in Google Sheets, standardizing percentage formats and structuring disaggregation criteria into dedicated columns to prevent aggregation distortion.  
   ##### Normalized Dataset Preview:  
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_4_3_tidy_format_table.png)

4. **BI Connection:**  
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, setting `Porcentaje de gasto` aggregation to `AVG` (average) and applying custom filters to isolate specific disaggregation criteria and exclude total rows.

5. **Dashboard Design & Interactive Visuals:**  
   * Built an interactive dashboard featuring KPI scorecards, comparative bar charts by expenditure item and locality size, a donut chart showing spending distribution, a heatmap table, and dropdown controls for `Criterio de desagregación` and `Rubro de gasto`.  
   ##### Final Dashboard Preview:  
   ![Dashboard Screenshot](docs/screenshots/Cuadro_4_3_dashboard.png)
