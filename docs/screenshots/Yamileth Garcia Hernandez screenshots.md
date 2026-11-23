## 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025.

CUADRO 1.2 POBLACIÓN TOTAL POR ENTIDAD FEDERATIVA Y GRUPOS DE EDAD SEGÚN SEXO Y TAMAÑO DE LOCALIDAD

* **Author:** Yamileth
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1T0CZA8kbn7BW5JW_H8Qb7Fnwn8N0YXx_9eNoasBK9Wg/edit?usp=sharing)
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/17b68842-8ca6-4bdb-8548-61bca48a478c)

---

### 🛠️ Step-by-Step Data Pipeline & Analytical Process

**1. INEGI Source Table Selection:**
* Downloaded raw data table:
  * INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados de hogares y viviendas. 2025. Cuadro 1.2 - Población total por entidad federativa y grupos de edad según sexo y tamaño de localidad.

**2. Variable Identification (Dimensions vs. Metrics):**
* **State** *(Entidad Federativa)*: Geographic dimension representing the 32 federal entities of Mexico and the national total (NACIONAL).
* **Age Group** *(Grupo de Edad)*: Categorical dimension classifying population age ranges (*0 a 4 años, 5 a 11 años, 12 a 19 años, 20 a 29 años, 30 a 39 años, 40 a 49 años, 50 a 59 años,* and *60 años y más*).
* **Gender** *(Sexo)*: Demographic dimension distinguishing between *Hombre* (Male) and *Mujer* (Female).
* **Locality Size** *(Tamaño de Localidad)*: Categorical dimension classifying settlements by population volume (*Grande* and *Pequeño*).
* **Total Population** *(Población)*: Quantitative metric representing the total number of inhabitants for each unique combination of dimensions.

**3. Data Cleaning & Tidy Data Transformation (Google Sheets):**
* Restructured the raw INEGI cross-tabulated matrix into a normalized **Tidy Data** format where each column represents a single variable (`estado`, `grupo_edad`, `genero`, `tamano_localidad`, `poblacion`) and each row represents a unique observation.
* Standardized numeric formatting and verified data integrity for seamless aggregation.

**Normalized Dataset Preview:**
![Tidy Data Screenshot](yamileth_1_2_tidy.png)

**4. Interactive Dashboard & Visualization (Looker Studio):**
* Connected the processed Google Sheet directly to Looker Studio.
* Built interactive filter controls (State, Age Group, Gender, and Locality Size) alongside KPI scorecards and demographic distribution charts to analyze population structure across Mexico.

**Final Dashboard Preview:**
![Dashboard Screenshot](yamileth_1_2_dashboard.png)
