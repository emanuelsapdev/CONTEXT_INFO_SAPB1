# 4.9.1.123 MEDIAN Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 250–253

Finds the statistical median of an input expression with a numeric data type. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
MEDIAN( <expression> )
```

### Window function:

```sql
MEDIAN( <expression> ) <window_specification>
```

## Syntax Elements

#### expression

Specifies the input data expression for the MEDIAN function.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The MEDIAN function finds the statistical median of an input expression with a numeric data type. Although it is grouped with the aggregate functions, its optional OVER clause positions it as a windows function as well.

Null values are eliminated. If there is an even number of elements, then the average of the two middle elements is returned. Otherwise, the middle element is returned.

The result type is the type that is selected for the expression "x/2" for an x value of the input data type.

## Examples

**Median of integer input** The following example returns a median value of `2`.

```sql
CREATE ROW TABLE T (class CHAR(10), date DAYDATE, val INT);
INSERT INTO T VALUES('A', '01.01.1972', 1);
INSERT INTO T VALUES('A', '02.01.1972', 3);
INSERT INTO T VALUES('A', '03.01.1972', null);
INSERT INTO T VALUES('A', '04.01.1972', 2);
SELECT MEDIAN(val) "median value" FROM T;
```

If the number of non-null values is even, then the average of the two middle values is returned. For the following example, the average of 2 and 3 is returned. Since the input and output types are the same, the integer is rounded. The returned result is `3`.

```sql
INSERT INTO T VALUES('A', '05.01.1972', 4);
SELECT MEDIAN(val) "median value" FROM T;
```

**Median of double input** The following example uses double values instead of integers. The returned result is `2.5`.

```sql
CREATE ROW TABLE T (TS_ID CHAR(10), date DAYDATE, val DOUBLE);
INSERT INTO T VALUES('A', '01.01.1972', 1.0);
INSERT INTO T VALUES('A', '02.01.1972', 3.0);
INSERT INTO T VALUES('A', '03.01.1972', null);
INSERT INTO T VALUES('A', '04.01.1972', 2.0);
INSERT INTO T VALUES('A', '05.01.1972', 4.0);
SELECT MEDIAN(val) "median value" FROM T;
```

**Median as a window function** The following example uses double values instead of integers.

```sql
CREATE ROW TABLE T (TS_ID CHAR(10), date DAYDATE, val DOUBLE);
INSERT INTO T VALUES('A', '01.01.1972', 1.0);
INSERT INTO T VALUES('A', '02.01.1972', 3.0);
INSERT INTO T VALUES('A', '03.01.1972', null);
INSERT INTO T VALUES('A', '04.01.1972', 2.0);
INSERT INTO T VALUES('A', '04.01.1972', 4.0);
SELECT MEDIAN(val) OVER (PARTITION BY TS_ID ) AS WF1 FROM T;
```

The returned result is:

| **WF1** |
| --- |
| 2.5 |
| 2.5 |
| 2.5 |
| 2.5 |
| 2.5 |

**Median of sliding window (GROUPS BETWEEN)** Both of the SELECT statements in the following example produce identical results.

```sql
CREATE ROW TABLE T (TS_ID CHAR(10), date DAYDATE, val DOUBLE);
INSERT INTO T VALUES('A', '01.01.1972', 1.0);
INSERT INTO T VALUES('A', '02.01.1972', 3.0);
INSERT INTO T VALUES('A', '03.01.1972', null);
INSERT INTO T VALUES('A', '04.01.1972', 2.0);
INSERT INTO T VALUES('A', '04.01.1972', 4.0);
SELECT MEDIAN(val) OVER (PARTITION BY TS_ID ORDER BY date) AS WF2A FROM T;
SELECT MEDIAN(val) OVER (PARTITION BY TS_ID ORDER BY date GROUPS BETWEEN
UNBOUNDED PRECEDING AND CURRENT ROW) AS WF2B FROM T;
```

The returned result is:

| **WF2B** |
| --- |
| 1 |
| 1 |
| 2 |
| 2 |
| 2 |
| 2 |
| 2.5 |
| 2.5 |
| 2.5 |
| 2.5 |

**Median of sliding window (ROWS BETWEEN)** The following example uses ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW.

```sql
CREATE ROW TABLE T (TS_ID CHAR(10), date DAYDATE, val DOUBLE);
INSERT INTO T VALUES('A', '01.01.1972', 1.0);
INSERT INTO T VALUES('A', '02.01.1972', 3.0);
INSERT INTO T VALUES('A', '03.01.1972', null);
INSERT INTO T VALUES('A', '04.01.1972', 2.0);
INSERT INTO T VALUES('A', '04.01.1972', 4.0);
SELECT MEDIAN(val) OVER (PARTITION BY TS_ID ORDER BY date ROWS BETWEEN UNBOUNDED
PRECEDING AND CURRENT ROW) AS WF3 FROM T;
```

The returned result is:

| **WF3** |
| --- |
| 1 |
| 1 |
| 1 |
| 1 |
| 1 |
| 2 |
| 2 |
| 2 |
| 2 |
| 2 |
| 2.5 |
| 2 |
| 2.5 |
| 2 |
| 2.5 |

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) Expressions [→](../../4.06-Expressions.md)
