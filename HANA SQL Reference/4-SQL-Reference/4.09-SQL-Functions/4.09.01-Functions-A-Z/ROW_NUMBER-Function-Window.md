# 4.9.1.164 ROW_NUMBER Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 301–303

Sequentially numbers the rows within a partition of a result set, with the first row of each partition assigned as 1.

## Syntax

```sql
ROW_NUMBER() <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The output of the ROW_NUMBER function can be non-deterministic among tie values. The ordering of the sequence is determined by the `<windows_order_by_clause>` within the OVER windows clause.

## Examples

The following example returns the sales figures sorted in descending number by product type. The data is partitioned by the product name, and the row number is returned for each type within its product.

```sql
CREATE ROW TABLE ProductSales(ProdName VARCHAR(50), Type VARCHAR(20), Sales INT);
INSERT INTO ProductSales VALUES('Tee Shirt','Plain',21);
INSERT INTO ProductSales VALUES ('Tee Shirt','Lettered',22);
INSERT INTO ProductSales VALUES ('Tee Shirt','Team logo',30);
INSERT INTO ProductSales VALUES('Hoodie','Plain',60);
INSERT INTO ProductSales VALUES ('Hoodie','Lettered',65);
INSERT INTO ProductSales VALUES ('Hoodie','Team logo',80);
INSERT INTO ProductSales VALUES('Ballcap','Plain',8);
INSERT INTO ProductSales VALUES ('Ballcap','Lettered',40);
INSERT INTO ProductSales VALUES ('Ballcap','Team logo',27);
SELECT ProdName, Type, Sales,
  ROW_NUMBER() OVER (PARTITION BY ProdName ORDER BY Sales DESC) AS row_num
FROM ProductSales
ORDER BY ProdName, Sales DESC;
```

| **PRODNAME** | **DESCRIPTION** | **SALES** | **ROW_NUM** |
| --- | --- | --- | --- |
| Ballcap | Lettered | 40 | 1 |
| Ballcap | Team logo | 27 | 2 |
| Ballcap | Plain | 8 | 3 |
| Hoodie | Team logo | 80 | 1 |
| Hoodie | Lettered | 65 | 2 |
| Hoodie | Plain | 60 | 3 |
| Tee Shirt | Team logo | 30 | 1 |
| Tee Shirt | Lettered | 22 | 2 |
| Tee Shirt | Plain | 21 | 3 |

In the following example, the ROW_NUM values for the items are different because there is no `<windows_order_by_clause>` specification:

```sql
SELECT ProdName, Type, Sales,
  ROW_NUMBER() OVER (PARTITION BY ProdName) AS row_num
FROM ProductSales
ORDER BY ProdName, Sales DESC;
```

| **PRODNAME** | **DESCRIPTION** | **SALES** | **ROW_NUM** |
| --- | --- | --- | --- |
| Ballcap | Lettered | 40 | 2 |
| Ballcap | Team logo | 27 | 3 |
| Ballcap | Plain | 8 | 1 |
| Hoodie | Team logo | 80 | 3 |
| Hoodie | Lettered | 65 | 2 |
| Hoodie | Plain | 60 | 1 |
| Tee Shirt | Team logo | 30 | 3 |
| Tee Shirt | Lettered | 22 | 2 |
| Tee Shirt | Plain | 21 | 1 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
