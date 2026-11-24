### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.
Table 7.4 - Average Quarterly Monetary Income by State and Education Level by Sex

* **Authors:** María Luisa Rodríguez Hernández
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1FaGUmB3sZr33kyQoXdgvYMW9FN3_53bElbiw2P2LLEo/edit?gid=936074724#gid=936074724)
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/3/reporting/8884c062-41a0-4dc6-9e6d-98b8289f3bff/page/9kDBG/edit)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGIEncuesta Nacional de Ingresos y Gastos de los Hogares ENIGH 2024 Tabulados por entidad federativa 2025 Cuadro 7.4 - INGRESO PROMEDIO TRIMESTRAL MONETARIO POR ENTIDAD FEDERATIVA Y NIVEL DE ESCOLARIDAD SEGÚN SEXO.](original_table.jpeg)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`State` (*Entidad Federativa*):**
     *Geographic dimension representing the national total and the 32 federal entities/states of Mexico.*

   * **`Education Level` (*Nivel de Escolaridad*):**
     *Categorical dimension classifying the population by highest education level reached: up to complete primary, secondary (complete or incomplete), high school (complete or incomplete), undergraduate (complete or incomplete), and graduate studies (complete or incomplete).*

   * **`Gender` (*Género*):**
     *Demographic breakdown identifying both sexes combined (*Ambos*), male (*Hombres*) and female (*Mujeres*).*

   * **`Average Income` (*Ingreso Promedio* - Metric):**
     *The numerical field measuring the average quarterly monetary income, in Mexican pesos, for each combination of state, education level and gender.*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, converting the Total, Hombres and Mujeres columns into a single `Gender` column, and removing header overlays and title rows. Since the metric is an average, values are never summed across rows.

   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](dashboard.jpeg)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings (ensuring `Average Income` is set to `AVG` instead of `SUM`, since it is an average).

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring key metrics (KPI scorecards), a grouped bar chart comparing average income by education level and gender, a heatmap table by state, and dynamic slicers/filters for `State`, `Education Level`, and `Gender`.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](tidy_format_table.png)
