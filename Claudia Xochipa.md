📊 INEGI National Household Income and Expenditure Survey (ENIGH) 2024. Tables by Federal Entity. 2025.

Table 7.6 – QUARTERLY MONETARY AVERAGE INCOME BY FEDERAL ENTITY OF THE POPULATION THAT CONSIDERS ITSELF AFRO-DESCENDANT OR NOT, ACCORDING TO SEX.

* Authors: [Claudia Xochipa Vazquez]
* Processed Data Source: 🔗 [View Processed Google Sheet](https://docs.google.com/spreadsheets/d/1qVIgIN19VPug9szwohLLFh7YGfEVZxcAS5ZWFuNwciU/edit?usp=sharing).
* Interactive Dashboard: 📊 [View Looker Studio Report](https://datastudio.google.com/reporting/fa32e2ca-a86a-4874-b778-868d1675ac8f).

🛠️ Step-by-Step Data Pipeline & Analytical Process

1. INEGI Source Table Selection:

* Selected the original data table from INEGI's National Household Income and Expenditure Survey (ENIGH) 2024.
* The table provides information about average income by federal entity, Afro-descendant status, and sex.

[Original INEGI Table](docs/screenshots/Cuadro_7_6_Original_Table.jpg).

2. Variable Identification (Dimensions vs. Metrics):

* "Federal Entity" (Entidad Federativa):
  
  * Qualitative (Nominal). Represents the 32 federal entities of Mexico.

* "Afro-descendant Status" (Condición de Afrodescendencia):
  
  * Qualitative (Nominal). Identifies whether individuals consider themselves Afro-descendant or not.

* "Sex" (Sexo):
  
  * Qualitative (Nominal). Classifies the information into men, women, and total men and women.

* "Average Income" (Ingreso Promedio):
  
  * Quantitative. Represents the average income corresponding to each federal entity and demographic category.

3. Tidy Data Transformation:

* Organized the dataset into a structured tabular format, using one row for each combination of federal entity, Afro-descendant status, and sex.
* Standardized the column headings and arranged the information into four main variables: "Federal Entity", "Afro-descendant Status", "Sex", and "Average Income".
* This structure facilitates data filtering, comparison, and visualization in Business Intelligence tools.

Normalized Dataset Preview:

[Tidy Data Screenshot](docs/screenshots/Cuadro_7_6_Tidy_Data.jpg)

4. BI Connection:

* Connected the processed Google Sheets document to Looker Studio as a data source.
* Used the four available variables to organize the information and create interactive visualizations.
* Configured "Average Income" as a numerical metric, allowing income values to be analyzed and compared across different categories.

5. Dashboard Design & Interactive Visuals:

* Developed an interactive dashboard to analyze average income across the federal entities of Mexico.
* The dashboard uses graphical visualizations to compare average income according to Afro-descendant status and sex.
* The available dimensions allow users to explore differences between federal entities and demographic categories.

Final Dashboard Preview:

[Dashboard Screenshot](docs/screenshots/Cuadro_7_6_Dashboard.jpg).
