# VitalPulse-Power-BI-End-to-End-Analytics
End-to-end Power BI project for VitalPulse Sports. From **ERP extraction to dashboards**, aligned with client needs to deliver insights on sales, logistics, products, and customers, supporting **data-driven decisions** and inventory optimization.

### Repository Structure
VitalPulse-BI-Project/

- ***README.md*** --> Main documentation
- **data**/
  - ***ExtraccionERP.xlsb*** --> ERP extract (source dataset)
- **reports**/
  - ***Proyecto final.pdf*** --> Final dashboards (screenshots)
  - ***VitalPulse.pbix*** # Power BI file
- **docs**/
  - ***FullExplanation.pdf*** --> Full technical explanation
- **modelling**/
  - ***Data Modelling.xlsx*** --> Custom Excel to explain the data model created from the ERP file
 
    


### Objectives

- Improve decision-making through sales, **logistics, product, and customer** insights.

- Optimize inventory and logistics based on **demand trends**.

- Focus on key metrics such as **sales performance, margins, delayed/cancelled orders, customer distribution, and top-selling products**.


### Table of Contents of the technical explanation
See the full explanation in [`docs/FullExplanation.pdf`](docs/FullExplanation.pdf)

1. [Requirements Gathering](#1-requirements-gathering)  
2. [Data Extraction & Transformation](#2-data-extraction--transformation)  
3. [Data Modelling](#3-data-modelling)  
4. [DAX Calculations](#4-dax-calculations)  
5. [Dashboard Design](#5-dashboard-design)  
6. [Final Results](#6-final-results)  
7. [How to Use This Project](#7-how-to-use-this-project)

### 1. Requirements Gathering
- Source: ERP export (`ExtraccionERP.xlsb`) with 33 columns in flat format.    
- Key metrics: Sales (MoM/YoY), margin evolution, delayed & cancelled orders, customer segmentation, top-selling products.  
- Objective: Deliver dashboards fully aligned with the client’s decision-making needs.  

### 2. Data Extraction & Transformation
- Imported Excel extract into Power BI.  
- Cleaned and validated fields using Power Query.  
- Corrected data types, removed duplicates/nulls, and fixed anomalies.

### 3. Data Modelling
- Built a **star schema**:
  - Fact tables: `f_nvl_ventas` (sales line level), `f_nvl_pedido` (order level).  
  - Dimension tables: Customers, Orders, Products, Dates.  
- Ensured correct granularity: order vs. sales line.  
- One-to-many relationships from dimensions to facts.
- The star schema design and table relationships are also documented in a dedicated Excel file:  
  [`modelling/Data Modelling.xlsx`](modelling/Data%20Modelling.xlsx)  
  This file includes the mapping of fact and dimension tables, granularity levels, and schema structure used in Power BI.

### 4. DAX Calculations
Created measures to analyze:  
- **Sales KPIs**: monthly totals, MoM & YoY growth, trends.  
- **Margins**: % margin evolution, growth comparisons.  
- **Orders & Logistics**: cancelled, delayed, avg. units/order.  
- **Customers**: number by region, mapping fixes (e.g., Puerto Rico).

### 5. Dashboard Design
Three dashboards were developed:  

1. **Sales**: revenue, units, margins, trends.  
2. **Logistics**: delayed & cancelled orders, delivery performance.  
3. **Products & Customers**: top-selling items, customer distribution, segmentation.

### 6. Final Results
- 📊 [Live Power BI Report](https://app.powerbi.com/view?r=eyJrIjoiOGI4MzllNjQtMWY0Yi00MmM1LWI0NDMtMDUwMmVmODIzMzVhIiwidCI6IjAzYTBmYjY5LWE0ZDAtNDQyZC1hNGQ0LWNmYjVkYTgwNzUwMCJ9)  
- 📄 [PDF Report](reports/Proyecto%20final.pdf)


### 7. How to Use This Project
1. **Clone the repository**: 

   ```bash

   git clone https://github.com/MarioNavarro2810/VitalPulse-BI-Project.git

2. **Open VitalPulse.pbix in Power BI Desktop**.

   File: [reports/Proyecto final.pbix](reports/Proyecto%20final.pbix)

     - Explore the dashboards, visuals, and DAX measures already set up.

3. **Explore the ERP dataset**
   
   File: [data/ExtraccionERP.xlsb](data/ExtraccionERP.xlsb)

     - This is the raw ERP extract in Excel Binary Workbook format (.xlsb), which helps reduce file size compared to .xlsx.

     - You can open it directly in Excel or import it into Power BI.

     - If you prefer .xlsx, simply open the file in Excel and save it as Excel Workbook (.xlsx)*.

4. **Review the data model design**

   File: [modelling/Data Modelling.xlsx](modelling/Data%20Modelling.xlsx)

     - Contains the star schema, fact and dimension tables, and relationship design used in the Power BI report.







