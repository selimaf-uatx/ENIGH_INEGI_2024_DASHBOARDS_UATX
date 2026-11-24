### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados con enfoque de género. 2025.
Table 2.4 - Percentage of Quarterly Current Income Earners by Sex and Age Range by Household Income Decile

* **Authors:** María Luisa Rodríguez Hernández
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1m7PkUtnz3K2YnVpezLIpnPYT8QGP1kxVQzODyxzi7ek/edit?gid=1985150242#gid=1985150242)
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/u/3/reporting/061dd37d-1fcc-4d90-b15a-d3351b4b08c6/page/5FiDG)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados con enfoque de género. 2025. Cuadro 2.4 - PORCENTAJE DE PERCEPTORES DE INGRESO CORRIENTE TRIMESTRAL POR SEXO Y RANGOS DE EDAD SEGÚN DECILES DE INGRESO DEL HOGAR.](cuadro_2_4_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`Age Group` (*Grupo de Edad*):**
     *Categorical dimension dividing the population aged 14 and over into age ranges: 14-19, 20-29, 30-39, 40-49, 50-64 and 65+, plus the overall total.*

   * **`Decile` (*Decil*):**
     *Ordinal dimension that ranks households by quarterly current income, from decile I (lowest income) to decile X (highest income), plus the overall total.*

   * **`Gender` (*Género*):**
     *Demographic breakdown identifying both sexes combined (*Ambos sexos*), male (*Hombres*) and female (*Mujeres*).*

   * **`Percentage` (*Porcentaje* - Metric):**
     *Numerical field showing the percentage of people aged 14 and over who receive current income, relative to the total population with the same decile, age range and sex. The closer to 100, the larger the share of income earners.*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, converting the decile columns (I to X) into a single `Decile` column, adding a `Gender` column for each block of the table, and removing title rows, notes and header overlays. Since the metric is a percentage, values are never summed across rows.

   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](cuadro_2_4_tidy_format_table.png)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings (ensuring `Percentage` is set to `AVG` instead of `SUM`, since adding percentages would give meaningless values).

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring a heatmap table of the percentage of income earners by decile, age group and gender, a bar chart of income earners by age group, a bar chart comparing men and women by decile, and dynamic filters for `Age Group`, `Decile` and `Gender`.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](cuadro_2_4_dashboard.png)
