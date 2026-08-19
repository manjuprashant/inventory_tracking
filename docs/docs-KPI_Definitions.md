# KPI Definitions

## Overview

This document defines all Key Performance Indicators used in the Inventory Tracking Dashboard.

---

# Total Inventory Quantity

Definition:
Total quantity of products available in inventory.

Formula:

```DAX
SUM(Inventory[Quantity])
```

Business Value:
Measures available stock.

---

# Total Inventory Value

Definition:
Total monetary value of inventory.

Formula:

```DAX
SUMX(
Inventory,
Inventory[Quantity] * Inventory[Unit Price]
)
```

Business Value:
Measures inventory investment.

---

# Average Stock Level

Definition:
Average inventory quantity per product.

Formula:

```DAX
AVERAGE(Inventory[Quantity])
```

Business Value:
Tracks stock availability.

---

# Stock Turnover

Definition:
Measures how quickly inventory is sold.

Formula:

```DAX
DIVIDE(
[Units Sold],
[Average Stock Level]
)
```

Business Value:
Indicates inventory efficiency.

---

# Low Stock Count

Definition:
Number of products below inventory threshold.

Formula:

```DAX
COUNTROWS()
```

Business Value:
Supports replenishment planning.

---

# Inventory Health Score

Definition:
Overall inventory performance indicator.

Formula:

```DAX
DIVIDE(
[Total Inventory Quantity],
[Total Products]
)
```

Business Value:
Provides inventory quality assessment.

---

# Warehouse Inventory Value

Definition:
Inventory value per warehouse.

Business Value:
Supports warehouse performance evaluation.

---

# Category Inventory Value

Definition:
Inventory value by category.

Business Value:
Identifies high-value categories.