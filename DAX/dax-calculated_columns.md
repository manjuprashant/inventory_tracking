# Calculated Columns Documentation

## Overview

This document contains calculated columns used within the Inventory Tracking Dashboard.

---

# Inventory Value

```DAX
Inventory Value =
Inventory[Quantity] * Inventory[Unit Price]
```

Purpose:
Calculates value of inventory for each product.

---

# Low Inventory Flag

```DAX
Low Inventory Flag =
IF(
    Inventory[Quantity] < 50,
    "Low Stock",
    "Available"
)
```

Purpose:
Identifies low-stock products.

---

# Inventory Status

```DAX
Inventory Status =
SWITCH(
    TRUE(),
    Inventory[Quantity] < 20, "Critical",
    Inventory[Quantity] < 50, "Low",
    Inventory[Quantity] < 200, "Normal",
    "High"
)
```

Purpose:
Classifies inventory levels.

---

# Warehouse Category

```DAX
Warehouse Category =
IF(
    Inventory[Quantity] > 500,
    "High Volume",
    "Standard"
)
```

Purpose:
Classifies warehouse inventory capacity.

---

# Stock Value Category

```DAX
Stock Value Category =
IF(
    Inventory[Inventory Value] > 10000,
    "High Value",
    "Regular Value"
)
```

Purpose:
Groups products by inventory value.

---

# Inventory Age Group

```DAX
Inventory Age Group =
SWITCH(
    TRUE(),
    Inventory[Days In Stock] <= 30, "0-30 Days",
    Inventory[Days In Stock] <= 60, "31-60 Days",
    Inventory[Days In Stock] <= 90, "61-90 Days",
    "90+ Days"
)
```

Purpose:
Categorizes inventory age.

---

# Reorder Required

```DAX
Reorder Required =
IF(
    Inventory[Quantity] < 50,
    "Yes",
    "No"
)
```

Purpose:
Flags products needing replenishment.

---

# Product Performance

```DAX
Product Performance =
IF(
    Inventory[Units Sold] > 100,
    "Fast Moving",
    "Slow Moving"
)
```

Purpose:
Classifies product sales performance.