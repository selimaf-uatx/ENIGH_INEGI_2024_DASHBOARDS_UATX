
### 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.
Cuadro 1.3 - HOGARES, TOTAL DE INTEGRANTES DEL HOGAR, EDAD DEL JEFE, INTEGRANTES DEL HOGAR DE 15 A 64 AÑOS, DE 65 Y MÁS AÑOS, ECONÓMICAMENTE ACTIVOS, NO ECONÓMICAMENTE ACTIVOS, PERCEPTORES POR HOGAR E INTEGRANTES OCUPADOS POR ENTIDAD FEDERATIVA Y TAMAÑO DE LOCALIDAD
- **Authors:** Israel Ochoa Ordoñez
- **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1j9JcLNK94cttNesWORkAACQC5XBmXSoL_z58_eG2IVg/edit?usp=sharing)
- **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/3ca4486e-3338-4b7c-8314-9aa35487026c)

#### 🛠️ Step-by-Step Data Pipeline & Analytical Process

1. **INEGI Source Table Selection:**
  - Downloaded raw data table: ![INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 1.3 - Hogares e indicadores sociodemográficos por entidad federativa y tamaño de localidad.](docs/screenshots/Cuadro_1_3_original_table.png)

2. **Variable Identification (Dimensions vs. Metrics):**
- **`State` (*Entidad Federativa*):**
     *Geographic dimension representing the 32 federal entities/states of Mexico.*

- **`Locality Size` (*Tamaño de Localidad*):**
     *Geographic classification separating urban areas (≥ 2,500 inhabitants) from rural areas (< 2,500 inhabitants).*

- **`Households` (*Hogares*):**
     *Demographic dimension representing the total number of households.*

- **`Total Household Members` (*Total de integrantes del hogar*):**
     *Demographic dimension counting all individuals residing in the household.*

- **`Age of Household Head` (*Edad del jefe*):**
     *Demographic dimension categorizing households by the age bracket of the household head.*

- **`Household Members Aged 15 to 64` (*Integrantes del hogar de 15 a 64 años*):**
     *Demographic dimension representing the working-age population segment within the household.*

- **`Household Members Aged 65 and Over` (*Integrantes del hogar de 65 y más años*):**
     *Demographic dimension representing the senior population segment within the household.*

- **`Economically Active Household Members Aged 15 and Over` (*Integrantes del hogar de 15 y más años económicamente activos*):**
     *Economic dimension measuring household members aged 15+ participating in the labor force.*

- **`Non-Economically Active Household Members Aged 15 and Over` (*Integrantes del hogar de 15 y más años no económicamente activos*):**
     *Economic dimension measuring household members aged 15+ outside the labor force.*

- **`Income Recipients per Household` (*Perceptores por hogar*):**
     *Economic dimension indicating the number of household members earning income.*

- **`Employed Household Members` (*Integrantes del hogar ocupados*):**
     *Economic dimension representing household members currently employed.*

- **`Estimated Value / Average` (*Valor / promedio estimado* - Metric):**
     *The unique numerical field representing the estimated value or average for each demographic and economic indicator.*

3. **Tidy Data Transformation:**
- Reshaped and unpivoted the original matrix table into a normalized flat structure (*Tidy Data*) in Google Sheets, removing header overlays and total/subtotal rows to avoid double-counting.
   
   ##### Normalized Dataset Preview:
   ![Tidy Data Screenshot](docs/screenshots/Cuadro_1_3_tidy_format_table.png)

4. **BI Connection:**
- Connected the processed Google Sheet directly to Looker Studio as a live data source, validating metric aggregation settings (ensuring `Estimated Value / Average` is properly configured).

5. **Dashboard Design & Interactive Visuals:**
- Built an interactive dashboard featuring key metrics (KPI scorecards), breakdown charts, explanatory descriptions, and dynamic slicers/filters for `State` and `Locality Size`.

   ##### Final Dashboard Preview:
   ![Dashboard Screenshot](docs/screenshots/Cuadro_1_3_dashboard.png)
