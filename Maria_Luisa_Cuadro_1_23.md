### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025.
CUADRO 1.23 - VIVIENDAS POR ENTIDAD FEDERATIVA, SEGÚN TIPO DE TENENCIA DE LA VIVIENDA
- **Author:** Maria Luisa
- **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1SEQcH-NlH6iCFjRlJT8SAV8ZQk12eJVjLHRqJnBkSK8/edit?gid=1968418830#gid=1968418830)
- **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/3/reporting/8ea8c4cd-47b4-42cc-870a-2caa64f62032/page/RvdDG)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025. Cuadro 1.23 - Viviendas por entidad federativa, según tipo de tenencia de la vivienda.](docs/screenshots/Cuadro_1_23_Viviendas_tenencia_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`State` (*Entidad Federativa*):**
     *Geographic dimension representing the 32 federal entities/states of Mexico.*

   * **`Housing Tenure` (*Tipo de Tenencia*):**
     *Categorical dimension classifying housing occupancy status (Propia, Rentada, Prestada, Propia pero la están pagando, Intestada o en litigio, Otra situación).*

   * **`Dwellings - Absolute` (*Viviendas (Absolutos)* - Metric):**
     *Numerical count representing the number of dwellings in each category.*

   * **`Percentage - Relative` (*Porcentaje (Relativos)* - Metric):**
     *Numerical percentage metric representing the relative share of each tenure type within a state.*

   * **`Total Dwellings` (*Total de viviendas* - Metric):**
     *Numerical field indicating the total dwelling count per federal entity.*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, removing header overlays and total/subtotal rows to avoid double-counting.
   
   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_1_23_Viviendas_tenencia_tidy_format_table.png)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings and filter controls.

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring key metrics (KPI scorecards), national distribution and state ranking charts, and dynamic slicers/filters for `Entidad Federativa`, `Tipo de Tenencia`, and `Viviendas (Absolutos)`.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](docs/screenshots/Cuadro_1_23_Viviendas_tenencia_dashboard.png)
