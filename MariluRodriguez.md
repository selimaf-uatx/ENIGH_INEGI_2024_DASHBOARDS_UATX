### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados con enfoque de género. 2025.
CUADRO 2.4 - PORCENTAJE DE PERCEPTORES DE INGRESO CORRIENTE TRIMESTRAL POR SEXO Y RANGOS DE EDAD SEGÚN DECILES DE INGRESO DEL HOGAR
- **Author:** Maria Luisa
- **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1m7PkUtnz3K2YnVpezLIpnPYT8QGP1kxVQzODyxzi7ek/edit?gid=1985150242#gid=1985150242)
- **Interactive Dashboard:** 📊 [View Looker Studio Report](https://lookerstudio.google.com/reporting/061dd37d-1fcc-4d90-b15a-d3351b4b08c6/page/5FiDG)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados con enfoque de género. 2025. Cuadro 2.4 - Porcentaje de perceptores de ingreso.](docs/screenshots/Cuadro_2_4_Porcentaje_perceptores_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`Age Group` (*Grupo de edad*):**
     *Categorical dimension grouping the population into specific age brackets (e.g., 14 a 19 años, 20 a 29 años, ..., 65 y más años).*

   * **`Decile` (*Decil*):**
     *Geographic or economic stratification dimension dividing households into ten equal groups (Deciles I to X) according to their income level.*

   * **`Gender` (*Género*):**
     *Demographic breakdown identifying the population by sex (Hombres, Mujeres, Ambos sexos).*

   * **`Percentage` (*Porcentaje* - Metric):**
     *The numerical percentage metric representing the proportion of current quarterly income earners.*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, removing header overlays and total/subtotal rows to avoid double-counting.
   
##### Normalized Dataset Preview:
![Tidy Data Screenshot](docs/screenshots/Cuadro_2_4_Porcentaje_perceptores_tidy_format_table.png)

5. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings and filter controls.

6. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring key metrics (KPI scorecards), breakdown charts by decile and age group, and dynamic slicers/filters for `Grupo de edad`, `Decil`, and `Genero`.

##### Final Dashboard Preview:
![Dashboard Screenshot](docs/screenshots/Cuadro_2_4_Porcentaje_perceptores_dashboard.png)
