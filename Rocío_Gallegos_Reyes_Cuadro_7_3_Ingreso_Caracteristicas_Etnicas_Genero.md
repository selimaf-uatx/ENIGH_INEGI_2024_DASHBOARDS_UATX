### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 7.3 - INGRESO PROMEDIO TRIMESTRAL MONETARIO POR ENTIDAD FEDERATIVA Y CARACTERÍSTICAS ÉTNICAS SEGÚN SEXO

**Authors:** Rocío Gallegos Reyes  
**Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1w1bVY6P2cMRUcBAKMbBfUuIXILlEcXaMGJShIcuuKOc/edit?gid=1550471446#gid=1550471446)  
**Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/0/reporting/77274d03-86f6-45f2-9db0-04d3c17773b2/page/0jBBG)  

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**  
   * Downloaded raw data table for Cuadro 7.3 examining average quarterly monetary income by federal entity, ethnic self-identification or indigenous language speaking status, and gender.  
   ![Original Table Screenshot](docs/screenshots/Cuadro_7_3_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**  
   * **`Entidad Federativa` (State - Qualitative Geographic Dimension):** Geographic dimension representing the 32 federal entities of Mexico and the national benchmark.  
   * **`Características étnicas` (Ethnic Characteristics - Qualitative Dimension):** Categorical dimension distinguishing individuals who self-identify as indigenous, speak an indigenous language, or both, alongside general state averages.  
   * **`Genero` (Gender - Qualitative Dimension):** Demographic breakdown separating male (`HOMBRES`) and female (`MUJERES`) income earners.  
   * **`Ingreso` (Average Quarterly Income - Quantitative Metric):** Continuous numerical indicator measuring average quarterly monetary income in Mexican pesos.  

3. **Tidy Data Transformation:**  
   * Unpivoted the multi-column gender layout (`HOMBRES` and `MUJERES`) from the original INEGI table into a normalized vertical structure (`Tabla modificada`) in Google Sheets, consolidating gender into a single categorical column (`Genero`) and standardizing monetary values.  
   ##### Normalized Dataset Preview:  
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_7_3_tidy_format_table.png)

4. **BI Connection:**  
   * Connected the modified Google Sheet directly to Looker Studio as a live data source, configuring `Ingreso` with `AVG` aggregation to ensure accurate cross-filtering by state, gender, and ethnic characteristics.

5. **Dashboard Design & Interactive Visuals:**  
   * Built an interactive dashboard displaying KPI scorecards for gender and ethnic income gaps, comparative charts across ethnic categories and sex, a state-level breakdown table, and dynamic dropdown filters for `Entidad Federativa`, `Características étnicas`, and `Genero`.  
   ##### Final Dashboard Preview:  
   ![Dashboard Screenshot](docs/screenshots/Cuadro_7_3_dashboard.png)
