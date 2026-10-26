# 4.9.1.170 SERIES_FILTER Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 313–317

Performs a filtered calculation on a series of data.

## Syntax

```sql
SERIES_FILTER(<filter_parameter> => <expression> [, <filter_parameter> =>
<expression> ... ])
 OVER (
   [ <series_definition> | <series_reference> ]
   [ <window_partition_by_clause> ]
   [ ORDER BY <window_order_by_expression> ]
   [ <window_frame_clause> ]
      )
```

## Syntax Elements

#### filter_parameter

```sql
<filter_parameter> ::= VALUE | METHOD_NAME | ALPHA | BETA
```

VALUE is a required parameter that specifies the column to which the filter is applied. The column must represent numeric data. NULL values are not permitted.

METHOD_NAME is a required parameter that specifies the name of the filter method. Specify SINGLESMOOTH for single exponential smoothing or DOUBLESMOOTH for double exponential smoothing.

ALPHA is an optional smoothing decimal parameter for the level of the series that ranges between 0 and 1. The default value is 0.1.

BETA is a smoothing decimal parameter for the trend of the series that ranges between 0 and 1. The default value is 0.1. This parameter is only required for double exponential smoothing.

SERIES_FILTER implements several filtering algorithms that are identified by METHOD_NAME. Trailing NULL values in the input series are replaced by forecasted values.

All filter algorithms require that the series is equidistant and it must not contain any missing values. The function returns an error when it is called with a series property indicating a property that does not match.

#### window_partition_by_clause

Specifies one or more partitions to be created using the supplied expressions.

```sql
<window_partition_by_clause> ::= PARTITION BY <expression> [ { ,
<expression> } ... ]
```

#### window_order_by_expression

Determines the order of the input. Only one expression must be supplied in the `<window_order_by_expression>` for this function.

This expression must not contain any null values or duplicates. See the description of the `<window_order_by_clause>` clause in the Window Functions topic for other syntax information for this clause.

#### window_frame_clause

Physically limits the rows within a partition by specifying a number of rows preceding or following the current row.

```sql
<window_frame_clause> ::= <window_frame_unit> <window_frame_extent>
<window_frame_unit> ::= ROWS
<window_frame_extent> ::= <window_frame_start> | <window_frame_between>
<window_frame_start> ::= UNBOUNDED PRECEDING | <window_frame_preceding> |
CURRENT ROW
<window_frame_preceding> ::= <unsigned_integer> PRECEDING
<window_frame_between> ::= BETWEEN <lower_window_frame_bound> AND
<upper_window_frame_bound>
<lower_window_frame_bound> ::= <window_frame_bound>
<upper_window_frame_bound> ::= <window_frame_bound>
<window_frame_bound> := <window_frame_start> | UNBOUNDED FOLLOWING |
<window_frame_following>
<window_frame_following> ::= <unsigned_integer> FOLLOWING
```

ROWS requires a ORDER BY clause to be specified.

UNBOUND PRECEDING specifies that the window starts at the first row of the partition. It can only be specified as `<window_frame_start>`. CURRENT ROW specifies that the window starts or ends at the current row when used with ROWS.

PRECEDING indicates that the number of rows or values to precede the current row. `<unsigned_integer>` should be 0 or a positive integer literal.

`<lower_window_frame_bound>` and `<upper_window_frame_bound>` specify the lower (starting) bound and the upper (ending) bound of the window frame. The upper bound cannot be smaller than the lower bound.

UNBOUNDED FOLLOWING specifies that the window ends at the last row of the partition. UNBOUNDED FOLLOWING can only be specified as a window frame end.

FOLLOWING indicates the number of rows or values to follow the current row. When specified as the window frame start, the window frame end should be `<unsigned_integer>` FOLLOWING. The `<unsigned_integer>` should be 0 or a positive integer literal.

## Description

The window functions allow you to divide the result sets of a query, or a logical partition of a query, into groups of rows called window partitions.

A window partition is specified by one or more expressions in the OVER clause.

Window functions other than ROW_NUMBER, PERCENTILE_DISC, PERCENTILE_CONT and the window aggregate functions must have an ORDER BY clause in the OVER clause.

Result sets are first partitioned as specified by the PARTITION BY clause, and then sorted by ORDER BY clause specification within the window partition. Then, window functions are applied to each row within window partition boundaries.

The ORDER BY clause in the OVER clause only evaluates the window function so that the order of resulting rows is non-deterministic if not specified by ORDER BY for SELECT.

The default window frame of the window function depends on whether a window ORDER BY clause is specified. If a window ORDER BY clause is specified, then the default window frame becomes 'between UNBOUNDED PRECEDING and CURRENT ROW': The window function computes on rows preceding or peer with the current row. As a result, the function returns cumulative values.

