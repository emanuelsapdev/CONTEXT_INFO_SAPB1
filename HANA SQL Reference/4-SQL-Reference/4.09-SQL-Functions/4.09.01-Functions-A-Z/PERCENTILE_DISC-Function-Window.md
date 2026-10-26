# 4.9.1.146 PERCENTILE_DISC Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 278–280

Returns the first value whose cumulative distribution value is greater than or equal to the percentile value of a constant.

## Syntax

```sql
PERCENTILE_DISC( <constant_literal> ) WITHIN GROUP ( ORDER BY <expression> [ ASC
| DESC ] [ NULLS FIRST | NULLS LAST ] ) <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Returns the first value whose cumulative distribution value is greater than or equal to the percentile value of `<constant_literal>`.

A discrete distribution of the values of `<expression>` is assumed. Only a single `<expression>` can be specified in ORDER BY clause; this expression must evaluate to a numeric type. The `<constant_literal>` should be a numeric value between, and including, 0 to 1, because it is a percentile value. The return value is always in the set of values of `<expression>`.

## Examples

```sql
CREATE ROW TABLE p_disc (class CHAR(10), val INT, offset INT);
 INSERT INTO p_disc VALUES('A', 1, 1);
 INSERT INTO p_disc VALUES('A', 3, 3);
 INSERT INTO p_disc VALUES('A', 5, null);
 INSERT INTO p_disc VALUES('A', 5, 2);
 INSERT INTO p_disc VALUES('A', 10, 0);
 INSERT INTO p_disc VALUES('B', 1, 3);
 INSERT INTO p_disc VALUES('B', 1, 1);
 INSERT INTO p_disc VALUES('B', 7, 1);
```

```sql
SELECT class,
 val,
 PERCENTILE_DISC(0.125) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pd1,
 PERCENTILE_DISC(0.5) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pd2,
 PERCENTILE_DISC(0.875) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pd3
FROM p_disc;
```

| **CLASS** | **VAL** | **PD1** | **PD2** | **PD3** |
| --- | --- | --- | --- | --- |
| A | 1 | 1 | 5 | 10 |
| A | 3 | 1 | 5 | 10 |
| A | 5 | 1 | 5 | 10 |
| A | 5 | 1 | 5 | 10 |
| A | 10 | 1 | 5 | 10 |
| B | 1 | 1 | 1 | 7 |
| B | 1 | 1 | 1 | 7 |
| B | 7 | 1 | 1 | 7 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) PERCENTILE_CONT Function (Window) [→](PERCENTILE_CONT-Function-Window.md)
