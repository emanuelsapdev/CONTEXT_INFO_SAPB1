# 4.9.1.108 LEAD Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 230–231

Returns the offset of rows after the current row. The `<offset>` should be non-negative and its default is 1.

## Syntax

```sql
LEAD( <expression> [, <offset> [, <default_expr> ] ] ) <window_specification>
```

## Syntax Elements

#### offset

If the `<offset>` crosses boundaries of the partition, then the `<default_expr>` value is returned. If the `<default_expr>` is not specified, then a null value is returned. The `<offset>` and `<default_expr>` are evaluated at current row.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The output of the LEAD function can be non-deterministic among tie values.

## Examples

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
  offset,
  LEAD(val) OVER (PARTITION BY class ORDER BY val) AS lead,
  LEAD(val, offset, -val) OVER (PARTITION BY class ORDER BY val) AS lead2,
  LAG(val) OVER (PARTITION BY class ORDER BY val) AS lag,
  LAG(val, offset, -val) OVER (PARTITION BY class ORDER BY val) AS lag2
 FROM T;
```

| **CLASS** | **VAL** | **OFFSET** | **LEAD** | **LEAD2** | **LAG** | **LAG2** |
| --- | --- | --- | --- | --- | --- | --- |
| A | 1 | 1 | 3 | 3 | null | -1 |
| A | 3 | 3 | 5 | 10 | 1 | -3 |
| A | 5 | null | 5 | -5 | 3 | -5 |
| A | 5 | 2 | 10 | -5 | 5 | 3 |
| A | 10 | 0 | null | 10 | 5 | 10 |
| B | 1 | 3 | 1 | -1 | null | -1 |
| B | 1 | 1 | 7 | 7 | 1 | 1 |
| B | 7 | 1 | null | -7 | 1 | 1 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