If a window ORDER BY clause is not specified, then the default window frame becomes 'between UNBOUNDED PRECEDING and UNBOUNDED FOLLOWING': The window function computes on the whole window partition. As a result, the function returns the same value within a window partition regardless of current row.

## Examples

The following example illustrates single and double exponential smoothing with forecasting.

```sql
DROP TABLE weather;
CREATE COLUMN TABLE weather (ts DATE, temperature FLOAT);
INSERT INTO weather VALUES('2014-01-01', 0);
INSERT INTO weather VALUES('2014-01-02', 3);
INSERT INTO weather VALUES('2014-01-03', 4.5);
INSERT INTO weather VALUES('2014-01-04', 6);
INSERT INTO weather VALUES('2014-01-05', 6.3);
INSERT INTO weather VALUES('2014-01-06', 6.9);
INSERT INTO weather VALUES('2014-01-07', NULL);
INSERT INTO weather VALUES('2014-01-08', NULL);
SELECT ts, temperature,
       SERIES_FILTER(VALUE => temperature, METHOD_NAME => 'SINGLESMOOTH', ALPHA
=> 0.2) OVER (ORDER BY ts) AS SES,
       SERIES_FILTER(VALUE => temperature, METHOD_NAME => 'DOUBLESMOOTH', ALPHA
=> 0.2, BETA => 0.3) OVER (ORDER BY ts) AS DES
FROM weather;
```

| **TS** | **TEMPERATURE** | **SES** | **DES** |
| --- | --- | --- | --- |
| 01.01.2014 | 0.0 | NULL | NULL |
| 02.01.2014 | 3.0 | 0 | 3 |
| 03.01.2014 | 4.5 | 0.6000000000000001 | 6 |
| 04.01.2014 | 6.0 | 1.3800000000000001 | 8.61 |
| 05.01.2014 | 6.3 | 2.3040000000000003 | 10.8414 |
| 06.01.2014 | 6.9 | 3.1032 | 12.414036 |
| 07.01.2014 | NULL | 3.86256 | 13.46130264 |
| 08.01.2014 | NULL | 3.86256 | 15.61137648 |

The following example uses a window frame ROWS specification:

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
```

```sql
SELECT class,
  val,
  SUM(val) OVER(PARTITION BY class ORDER BY val) AS s0,
  SUM(val) OVER(PARTITION BY class ORDER BY val ROWS BETWEENn UNBOUNDED
PRECEDING AND UNBOUNDED FOLLOWING) AS s1,
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN UNBOUNDED
PRECEDING AND CURRENT ROW) AS s2,
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN UNBOUNDED
PRECEDING AND 1 PRECEDING) AS s3,
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN UNBOUNDED
PRECEDING AND 1 FOLLOWING) AS s4
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN CURRENT ROW AND
UNBOUNDED FOLLOWING) AS s5,
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN CURRENT ROW AND
CURRENT ROW) AS s6,
  SUM(val) OVER (PARTITION BY class ORDER BY val ROWS BETWEEN CURRENT ROW AND 1
FOLLOWING) AS s7
 FROM T;
```

| **CLASS** | **VAL** | **S0** | **S1** | **S2** | **S3** | **S4** | **S5** | **S6** | **S7** | **S8** | **S9** | **S10** | **S11** | **S12** | **S13** | **S14** | **S15** | **S16** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A | 1 | 1 | 24 | 1 | null | 4 | 24 | 1 | 4 | 24 | 1 | null | 4 | 23 | 8 | 1 | 1 | 1 |
| A | 3 | 4 | 24 | 4 | 1 | 9 | 23 | 3 | 8 | 24 | 4 | 1 | 9 | 20 | 10 | 4 | 3 | 4 |
| A | 5 | 14 | 24 | 9 | 4 | 14 | 20 | 5 | 10 | 23 | 8 | 4 | 13 | 15 | 15 | 9 | 5 | 8 |
| A | 5 | 14 | 24 | 14 | 9 | 24 | 15 | 5 | 15 | 20 | 10 | 8 | 20 | 10 | 10 | 14 | 5 | 10 |
| A | 10 | 24 | 24 | 24 | 14 | 24 | 10 | 10 | 10 | 15 | 15 | 10 | 15 | null | null | 24 | 10 | 15 |
| B | 1 | 2 | 9 | 1 | null | 2 | 9 | 1 | 2 | 9 | 1 | null | 2 | 8 | 8 | 1 | 1 | 1 |
| B | 1 | 9 | 9 | 2 | 1 | 9 | 8 | 1 | 8 | 9 | 2 | 1 | 9 | 7 | 7 | 2 | 1 | 2 |
| B | 7 | 9 | 9 | 9 | 2 | 9 | 7 | 7 | 7 | 8 | 8 | 2 | 8 | null | null | 9 | 7 | 8 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
