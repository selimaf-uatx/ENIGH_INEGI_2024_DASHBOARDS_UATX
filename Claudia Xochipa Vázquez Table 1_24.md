📊 INEGI. National Household Income and Expenditure Survey. ENIGH 2024. Tables by Federal Entity. 2025.

Table 1.24 – OWNER-OCCUPIED DWELLINGS BY FEDERAL ENTITY, ACCORDING TO ACQUISITION METHOD

- Authors: [Claudia Xochipa Vázquez]
- Processed Data Source: 🔗 "View Processed Google Sheet" (INSERT_YOUR_GOOGLE_SHEETS_LINK)
- Interactive Dashboard: 📊 "View Looker Studio Report" (INSERT_YOUR_LOOKER_STUDIO_LINK)

---

🛠️ Step-by-Step Data Pipeline & Analytical Process

1. INEGI Source Table Selection:

- Downloaded raw data table:

"INEGI Table 1.24 – Owner-Occupied Dwellings by Federal Entity, According to Acquisition Method" (docs/screenshots/Cuadro_1_24_Viviendas_propias_por_adquisicion_original_table.jpg)

2. Variable Identification (Dimensions vs. Metrics):

- "Federal Entity" (Entidad Federativa):
  Geographic dimension representing the 32 federal entities of Mexico.

- "Acquisition Method" (Forma de Adquisición):
  Categorical variable identifying how owner-occupied dwellings were acquired, including four categories: purchased already built, commissioned construction, self-built by the owner or family members, and acquired in another way.

- "Absolute Dwellings" (Viviendas Absolutas):
  Numerical metric representing the number of owner-occupied dwellings for each federal entity and acquisition method.

- "Relative Dwellings" (Viviendas Relativas):
  Numerical metric representing the percentage of owner-occupied dwellings corresponding to each acquisition method within each federal entity.

3. Tidy Data Transformation:

- Reshaped and unpivoted the original matrix table into a normalized flat structure (Tidy Data) in Google Sheets. The original acquisition method categories and their absolute and relative values were reorganized into four columns: "Federal Entity", "Acquisition Method", "Absolute Dwellings", and "Relative Dwellings".

Normalized Dataset Preview:

"Tidy Data Screenshot" (docs/screenshots/Cuadro_1_24_Viviendas_propias_por_adquisicion_tidy_format_table.jpg)

4. BI Connection:

- Connected the processed Google Sheet directly to Looker Studio as a data source, configuring "Federal Entity" and "Acquisition Method" as dimensions, and "Absolute Dwellings" and "Relative Dwellings" as metrics. The numerical fields were configured with appropriate aggregation settings to support comparisons between federal entities and acquisition methods.

5. Dashboard Design & Interactive Visuals:

- Built an interactive dashboard featuring a main KPI scorecard displaying the total number of absolute dwellings, a pie chart showing the percentage distribution of owner-occupied dwellings according to acquisition method, and a horizontal bar chart comparing the total number of dwellings across the different acquisition categories.

- Also included a stacked horizontal bar chart comparing owner-occupied dwellings by federal entity and acquisition method, as well as a bar chart ranking federal entities according to their total number of owner-occupied dwellings, from highest to lowest.

- The dashboard includes dynamic filters for "Acquisition Method" and "Federal Entity", allowing users to explore specific categories and compare the results across Mexico.

Final Dashboard Preview:

"Dashboard Screenshot" (docs/screenshots/Cuadro_1_24_Viviendas_propias_por_adquisicion_dashboard.jpg)
