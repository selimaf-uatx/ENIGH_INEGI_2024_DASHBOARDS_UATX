### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 7.1 - TOTAL DE PERSONAS PERCEPTORES DE INGRESO Y SU INGRESO PROMEDIO TRIMESTRAL MONETARIO POR ENTIDAD FEDERATIVA Y TIPO DE DISCAPACIDAD

**Authors:** Rocío Gallegos Reyes  
**Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/15QSmnux9wz6V6u3Wahoe4kmY9rzX7PxoYrBsnPf0rk0/edit?gid=263878760#gid=263878760)  
**Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/0/reporting/6fdc7bef-5b50-4be5-b576-14b16ba51296/page/0QEEG)  

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**  
   * Downloaded raw data table for Cuadro 7.1 evaluating income earners and average quarterly monetary income by federal entity and disability type.  
   ![Original Table Screenshot](docs/screenshots/Cuadro_7_1_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**  
   * **`Entidad Federativa` (State - Qualitative Geographic Dimension):** Geographic dimension covering the 32 federal entities of Mexico plus national aggregates.  
   * **`Tipo de discapacidad` (Disability Type - Qualitative Dimension):** Categorical breakdown distinguishing individuals with and without disabilities, along with specific functional limitations (vision, mobility, hearing, cognitive, self-care, and communication).  
   * **`Personas perceptoras de ingreso` (Income Earners - Quantitative Metric):** Discrete numerical metric counting the total number of individuals receiving monetary income in each group.  
   * **`Ingreso promedio trimestral` (Average Quarterly Income - Quantitative Metric):** Continuous monetary metric measuring average quarterly income in Mexican pesos.  

3. **Tidy Data Transformation:**  
   * Cleaned and restructured the raw tabulations into a flat format (`Tabla limpia`) in Google Sheets, removing merged headers and standardizing currency and integer fields.  
   ##### Normalized Dataset Preview:  
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_7_1_tidy_format_table.png)

4. **BI Connection:**  
   * Connected the processed Google Sheet directly to Looker Studio, enforcing `AVG` aggregation on `Ingreso promedio trimestral` and applying exclusion filters for national and overall total rows where required.

5. **Dashboard Design & Interactive Visuals:**  
   * Built an interactive dashboard featuring comparative KPI scorecards (national, without disability, and with disability), a horizontal bar chart ranking average income by specific disability type, a scatter plot correlating income earners with average quarterly earnings across states, a heatmap detail table, and interactive dropdown filters.  
   ##### Final Dashboard Preview:  
   ![Dashboard Screenshot](docs/screenshots/Cuadro_7_1_dashboard.png)
