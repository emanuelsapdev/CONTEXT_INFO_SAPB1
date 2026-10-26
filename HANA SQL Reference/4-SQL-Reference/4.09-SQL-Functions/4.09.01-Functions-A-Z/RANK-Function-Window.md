# 4.9.1.153 RANK Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 287–288

Returns rank of a row within a partition, starting from 1.

## Syntax

```sql
RANK() <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The RANK function returns duplicate values in the ranking sequence when there are ties between values and the next rankings are skipped.

## Examples

In this example, the data is partitioned by the product name, and the sales of types within the products are ranked. The plain ballcap is ranked 4 instead of 3 because of the sales numbers for the team logo and lettered versions of the ballcap, which are tied at rank 2.

```sql
CREATE ROW TABLE ProductSales(ProdName VARCHAR(50), Type VARCHAR(20), Sales INT);
INSERT INTO ProductSales VALUES('Tee Shirt','Plain',21);
INSERT INTO ProductSales VALUES('Tee Shirt','Lettered',22);
INSERT INTO ProductSales VALUES('Tee Shirt','Team logo',30);
INSERT INTO ProductSales VALUES('Hoodie','Plain',60);
INSERT INTO ProductSales VALUES('Hoodie','Lettered',65);
INSERT INTO ProductSales VALUES('Hoodie','Team logo',80);
INSERT INTO ProductSales VALUES('Ballcap','Vintage',60);
INSERT INTO ProductSales VALUES('Ballcap','Plain',8);
INSERT INTO ProductSales VALUES('Ballcap','Lettered',40);
INSERT INTO ProductSales VALUES('Ballcap','Team logo',40);
SELECT ProdName, Type, Sales,
RANK() OVER ( PARTITION BY ProdName ORDER BY Sales DESC ) AS Rank
FROM ProductSales
ORDER BY ProdName, Type;
```

| **PRODNAME** | **Type** | **SALES** | **RANK** |
| --- | --- | --- | --- |
| Ballcap | Lettered | 40 | 2 |
| Ballcap | Plain | 8 | 4 |
| Ballcap | Team logo | 40 | 2 |
| Ballcap | Vintage | 60 | 1 |
| Hoodie | Lettered | 65 | 2 |
| Hoodie | Plain | 60 | 3 |
| Hoodie | Team logo | 80 | 1 |
| Tee Shirt | Lettered | 22 | 2 |
| Tee Shirt | Plain | 21 | 3 |
| Tee Shirt | Team logo | 30 | 1 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
