# 📊 AdventureWorks Sales Analysis (Power BI Beginner Project)
***A Series of a set of 3 Levels to building a beginner Power BI Project - self workings***

This repository contains a beginner-friendly Power BI project that uses the **AdventureWorks+Sales dataset**, simulating a multinational manufacturing company's operations. The project walks through minor end-to-end data preparation, transformation, modeling, and interactive dashboard creation using **Power BI Desktop** and **Power Query Editor**. The repository includes the following key files:

- Adventure Works [Beginner] Problem Statement.docx: This document outlines the project tasks and provides detailed descriptions and guidelines.
- Adventure Works Sales [Beginner].pbix: A PowerBI pbix file containing the implementation of the project tasks, showcasing data analysis, visualization, and manipulation techniques.
- AdventureWorks+Sales.xlsx: The Excel dataset used in this project contains various attributes related to housing data.


---

## 🎯 Project Objective

- Load and explore sales, product, customer, and geography data from Excel.
- Transform raw data using Power Query: clean, split, merge, extract, and aggregate data.
- Build a data model and join relevant tables.
- Visualize insights using interactive visuals and geographical hierarchies.

---

## 🧾 Dataset

- **AdventureWorks+Sales.xlsx** (provided along with this project)
  - Contains tables like Customers, Sales, Products, Date, etc..
  - Load the provided Excel sheet in Power BI.
  - Represents fictional sales data of AdventureWorks Cycles across multiple regions and categories.

---

## 🛠 Tools & Technologies Used

- **Power BI Desktop**
- **Power Query Editor**
- **Excel (.xlsx)**

---

## 🔧 Power Query Data Transformation Steps

1. **Data Load**
   - Load all relevant tables from Excel ending with `_xlsx`.

2. **Column Profiling**
   - Enable: `Column Profile`, `Column Quality`, and `Column Distribution` from the *View* tab in Power Query Editor to check data quality.

3. **Date Breakdown**
   - From the `Date` column, extract:
     - Month Name
     - Month Number
     - Day Name
     - Year  
   *(Use Add Column → Date → desired components, then rename)*

4. **Merge Columns: Category - Subcategory**
   - From the **Product** table, merge `Category` and `Subcategory` with a `-` hyphen separator.
   - Use *Add Column → Merge Columns* to retain the original columns.

5. **Split Customer Names**
   - In the **Customer** table, split full name into First Name and Last Name.
   - Use *Transform → Split Column by Delimiter (space)* and rename resulting columns.

6. **Join and Aggregate Sales by Category**
   - **Join Tables:**
     - Join **Sales** and **Product** tables using `ProductKey`.
     - Recommended Join Type: **Right Outer Join** (ensures all sales retained).
   - **Group & Aggregate:**
     - Group by `Product Category`
     - Aggregate: Sum of `Sales Amount`
   - Rename resulting table to `Category Wise Sales`.

7. **Round Sales Values**
   - Round the `Total Sales` column to appropriate decimals using *Transform → Rounding* options.

8. **Query Diagnostics**
   - Use *Tools → Start Diagnostics → Perform Steps → Stop Diagnostics*.
   - Analyze performance using the generated diagnostics table.

---

## 📊 Data Modeling & Visuals

### 🔗 Hierarchy Created:
`Country-Region` → `State-Province` → `City`

### 📈 Dashboard Elements:
- **Clustered Column Chart** showing total sales by Country/Region.
- Enable **drill-down** to explore data across states and cities.
- Filter out “Not Applicable” sales entries for cleaner visuals.

---

## 💡 Learning Outcomes

By working through this project, you will:
- Understand Power BI's data import and transformation capabilities.
- Practice common data cleaning techniques (splitting, merging, extracting).
- Build and model relationships using joins.
- Use Power Query Diagnostics to optimize transformations.
- Design an interactive dashboard with hierarchical data navigation.

---

## 🧩 Tags

`Power BI` `Data Transformation` `Power Query` `Data Modeling`  
`Dashboard` `Beginner Project` `AdventureWorks` `Sales Analysis`

---

## 👤 Author

**Bidarth Kr. Singh**

---

## 📌 Credits

        This project was created by Bidarth Kr. Singh and is distributed under the "Apache License" license.

---

