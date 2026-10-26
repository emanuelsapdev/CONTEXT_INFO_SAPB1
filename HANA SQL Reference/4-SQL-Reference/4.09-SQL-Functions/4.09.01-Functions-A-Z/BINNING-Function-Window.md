# 4.9.1.21 BINNING Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 108–110

Partitions an input set into disjoint subsets by assigning a bin number to each row.

## Syntax

```sql
BINNING( <binning_param> => <expression> [ {, <binning_parameter> =>
<expression> } ... ] ) <window_specification>
<binning_param> ::= VALUE | BIN_COUNT | BIN_WIDTH | TILE_COUNT | STDDEV_COUNT
```

## Syntax Elements

#### binning_param

VALUE is always required. It specifies the column that binning is applied to. When BIN_WIDTH is used, the input column must have a numeric data type. BIN_COUNT specifies the number of equal-width bins. BIN_WIDTH specifies the width of the bins. TILE_COUNT specifies the number of bins with equal number of records. STDDEV_COUNT specifies the number of standard deviations left and right from the mean.

The appropriate binning method is selected based on the parameter specified – exactly one of the last four parameters must be non-NULL. The value assigned to binning method parameter must be an integer expression.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The OVER clause must not specify a `<window_order_by_clause>` nor any window frame since the binning function works on an entire partition.

## Examples

The following example distributes the value of the input set into four bins that all have an equal width.

```sql
DROP TABLE weather;
CREATE ROW TABLE weather (station INT, ts DATE, temperature FLOAT);
INSERT INTO weather VALUES(1, '2014-01-01', 0);
INSERT INTO weather VALUES(1, '2014-01-02', 3);
INSERT INTO weather VALUES(1, '2014-01-03', 4.5);
INSERT INTO weather VALUES(1, '2014-01-04', 6);
INSERT INTO weather VALUES(1, '2014-01-05', 6.3);
INSERT INTO weather VALUES(1, '2014-01-06', 5.9);
INSERT INTO weather VALUES(1, '2015-01-01', 1);
INSERT INTO weather VALUES(1, '2015-01-02', 3.4);
INSERT INTO weather VALUES(1, '2015-01-03', 5);
INSERT INTO weather VALUES(1, '2015-01-04', 6.7);
INSERT INTO weather VALUES(1, '2015-01-05', 4.6);
INSERT INTO weather VALUES(1, '2015-01-06', 6.9);
SELECT *, BINNING(VALUE => temperature, BIN_COUNT => 4) OVER () AS bin_num FROM
weather;
```

| **STATION** | **TS** | **TEMPERATURE** | **BIN_NUM** |
| --- | --- | --- | --- |
| 1 | 01.01.2014 | 0.0 | 1 |
| 1 | 02.01.2014 | 3.0 | 2 |
| 1 | 03.01.2014 | 4.5 | 3 |
| 1 | 04.01.2014 | 6.0 | 4 |
| 1 | 05.01.2014 | 6.3 | 4 |
| 1 | 06.01.2014 | 5.9 | 4 |
| 1 | 01.01.2014 | 1.0 | 1 |
| 1 | 02.01.2014 | 3.4 | 2 |
| 1 | 03.01.2014 | 5.0 | 3 |
| 1 | 04.01.2014 | 6.7 | 4 |
| 1 | 05.01.2014 | 4.6 | 3 |
| 1 | 06.01.2014 | 6.9 | 4 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
