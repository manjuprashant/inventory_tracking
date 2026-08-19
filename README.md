# Inventory Tracking Dashboard

A comprehensive Power BI dashboard for monitoring inventory performance, stock levels, warehouse operations, and inventory health using the Zepto Inventory Dataset.

## Project Overview

This project provides an end-to-end inventory analytics solution that helps businesses:

* Monitor inventory levels across warehouses
* Track stock turnover performance
* Identify low-stock and overstock situations
* Analyze inventory trends over time
* Compare warehouse performance
* Generate actionable business insights

The dashboard enables inventory managers and business stakeholders to make data-driven decisions for inventory optimization and supply chain efficiency.

---

## Dataset

**Source:** Zepto Inventory Dataset (Kaggle)

Dataset Link:
https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset

### Dataset Attributes

* Product ID
* Product Name
* Category
* Warehouse
* Quantity
* Unit Price
* Inventory Date
* Units Sold
* Stock Status

---

## Project Objectives

* Analyze inventory availability
* Calculate stock turnover metrics
* Monitor low inventory products
* Compare warehouse inventory performance
* Track inventory movement trends
* Create executive-level KPI reporting
* Provide inventory optimization insights

---

## Tools & Technologies

* Power BI Desktop
* Power Query
* DAX
* Microsoft Excel
* Kaggle Dataset

---

## Data Preparation

The following data preparation steps were performed:

1. Imported inventory dataset into Power BI
2. Removed duplicate records
3. Handled missing values
4. Standardized data formats
5. Corrected column data types
6. Created calculated columns
7. Built DAX measures for KPIs

---

## Key Performance Indicators (KPIs)

### Total Inventory Value

```DAX
Total Inventory Value =
SUMX(
    Inventory,
    Inventory[Quantity] * Inventory[Unit Price]
)
```

### Average Stock Level

```DAX
Average Stock =
AVERAGE(Inventory[Quantity])
```

### Stock Turnover

```DAX
Stock Turnover =
DIVIDE(
    SUM(Inventory[Units Sold]),
    AVERAGE(Inventory[Quantity])
)
```

### Low Inventory Flag

```DAX
Low Inventory Flag =
IF(
    Inventory[Quantity] < 50,
    "Low Stock",
    "Available"
)
```

---

## Dashboard Features

### Executive Summary

* Total Inventory Value
* Total Products
* Average Stock Level
* Stock Turnover KPI
* Inventory Health Overview

### Inventory Analysis

* Stock by Category
* Category-wise Inventory Distribution
* Inventory Value Analysis

### Warehouse Comparison

* Inventory by Warehouse
* Warehouse Performance Analysis
* Inventory Allocation Insights

### Trend Analysis

* Inventory Trends Over Time
* Stock Movement Monitoring
* Historical Inventory Tracking

### Alert Dashboard

* Low Inventory Products
* Critical Stock Alerts
* Inventory Risk Monitoring

---

## Dashboard Screenshots

### Dashboard Overview

![Dashboard Overview](screenshots/dashboard-overview.png)

### Stock Turnover Analysis

![Stock Turnover](screenshots/stock-turnover.png)

### Warehouse Comparison

![Warehouse Comparison](screenshots/warehouse-comparison.png)

### Low Stock Alerts

![Low Stock Alerts](screenshots/low-stock-alerts.png)

### Inventory Trends

![Inventory Trends](screenshots/trend-analysis.png)

---

## Business Insights

### Inventory Health

* High-performing categories maintain healthy stock levels.
* Certain products require immediate replenishment.

### Warehouse Analysis

* Inventory distribution varies significantly across warehouses.
* Inventory balancing opportunities exist.

### Stock Turnover

* Fast-moving products contribute significantly to sales.
* Slow-moving products may increase holding costs.

### Risk Monitoring

* Low-stock products can lead to stockouts if not replenished promptly.
* Alert mechanisms support proactive inventory management.

---

## Project Structure

```text
inventory_tracking/
│
├── README.md
├── Inventory_Tracking_Report.pdf
├── Dashboard_Documentation.pdf
├── Business_Insights.pdf
├── Inventory_Tracking.pbix
│
├── dataset/
│   └── zepto_inventory_dataset.csv
│
├── screenshots/
│   ├── dashboard-overview.png
│   ├── stock-turnover.png
│   ├── warehouse-comparison.png
│   ├── low-stock-alerts.png
│   └── trend-analysis.png
│
└── docs/
    ├── KPI_Definitions.md
    ├── Data_Cleaning_Process.md
    └── Dashboard_Architecture.md
```

---

## Key Business Recommendations

* Implement automated reorder thresholds.
* Monitor low-stock products regularly.
* Balance inventory across warehouses.
* Reduce excess inventory for slow-moving products.
* Improve demand forecasting accuracy.

---

## Expected Benefits

* Improved inventory visibility
* Reduced stockout risk
* Better warehouse utilization
* Lower inventory holding costs
* Faster business decision-making

---

## Author

**Manjula Srinivasan**

Data Analytics Intern – Infotact Solutions

2026

---

## License

This project is developed for educational, portfolio, and business analytics demonstration purposes.
