### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.
Cuadro 4.7 - PORCENTAJE DE GASTO CORRIENTE MONETARIO TRIMESTRAL POR HOGAR POR GRANDES RUBROS DE GASTO Y SEXO DE LA JEFATURA DEL HOGAR
* **Authors:** Bernardo X / 
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1mclWeuUBgTvCGgv-KTS2cxDe1hOBaOcp6qmjqI3GjM4/edit?usp=drivesdk)
* **Interactive Dashboard:** 📊 [View Looker Studio Report](AQUI TU LINK DE LOOKER STUDIO)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
   * Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.
Cuadro 4.7 - PORCENTAJE DE GASTO CORRIENTE MONETARIO TRIMESTRAL POR HOGAR POR GRANDES RUBROS DE GASTO Y SEXO DE LA JEFATURA DEL HOGAR.
](docs/screenshots/Cuadro_4_7_Gasto_por_rubros_y_sexo_jefatura_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
   * **`Rubro de Gasto` (*Grandes Rubros de Gasto*):**
     *Categorical classification of household expenditure (Alimentos, bebidas y tabaco; Vestido y calzado; Vivienda, servicios de conservación, energía eléctrica y combustibles; Artículos y servicios para la limpieza, cuidados de la casa, enseres domésticos y muebles; Cuidados de la salud; Transporte, adquisición, mantenimiento, accesorios y servicios para vehículos; Comunicaciones; Cuidados personales, accesorios y efectos personales y otros gastos diversos; Servicios de educación, artículos educativos, artículos de esparcimiento y otros gastos de esparcimiento; Transferencias de gasto).*

   * **`Sexo de la Jefatura del Hogar` (*Sexo del Jefe del Hogar*):**
     *Demographic dimension separating households into three groups: Hogares Totales, Hogares con Jefatura Femenina and Hogares con Jefatura Masculina.*

   * **`Porcentaje de Gasto` (*Porcentaje de Gasto Corriente Monetario Trimestral* - Metric):**
     *The unique numerical field expressing the relative distribution of current monetary expenditure per household, expressed in percentages.*

3. **Tidy Data Transformation:**
   * Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, removing header overlays, definition rows and total/subtotal rows to avoid double-counting.
   
   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_4_7_Gasto_por_rubros_y_sexo_jefatura_tidy_format_table.png)

4. **BI Connection:**
   * Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings (ensuring `Porcentaje de Gasto` is set to `SUM`).

5. **Dashboard Design & Interactive Visuals:**
   * Built an interactive dashboard featuring key metrics (KPI scorecards), breakdown charts, and dynamic slicers/filters for `Rubro de Gasto` and `Sexo de la Jefatura del Hogar`.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](docs/screenshots/Cuadro_4_7_Gasto_por_rubros_y_sexo_jefatura_dashboard.png)
