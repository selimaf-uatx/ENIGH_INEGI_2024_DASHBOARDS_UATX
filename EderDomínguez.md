# Data Transformation & Looker Studio Reporting

This repository documents the workflow used to transform raw statistical data into a **Tidy Data** format using Google Sheets and build an interactive dashboard in Looker Studio.

---

## 1. Project Links

* **Google Sheets (Tidy Dataset):** [View Google Sheet](https://docs.google.com/spreadsheets/d/192-LTrh42RoR05OypWeA4lgS2GKCrqob/edit?usp=sharing&ouid=115402438294849232229&rtpof=true&sd=true)
* **Looker Studio (Interactive Dashboard):** [View Interactive Report](https://datastudio.google.com/s/lHQB1TeMwmg)

---

## 2. Original Data Source

* **Institution / Source:** INEGI - ENIGH 2024
* **Specific Table:** Table 1.3

---

## 3. Workflow & Methodology

1. **Locate the Original Data Table:** Retrieve the raw statistical table from the official institutional source.
2. **Identify Dimensions and Metrics:** Separate categorical attributes from quantitative measurements to define the analytical schema.
3. **Generate the Tidy Table in Google Sheets:** Restructure the raw table so that each variable forms a column, each observation forms a row, and each type of observational unit forms a table.
4. **Connect Data to Looker Studio:** Link the clean Google Sheets dataset as a data source in Looker Studio to initialize the report.
5. **Configure Visuals, Filters, and Descriptions:** Design the dashboard layout by adding interactive controls, charts, scorecards, and explanatory text blocks.

---

## 4. Tidy Table Structure

* **Dimensions:** Federal Entity, Locality Size, Households
* **Metrics:** Estimated Value / Average

---

## 5. Looker Studio Dashboard Elements

* **Header & Title:** Clear dashboard title and contextual overview of the dataset.
* **Data Visualizations:** Bar charts, comparison tables, and KPI scorecards displaying key metrics across dimensions.
* **Interactive Filters:** Drop-down controls allowing users to filter results dynamically by specific dimensions.
* **Descriptions:** Explanatory text boxes providing methodology notes, data definitions, and key takeaways.
