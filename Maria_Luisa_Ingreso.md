### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025.
CUADRO 7.4 - INGRESO PROMEDIO TRIMESTRAL MONETARIO POR ENTIDAD FEDERATIVA Y NIVEL DE ESCOLARIDAD SEGÚN SEXO
- **Author:** Maria Luisa[cite: 8]
- **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1FaGUmB3sZr33kyQoXdgvYMW9FN3_53bElbiw2P2LLEo/edit?gid=0#gid=0)
- **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/3/reporting/8884c062-41a0-4dc6-9e6d-98b8289f3bff/page/9kDBG)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025. Cuadro 7.4 - Ingreso promedio trimestral monetario por entidad federativa y nivel de escolaridad según sexo.](docs/screenshots/Cuadro_7_4_Ingreso_escolaridad_sexo_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`State` (*Entidad Federativa*):**
     *Geographic dimension representing the 32 federal entities of Mexico and the national total (NACIONAL).*[cite: 9]

   * **`Education Level` (*Nivel de Escolaridad*):**
     *Categorical dimension classifying educational attainment (e.g., A lo más primaria completa, Secundaria completa o incompleta, Preparatoria completa o incompleta, Profesional completa o incompleta, Posgrado completo o incompleto).*[cite: 9]

   * **`Gender` (*Genero*):**
     *Demographic dimension identifying the population breakdown by sex (Ambos, Hombres, Mujeres).*[cite: 9]

   * **`Average Quarterly Monetary Income` (*Ingreso Promedio* - Metric):**
     *Numerical currency metric representing the average monetary quarterly income in Mexican pesos ($).*[cite: 9, 10]

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, cleaning header rows and aligning variables into tidy columns (`Entidad Federativa`, `Nivel de Escolaridad`, `Genero`, `Ingreso Promedio`).[cite: 9]
   
   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_7_4_Ingreso_escolaridad_sexo_tidy_format_table.png)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating currency formatting ($) and metric aggregation settings.[cite: 10]

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring KPI scorecards, state-by-state income ranking charts, percentage distribution charts by gender and education level, and dynamic filters/slicers for `Genero`, `Entidad Federativa`, and `Nivel de Escolaridad`.[cite: 10]

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](docs/screenshots/Cuadro_7_4_Ingreso_escolaridad_sexo_dashboard.png)
