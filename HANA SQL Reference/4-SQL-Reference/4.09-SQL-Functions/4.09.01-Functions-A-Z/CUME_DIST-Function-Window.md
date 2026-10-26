# 4.9.1.49 CUME_DIST Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 159–161

Returns the relative rank of a row.

## Syntax

```sql
CUME_DIST() <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Returns the relative rank of a row.

The relative rank of a row R is defined as NP/NR, where:

- NP is defined to be the number of rows preceding or peer with R in the window ordering of the window partition of R.
- NR is defined to be the number of rows in the window ordering of the window.

## Examples

```sql
CREATE ROW TABLE ProductSales(ProdName VARCHAR(50), Description VARCHAR(20),
Sales INT);
INSERT INTO ProductSales VALUES('Tee Shirt','Plain',21);
INSERT INTO ProductSales VALUES ('Tee Shirt','Lettered',22);
INSERT INTO ProductSales VALUES ('Tee Shirt','Team logo',30);
INSERT INTO ProductSales VALUES('Hoodie','Plain',60);
INSERT INTO ProductSales VALUES ('Hoodie','Lettered',65);
INSERT INTO ProductSales VALUES ('Hoodie','Team logo',80);
INSERT INTO ProductSales VALUES('Ballcap','Plain',8);
INSERT INTO ProductSales VALUES ('Ballcap','Lettered',40);
INSERT INTO ProductSales VALUES ('Ballcap','Team logo',27);
SELECT ProdName, Description, Sales,
  PERCENT_RANK() OVER (ORDER BY Sales ASC) AS Percent_Rank,
  CUME_DIST() OVER (ORDER BY Sales ASC) AS Cume_Dist
FROM ProductSales
ORDER BY Sales DESC;
```

| **PRODNAME** | **DESCRIPTION** | **SALES** | **PERCENT_RANK** | **CUME_DIST** |
| --- | --- | --- | --- | --- |
| Hoodie | Team logo | 80 | 1 | 1 |
| Hoodie | Lettered | 65 | 0.875 | 0.888888888888888 8 |
| Hoodie | Plain | 60 | 0.75 | 0.7777777777777778 |
| Ballcap | Lettered | 40 | 0.625 | 0.666666666666666 6 |
| Tee Shirt | Team logo | 30 | 0.5 | 0.5555555555555556 |
| Ballcap | Team logo | 27 | 0.375 | 0.444444444444444 4 |
| Tee Shirt | Lettered | 22 | 0.25 | 0.3333333333333333 |
| Tee Shirt | Plain | 21 | 0.125 | 0.2222222222222222 |
| Ballcap | Plain | 8 | 0 | 0.1111111111111111 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
