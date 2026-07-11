---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["database", "schema", "postgres"]
domain: "Projects/POS"
---

# Summary
Database schema for transactions, inventories, users, and stock records.

# Key Concepts
- **Normalization**: 3NF validation to prevent transaction inconsistencies.
- **Tables**:
  - `products`: id, SKU, name, price, stock, category_id.
  - `sales`: id, timestamp, total, cashier_id.
  - `sale_items`: sale_id, product_id, quantity, unit_price.

# Examples
```sql
-- Transaction write query enforcing atomic stock reduction
BEGIN;
INSERT INTO sales (total, cashier_id) VALUES (450.00, 1) RETURNING id;
INSERT INTO sale_items (sale_id, product_id, quantity, unit_price) VALUES (currval('sales_id_seq'), 102, 2, 225.00);
UPDATE products SET stock = stock - 2 WHERE id = 102;
COMMIT;
```
