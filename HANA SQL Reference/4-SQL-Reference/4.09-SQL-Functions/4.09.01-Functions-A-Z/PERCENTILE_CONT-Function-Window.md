# 4.9.1.145 PERCENTILE_CONT Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 276–278

Returns an interpolated value using the percentile value of a constant.

## Syntax

```sql
PERCENTILE_CONT( <constant_literal> ) WITHIN GROUP ( ORDER BY <expression> [ ASC
| DESC ] [ NULLS FIRST | NULLS LAST ] ) <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Returns an interpolated value using the percentile value of `<constant_literal>`.

A continuous distribution of the values of `<expression>` is assumed. Only a single `<expression>` can be specified in ORDER BY clause; this expression must evaluate to a numeric type. The `<constant_literal>` should be a numeric value between, and including, 0 to 1, because it is a percentile value. In the interpolation, nulls are discarded in the calculation, and all indexes are 1 based. The details of the interpolation are as follows:

```sql
NR = the number of
                rows in the window partition R* P = the specified
                percentile value** INDEX1 = floor( 1 + ( P * (NR - 1) ) )
                INDEX2 = ceil( 1 + ( P * (NR - 1) ) )
                COEF1 = INDEX2 - ( 1 + ( P * (NR - 1) ) )
                COEF2 = INDEX1 - ( 1 + ( P * (NR - 1) ) )

                if INDEX1 == INDEX2
                then returns (value at INDEX1)
                else returns ( ( value at INDEX1 ) * COEF1 + ( value at INDEX2 )
* COEF2 )
```

## Examples

```sql
DROP TABLE p_cont;
CREATE ROW TABLE p_cont (class CHAR(10), val INT, offset INT);
 INSERT INTO p_cont VALUES('A', 1, 1);
 INSERT INTO p_cont VALUES('A', 3, 3);
 INSERT INTO p_cont VALUES('A', 5, null);
 INSERT INTO p_cont VALUES('A', 5, 2);
 INSERT INTO p_cont VALUES('A', 10, 0);
 INSERT INTO p_cont VALUES('B', 1, 3);
 INSERT INTO p_cont VALUES('B', 1, 1);
 INSERT INTO p_cont VALUES('B', 7, 1);
```

```sql
SELECT class,
 val,
 PERCENTILE_CONT(0.125) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pc1,
 PERCENTILE_CONT(0.5) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pc2,
 PERCENTILE_CONT(0.875) WITHIN GROUP (ORDER BY val) OVER (PARTITION BY class) AS
pc3
FROM p_cont;
```

| **CLASS** | **VAL** | **PC1** | **PC2** | **PC3** |
| --- | --- | --- | --- | --- |
| A | 1 | 2.0 | 5.0 | 7.5 |
| A | 3 | 2.0 | 5.0 | 7.5 |
| A | 5 | 2.0 | 5.0 | 7.5 |
| A | 5 | 2.0 | 5.0 | 7.5 |
| A | 10 | 2.0 | 5.0 | 7.5 |
| B | 1 | 1.0 | 1.0 | 5.5 |
| B | 1 | 1.0 | 1.0 | 5.5 |
| B | 7 | 1.0 | 1.0 | 5.5 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) PERCENTILE_DISC Function (Window) [→](PERCENTILE_DISC-Function-Window.md)
