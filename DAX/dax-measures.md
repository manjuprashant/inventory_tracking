# DAX Measures Documentation

## Overview

This document contains all DAX measures used in the Inventory Tracking Dashboard.

---

# Total Inventory Quantity

```DAX
Total Inventory Quantity =
SUM(Inventory[Quantity])
```

Purpose:
Calculates total inventory available across all products and warehouses.

---

# Total Inventory Value

```DAX
Total Inventory Value =
SUMX(
    Inventory,
    Inventory[Quantity] * Inventory[Unit Price]
)
```

Purpose:
Calculates the total monetary value of inventory.

---

# Average Stock Level

```DAX
Average Stock Level =
AVERAGE(Inventory[Quantity])
```

Purpose:
Calculates average inventory quantity per product.

---

# Total Products

```DAX
Total Products =
DISTINCTCOUNT(Inventory[Product ID])
```

Purpose:
Counts unique products in inventory.

---

# Total Categories

```DAX
Total Categories =
DISTINCTCOUNT(Inventory[Category])
```

Purpose:
Counts unique product categories.

---

# Total Warehouses

```DAX
Total Warehouses =
DISTINCTCOUNT(Inventory[Warehouse])
```

Purpose:
Counts warehouses available in dataset.

---

# Units Sold

```DAX
Units Sold =
SUM(Inventory[Units Sold])
```

Purpose:
Calculates total quantity sold.

---

# Stock Turnover

```DAX
Stock Turnover =
DIVIDE(
    [Units Sold],
    [Average Stock Level]
)
```

Purpose:
Measures inventory movement efficiency.

---

# Low Stock Count

```DAX
Low Stock Count =
CALCULATE(
    COUNTROWS(Inventory),
    Inventory[Quantity] < 50
)
```

Purpose:
Counts products with inventory below threshold.

---

# Inventory Value by Category

```DAX
Inventory Value by Category =
SUMX(
    Inventory,
    Inventory[Quantity] * Inventory[Unit Price]
)
```

Purpose:
Used in category-wise inventory value analysis.

---

# Inventory Value per Warehouse

```DAX
Inventory Value per Warehouse =
SUMX(
    Inventory,
    Inventory[Quantity] * Inventory[Unit Price]
)
```

Purpose:
Measures inventory value by warehouse.

---

# Monthly Inventory Trend

```DAX
Monthly Inventory Trend =
SUM(Inventory[Quantity])
```

Purpose:
Tracks inventory movement over time.

---

# Inventory Health Score

```DAX
Inventory Health Score =
DIVIDE(
    [Total Inventory Quantity],
    [Total Products]
)
```

Purpose:
Provides an overall inventory health indicator.

---

# Reorder Recommendation Count

```DAX
Reorder Recommendation Count =
CALCULATE(
    COUNTROWS(Inventory),
    Inventory[Quantity] < 50
)
```

Purpose:
Identifies products requiring replenishment.