### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.
Cuadro 3.2 - [Cantidad de vehículos por cada cien hogares por entidad federativa y tipo de vehículo]
* **Authors:** [Salma Belén Varela / Nombre de tu compañero]
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1PkOHHycnDcKkS_eZa1S9038R9OyEVcO0wSsxKjYtc7Y/edit?usp=sharing)
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/72c14602-52f2-4c44-ae39-d01f35337c90)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![Tabla original](docs/screenshots/Cuadro_3_2_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`[Variable 1]`:** *[Descripción]*
   * **`[Variable 2]`:** *[Descripción]*
   * **`[Variable 3]`:** *[Descripción]*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, removing header overlays and total/subtotal rows to avoid double-counting.
   
   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_3_2_tidy_format_table.png)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings.

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring key metrics (KPI scorecards), breakdown charts, and dynamic slicers/filters.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](docs/screenshots/Cuadro_3_2_dashboard.png)
