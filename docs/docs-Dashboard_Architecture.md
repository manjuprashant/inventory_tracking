# Dashboard Architecture

## Project Architecture Overview

The Inventory Tracking Dashboard follows a structured analytics architecture that transforms raw inventory data into actionable business insights.

---

# Architecture Flow

```text
Inventory Dataset
        │
        ▼
Power Query
(Data Cleaning & Transformation)
        │
        ▼
Data Model
(Relationships & Tables)
        │
        ▼
DAX Layer
(Measures & Calculations)
        │
        ▼
Visualization Layer
(Power BI Dashboard)
        │
        ▼
Business Insights
(Decision Support)
```

---

# Layer 1 – Data Source

Source:
Zepto Inventory Dataset

Contains:

- Product Data
- Inventory Quantity
- Category Details
- Warehouse Information
- Sales Information
- Inventory Dates

---

# Layer 2 – Power Query

Responsibilities:

- Data Cleaning
- Data Validation
- Null Handling
- Data Type Conversion
- Feature Engineering

Output:
Clean analytical dataset.

---

# Layer 3 – Data Model

Core Tables:

### Inventory Table

Contains:
- Product ID
- Product Name
- Category
- Quantity
- Unit Price
- Warehouse

### Date Table

Contains:
- Date
- Month
- Quarter
- Year

Relationships:
Date Table → Inventory Table

---

# Layer 4 – DAX Calculation Layer

Calculates:

- Inventory Value
- Stock Turnover
- Low Inventory Counts
- Average Stock Levels
- KPI Metrics

Purpose:
Generate business-ready calculations.

---

# Layer 5 – Visualization Layer

Dashboard Pages:

### Executive Dashboard
- KPI Cards
- Summary Metrics

### Inventory Analysis
- Category Analysis
- Inventory Distribution

### Warehouse Dashboard
- Warehouse Comparison

### Alert Dashboard
- Low Stock Monitoring

### Trend Dashboard
- Inventory Trend Analysis

---

# Layer 6 – Business Intelligence Layer

Provides:

- Inventory Optimization
- Warehouse Efficiency Analysis
- Replenishment Planning
- Inventory Risk Detection
- Strategic Decision Support

---

# Expected Outcomes

- Improved inventory visibility
- Reduced stockouts
- Better warehouse utilization
- Faster reporting
- Data-driven inventory decisions

---

# Technology Stack

- Power BI Desktop
- Power Query
- DAX
- Microsoft Excel
- Kaggle Dataset

---

# Final Deliverables

- Power BI Dashboard (.pbix)
- Dashboard Documentation
- Business Insights Report
- Project Report
- GitHub Repository
- Dashboard Screenshots