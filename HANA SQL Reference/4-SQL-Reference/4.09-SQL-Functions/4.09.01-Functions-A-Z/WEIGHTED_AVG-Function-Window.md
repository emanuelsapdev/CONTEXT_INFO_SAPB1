# 4.9.1.231 WEIGHTED_AVG Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 382–384

Computes a weighted moving average by using arithmetically decreasing weights.

## Syntax

```sql
WEIGHTED_AVG(<expression>) <window_specification>
```

## Syntax Elements

#### expression

`<expression>` indicates a numeric column that is used in the weighted moving average calculation.

In a window frame where `<n>` represents the actual number of elements (ROWS or GROUPS) in the window frame, and `<i>` represents the element number in the series, the weight factors are calculated with the following algorithm:

```sql
weight(<i>) = 2 * (<n> + 1 - <i>) / (<n> * (<n> + 1))
```

The weight factors are applied in reverse order so that in a window frame with n rows, the first weight factor is multiplied with the value of row n, the second weight factor with the value of row n-1, and so on. When using WEIGHTED_AVG with the GROUPS unit, the values within a group are first arithmetically averaged before they are multiplied with the corresponding weight factor.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Computes a weighted moving average by using arithmetically decreasing weights.

## Examples

```sql
CREATE ROW TABLE weather (station INT, ts DATE, temperature FLOAT);
INSERT INTO weather VALUES(1, '2014-01-01', 0.0);
INSERT INTO weather VALUES(1, '2014-01-02', 3.0);
INSERT INTO weather VALUES(1, '2014-01-03', 4.5);
INSERT INTO weather VALUES(1, '2014-01-04', 6.0);
INSERT INTO weather VALUES(1, '2014-01-05', 6.3);
INSERT INTO weather VALUES(1, '2014-01-06', 5.9);
INSERT INTO weather VALUES(2, '2014-01-01', 1.0);
INSERT INTO weather VALUES(2, '2014-01-02', 3.4);
INSERT INTO weather VALUES(2, '2014-01-03', 5.0);
INSERT INTO weather VALUES(2, '2014-01-04', 6.7);
INSERT INTO weather VALUES(2, '2014-01-05', 4.6);
INSERT INTO weather VALUES(2, '2014-01-06', 6.9);
SELECT ts, temperature, WEIGHTED_AVG(temperature) OVER (ORDER BY ts ROWS BETWEEN
1 PRECEDING AND CURRENT ROW) FROM weather ORDER BY ts;
```

| **ts** | **TEMPERATURE** | **WEIGHTED_AVG(temperature) OVER(ORDER BY ts ROWS BETWEEN 1PRECEDING AND CURRENT ROW) FROMweather ORDER BY ts** |
| --- | --- | --- |
| 01.01.2014 | 0 | 0 |
| 01.01.2014 | 1 | 0.6666666666666666 |
| 02.01.2014 | 3 | 2.3333333333333335 |
| 02.01.2014 | 3.4 | 3.2666666666666666 |
| 03.01.2014 | 4.5 | 4.133333333333333 |
| 03.01.2014 | 5 | 4.833333333333333 |
| 04.01.2014 | 6 | 5.666666666666666 |
| 04.01.2014 | 6.7 | 6.466666666666667 |
| 05.01.2014 | 6.3 | 6.433333333333333 |
| 05.01.2014 | 4.6 | 5.166666666666666 |
| 06.01.2014 | 5.9 | 5.466666666666667 |
| 06.01.2014 | 6.9 | 6.566666666666666 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
