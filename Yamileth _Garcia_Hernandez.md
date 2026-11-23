## 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.

CUADRO 4.2A GASTO CORRIENTE MONETARIO PROMEDIO TRIMESTRAL POR LA COMPOSICIÓN DE LOS GRANDES RUBROS DEL GASTO Y ENTIDAD FEDERATIVA SEGÚN DECILES DE HOGARES DE ACUERDO CON SU INGRESO CORRIENTE TOTAL TRIMESTRAL

* **Author:** Yamileth Garcia Hernández 
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1T0CZA8kbn7BW5JW_H8Qb7Fnwn8N0YXx_9eNoasBK9Wg/edit?usp=sharing) tabla 2.4A
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/cd8ce752-b8e1-42de-9e59-50e65faaab0a)

---

### 🛠️ Step-by-Step Data Pipeline & Analytical Process

**1. INEGI Source Table Selection:**
* Downloaded raw data table:
  * INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 4.2A - Gasto corriente monetario promedio trimestral por la composición de los grandes rubros del gasto y entidad federativa según deciles de hogares de acuerdo con su ingreso corriente total trimestral.

**2. Variable Identification (Dimensions vs. Metrics):**
* **State** *(Entidad Federativa)*: Geographic dimension representing the 32 federal entities of Mexico.
* **Major Expenditure Category** *(Grandes Rubros del Gasto)*: Categorical dimension classifying household spending into major groups (*Alimentos, bebidas y tabaco; Vestido y calzado; Vivienda y energía; Limpieza y enseres domésticos; Cuidados de la salud; Transporte y comunicaciones; Educación y esparcimiento; Cuidados personales*).
* **Household Income Decile** *(Deciles de Hogares)*: Socioeconomic dimension segmenting households into ten income deciles (**I** through **X**) based on total quarterly current income.
* **Average Quarterly Monetary Expenditure** *(Gasto Corriente Monetario Promedio Trimestral)*: Quantitative metric representing the average quarterly household expenditure in Mexican pesos.

**3. Data Cleaning & Tidy Data Transformation (Google Sheets):**
* Unpivoted the wide decile columns (`I` to `X`) and restructured the raw INEGI cross-tabulated matrix into a normalized **Tidy Data** format where each column represents a single variable (`estado`, `rubro_gasto`, `decil_hogar`, `gasto_promedio_trimestral`) and each row represents a unique observation.
* Excluded aggregate summary rows (`NACIONAL`) and total columns (`TOTAL`) to prevent double-counting in BI aggregations.

**4. Interactive Dashboard & Visualization (Looker Studio):**
* Connected the processed Google Sheet directly to Looker Studio.
* Built interactive filter controls (State, Expenditure Category, and Income Decile) alongside KPI scorecards and distribution charts to analyze consumption inequality and spending composition across income deciles in Mexico.
