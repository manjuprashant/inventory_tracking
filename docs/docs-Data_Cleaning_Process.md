# Data Cleaning Process

## Objective

Prepare inventory data for accurate analysis and dashboard reporting.

---

## Data Import

- Imported Zepto Inventory Dataset into Power BI.
- Verified row and column counts.

---

## Data Quality Checks

### Missing Values

- Identified null records.
- Replaced missing values where applicable.
- Removed invalid records.

### Duplicate Records

- Checked duplicate Product IDs.
- Removed duplicate entries.

### Data Type Validation

Corrected:

- Product ID → Text
- Product Name → Text
- Category → Text
- Warehouse → Text
- Quantity → Whole Number
- Unit Price → Decimal Number
- Date → Date

---

## Data Transformation

### Created Inventory Value

Inventory Value = Quantity × Unit Price

### Created Inventory Status

- Critical
- Low
- Normal
- High

### Created Reorder Flags

Used for low-stock monitoring.

---

## Validation

- Verified totals.
- Validated category counts.
- Checked warehouse distribution.
- Confirmed KPI accuracy.

---

## Outcome

The cleaned dataset was optimized for Power BI reporting and inventory analysis.