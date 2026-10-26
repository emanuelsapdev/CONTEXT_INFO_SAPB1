# 4.9.1.71 DENSE_RANK Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 178–179

Performs the same ranking operation as the RANK function, except that rank numbering does not skip when ties are found.

## Syntax

```sql
DENSE_RANK() <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The DENSE_RANK function performs the same ranking operation as the RANK function, except that rank numbering does not skip when ties are found.

## Examples

In this example, the RANK function returns the rank 5 for the row `('A', 10, 0)` because there were two rows that returned the rank of 3. However, DENSE_RANK returns the rank 4 for the row `('A', 10, 0)`.

```sql
CREATE ROW TABLE T (class CHAR(10), val INT, offset INT);
 INSERT INTO T VALUES('A', 1, 1);
 INSERT INTO T VALUES('A', 3, 3);
 INSERT INTO T VALUES('A', 5, null);
 INSERT INTO T VALUES('A', 5, 2);
 INSERT INTO T VALUES('A', 10, 0);
 INSERT INTO T VALUES('B', 1, 3);
 INSERT INTO T VALUES('B', 1, 1);
 INSERT INTO T VALUES('B', 7, 1);
SELECT class,
  val,
  ROW_NUMBER() OVER (PARTITION BY class ORDER BY val) AS row_num,
  RANK() OVER (PARTITION BY class ORDER BY val) AS rank,
  DENSE_RANK() OVER (PARTITION BY class ORDER BY val) AS dense_rank
 FROM T;
```

| **CLASS** | **VAL** | **ROW_NUM** | **RANK** | **DENSE_RANK** |
| --- | --- | --- | --- | --- |
| A | 1 | 1 | 1 | 1 |
| A | 3 | 2 | 2 | 2 |
| A | 5 | 3 | 3 | 3 |
| A | 5 | 4 | 3 | 3 |
| A | 10 | 5 | 5 | 4 |
| B | 1 | 1 | 1 | 1 |
| B | 1 | 2 | 1 | 1 |
| B | 7 | 3 | 3 | 2 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
