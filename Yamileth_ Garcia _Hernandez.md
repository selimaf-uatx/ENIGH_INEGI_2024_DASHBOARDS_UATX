## 📊 INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025.

CUADRO 4.4 GASTO CORRIENTE MONETARIO TRIMESTRAL EN ALIMENTOS Y BEBIDAS, POR GRUPOS DE PRODUCTOS ORDENADOS Y TIPO DE NUTRIENTES POR ENTIDAD FEDERATIVA

* **Author:** Yamileth Garcia Hernandez 
* **Processed Data Source:** 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1T0CZA8kbn7BW5JW_H8Qb7Fnwn8N0YXx_9eNoasBK9Wg/edit?usp=sharing) pestaña 4.4 orginial 
* **Interactive Dashboard:** 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/cb408cc9-73d4-4e9b-aef9-c18207e3db85)

---

### 🛠️ Step-by-Step Data Pipeline & Analytical Process

**1. INEGI Source Table Selection:**
* Downloaded raw data table:
  * INEGI. Encuesta Nacional de Ingresos y Gastos de los Hogares. ENIGH 2024. Tabulados por entidad federativa. 2025. Cuadro 4.4 - Gasto corriente monetario trimestral en alimentos y bebidas, por grupos de productos ordenados y tipo de nutrientes por entidad federativa.

**2. Variable Identification (Dimensions vs. Metrics):**
* **State** *(Entidad Federativa)*: Geographic dimension representing the 32 federal entities of Mexico.
* **Expenditure Item / Nutrient Group** *(Objeto del Gasto)*: Categorical dimension classifying food and beverage expenditure by product groups and nutrient types (e.g., *Cereales, Tortillas de maíz, Tubérculos, Aceites y grasas, Azúcar y mieles, Bebidas no alcohólicas, Proteínas de origen vegetal, Proteínas de origen animal, Res y ternera, Puerco, Aves*, etc.).
* **Quarterly Expenditure** *(Gasto - Miles de pesos)*: Quantitative metric representing total quarterly monetary expenditure in thousands of Mexican pesos.
* **Average Quarterly Expenditure** *(Promedio - Pesos)*: Quantitative metric representing the average quarterly household expenditure in Mexican pesos.

**3. Data Cleaning & Tidy Data Transformation (Google Sheets):**
* Restructured the raw INEGI cross-tabulated matrix into a normalized **Tidy Data** format where each column represents a single variable (`estado`, `objeto_gasto`, `gasto_miles_pesos`, `promedio_pesos`) and each row represents a unique observation.
* Removed aggregate summary rows (`NACIONAL`) and cleaned whitespace from numeric values to ensure accurate aggregations in BI tools.

**4. Interactive Dashboard & Visualization (Looker Studio):**
* Connected the processed Google Sheet directly to Looker Studio.
* Built interactive filter controls (State and Expenditure Item / Nutrient Group) alongside KPI scorecards and comparative bar charts to analyze food and nutrient spending patterns across Mexico.
