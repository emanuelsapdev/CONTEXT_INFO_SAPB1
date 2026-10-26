# 4.9.1.144 PERCENT_RANK Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 274–276

Calculates the percentage of values that are either less than or greater than the current value, per the ORDER BY specification for the window.

## Syntax

```sql
PERCENT_RANK() <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

For any row in group of rows in a result set, PERCENT_RANK calculates the percentage of values that are either less than or greater than the current value, per the ORDER BY specification for the window.

PERCENT_RANK returns (fractional) integers starting at 0 and ending with 1, as defined by the sort order (ASC or DESC) in the ORDER BY clause.

The relative rank of a row R is defined as (RANK()-1)/(NR-1), where NR is defined to be the number of rows in the window partition of R.

## Examples

In the this example, the rows are partitioned by ProdName, creating a group of rows for each product name. For each row, the PERCENT_RANK column expresses the rank of the sales value for that row as a percentage. Specifically, because ORDER BY (Sales ASC) is specified, PERCENT_RANK returns the percentage of values in the same group that have a lower value.

```sql
CREATE ROW TABLE ProductSales(ProdName VARCHAR(50), Type VARCHAR(20), Sales INT);
INSERT INTO ProductSales VALUES('Tee Shirt','Plain',21);
INSERT INTO ProductSales VALUES('Tee Shirt','Lettered',22);
INSERT INTO ProductSales VALUES('Tee Shirt','Team logo',30);
INSERT INTO ProductSales VALUES('Hoodie','Plain',60);
INSERT INTO ProductSales VALUES('Hoodie','Lettered',65);
INSERT INTO ProductSales VALUES('Hoodie','Team logo',80);
INSERT INTO ProductSales VALUES('Hoodie','Vintage',67);
INSERT INTO ProductSales VALUES('Ballcap','Plain',8);
INSERT INTO ProductSales VALUES('Ballcap','Lettered',40);
INSERT INTO ProductSales VALUES('Ballcap','Team logo',27);
SELECT ProdName, Type, Sales,
  PERCENT_RANK() OVER (PARTITION BY ProdName ORDER BY Sales ASC) AS Percent_Rank
FROM ProductSales
ORDER BY Sales DESC;
```

| **PRODNAME** | **Type** | **SALES** | **PERCENT_RANK** |
| --- | --- | --- | --- |
| Hoodie | Team logo | 80 | 1 |
| Hoodie | Vintage | 67 | 0.6666666666666666 |
| Hoodie | Lettered | 65 | 0.3333333333333333 |
| Hoodie | Plain | 60 | 0 |
| Ballcap | Lettered | 40 | 1 |
| Tee Shirt | Team logo | 30 | 1 |
| Ballcap | Team logo | 27 | 0.5 |
| Tee Shirt | Lettered | 22 | 0.5 |
| Tee Shirt | Plain | 21 | 0 |
| Ballcap | Plain | 8 | 0 |

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) RANK Function (Window) [→](RANK-Function-Window.md)
