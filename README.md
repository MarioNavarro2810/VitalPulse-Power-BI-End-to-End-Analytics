# VitalPulse-Power-BI-End-to-End-Analytics
End-to-end Power BI project for VitalPulse Sports. From ERP extraction to dashboards, aligned with client needs to deliver insights on sales, logistics, products, and customers, supporting data-driven decisions and inventory optimization.

### Repository Structure
VitalPulse-BI-Project/
│
├── README.md # Main documentation
├── **data**/
│ └── ExtraccionERP.xlsx # ERP extract (source dataset)
├── **reports**/
│ ├── Proyecto final.pdf # Final dashboards (screenshots)
│ └── VitalPulse.pbix # Power BI file
├── **docs**/
  └── VitalPulse.pdf # Full technical explanation


### Objectives

- Improve decision-making through sales, **logistics, product, and customer** insights.

- Optimize inventory and logistics based on **demand trends**.

- Focus on key metrics such as **sales performance, margins, delayed/cancelled orders, customer distribution, and top-selling products**.


### Table of Contents of the technical explanation
See the full explanation in [`docs/VitalPulse.pdf`](docs/VitalPulse.pdf)

1. [Requirements Gathering](#requirements-gathering)  
2. [Data Extraction & Transformation](#data-extraction--transformation)  
3. [Data Modelling](#data-modelling)  
4. [DAX Calculations](#dax-calculations)  
5. [Dashboard Design](#dashboard-design)  
6. [Final Results](#final-results)  
7. [How to Use This Project](#how-to-use-this-project)

### 1. Requirements Gathering
- Source: ERP export (`ExtraccionERP.xlsx`) with 33 columns in flat format.    
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

### 4. DAX Calculations
Created measures to analyze:  
- **Sales KPIs**: monthly totals, MoM & YoY growth, trends.  
- **Margins**: % margin evolution, growth comparisons.  
- **Orders & Logistics**: cancelled, delayed, avg. units/order.  
- **Customers**: number by region, mapping fixes (e.g., Puerto Rico).   

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
- 📄 [PDF Report](docs/VitalPulse.pdf) 

### 7. How to Use This Project
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/VitalPulse-BI-Project.git

2. Open VitalPulse.pbix in Power BI Desktop.

3. Explore the model, DAX measures, and dashboards.

4. Use data/ExtraccionERP.xlsx to refresh the dataset.








