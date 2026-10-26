# 4.9.14 Window Functions and the Window Specification

> [↑ 4.9 SQL Functions](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 408–413

Window functions allow you to perform analytic operations over a set of input rows.

## Syntax

```sql
<function_name> <window_specification>

<window_specification> ::= OVER ( { [ <window_partition_by_clause> ]
[ <window_order_by_clause> ] [ <window_frame_clause> ] } )
```

## Syntax Elements

#### function_name

Specifies the window function to operate over the data. See the individual function topics for more information on their syntax.

```sql
<function_name> ::=
 BINNING
 | CUBIC_SPLINE_APPROX
 | CUME_DIST
 | DENSE_RANK
 | LAG
 | LEAD
 | LINEAR_APPROX
 | NTILE
 | PERCENT_RANK
 | PERCENTILE_CONT
 | PERCENTILE_DISC
 | RANDOM_PARTITION
 | RANK
 | ROW_NUMBER
 | SERIES_FILTER
 | WEIGHTED_AVG
 | <window_aggregate_functions>
 | <spatial_functions>
```

For `<window_aggregate_functions>`, see Window Aggregate Functions [→](4.09.14.01-Window-Aggregate-Functions.md).

For `<spatial_functions>`, see the SAP HANA Spatial Reference guide.

#### window_partition_by_clause

```sql
<window_partition_by_clause> ::= PARTITION BY <expression> [ { ,
<expression> } ... ]
```

Creates one or more window partitions using the supplied expressions.

#### window_order_by_clause

Defines the sort order of the window.

```sql
<window_order_by_clause> ::= ORDER BY <window_order_by_expression> [ {,
<window_order_by_expression> }  ... ]
<window_order_by_expression> ::=
 <column> [ <collate_clause> ] [ ASC | DESC ] [ NULLS { FIRST | LAST } ]
<collate_clause> ::= COLLATE <collation_name>
```

##### collate_clause

Specifies the collation to use. `<collate_clause>` can only be used on columns defined as NVARCHAR or VARCHAR.

`<collation_name>` is one of the supported collation names listed in the COLLATIONS system view.

##### [ ASC | DESC ]

ASC sorts records in ascending order and DESC sorts records in descending order. The default is ASC.

##### [ NULLS FIRST | NULLS LAST ]

Specifies the ordering of NULL values.

##### position

`<position>` uses the entries in the select list to define the ordering required. For example:

```sql
SELECT col1, col2 FROM t ORDER BY 2;
```

ORDER BY 2 indicates that ordering should be undertaken using the second expression in the select list, which in this case is col2.

#### window_frame_clause

Defines the rows (bounds) of a window partition by specifying the number of rows preceding or following with respect to the current row. If you specify a `<window_frame_clause>`, you must also specify a `<window_order_by_clause>`.

```sql
<window_frame_clause> ::= <window_frame_unit> <window_frame_extent>
<window_frame_extent> ::= { <window_frame_start> | <window_frame_between> }
<window_frame_unit> ::= ROWS
<window_frame_start> ::= { UNBOUNDED PRECEDING | <window_frame_preceding> |
CURRENT ROW }
<window_frame_preceding> ::= <unsigned_integer> PRECEDING
<window_frame_between> ::= BETWEEN <lower_window_frame_bound> AND
<upper_window_frame_bound>
<lower_window_frame_bound> ::= <window_frame_bound>
<upper_window_frame_bound> ::= <window_frame_bound>
<window_frame_bound> := { <window_frame_start> | UNBOUNDED FOLLOWING |
<window_frame_following> }
<window_frame_following> ::= <unsigned_integer> FOLLOWING
```

`<window_frame_between>` specifies the lower (starting) bound and the upper (ending) bound of the window frame. The upper bound cannot be smaller than the lower bound.

UNBOUND PRECEDING specifies that the window starts at the first row of the partition. It can only be specified as `<window_frame_start>`. CURRENT ROW specifies that the window starts or ends at the current row when used with ROWS.

PRECEDING indicates that the number of rows or values to precede the current row. `<unsigned_integer>` should be 0 or a positive integer literal.

UNBOUNDED FOLLOWING specifies that the window ends at the last row of the partition. UNBOUNDED FOLLOWING can only be specified as a window frame end.

FOLLOWING indicates the number of rows or values to follow the current row. When specified as the window frame start, the window frame end should be `<unsigned_integer>` FOLLOWING. The `<unsigned_integer>` should be 0 or a positive integer literal.

## Description

The window functions allow you to divide the result sets of a query, or a logical partition of a query, into groups of rows called window partitions.

A window partition is specified by one or more expressions in the OVER clause.

Window functions not in the following list must have an ORDER BY clause in the OVER clause:

- AVG
- CORR
- CORR_SPEARMAN
- COUNT
- MAX
- MEDIAN
- MIN
- PERCENTILE_CONT
- PERCENTILE_DISC
- ROW_NUMBER
- STDDEV
- SUM
- VAR

Result sets are first partitioned as specified by PARTITION BY clause, and then sorted by ORDER BY clause specification within the window partition.

Finally window functions are applied to each row within window partition boundaries.

The ORDER BY clause in the OVER clause is only used to evaluate window function so that the order of resulting rows is non-deterministic if not specified by ORDER BY for SELECT.

The default window frame of the window function depends on whether or not a window ORDER BY clause is specified. If a window ORDER BY clause is specified, the default window frame becomes 'between UNBOUNDED PRECEDING and CURRENT ROW'. That is to say that the window function computes on rows preceding or peer with current row. As a result, the function returns cumulative values.

If a window ORDER BY clause is not specified, the default window frame becomes 'between UNBOUNDED PRECEDING and UNBOUNDED FOLLOWING'. That is to say that the window function computes on the whole window partition. As a result, the function returns the same value within a window partition regardless of current row.

## Examples

The examples use the example table T defined below.

```sql
CREATE TABLE myTable (Class CHAR(10), Value INT, Offset INT);
 INSERT INTO myTable VALUES('A', 1, 1);
 INSERT INTO myTable VALUES('A', 3, 3);
 INSERT INTO myTable VALUES('A', 5, NULL);
 INSERT INTO myTable VALUES('A', 5, 2);
 INSERT INTO myTable VALUES('A', 10, 0);
 INSERT INTO myTable VALUES('B', 1, 3);
 INSERT INTO myTable VALUES('B', 1, 1);
 INSERT INTO myTable VALUES('B', 7, 1);
```

```sql
SELECT Class, VAL,
  ROW_NUMBER() OVER (PARTITION BY Class ORDER BY Value) AS ROW_NUM,
  RANK() OVER (PARTITION BY Class ORDER BY Value) AS RANK,
  DENSE_RANK() OVER (PARTITION BY Class ORDER BY Value) AS DENSE_RANK
 FROM myTable;
```

| class | val | row_num | rank | dense_rank |
| --- | --- | --- | --- | --- |

| A | 1 | 1 | 1 | 1 |
| --- | --- | --- | --- | --- |
| A | 3 | 2 | 2 | 2 |
| A | 5 | 3 | 3 | 3 |
| A | 5 | 4 | 3 | 3 |
| A | 10 | 5 | 5 | 4 |
| B | 1 | 1 | 1 | 1 |
| B | 1 | 2 | 1 | 1 |
| B | 7 | 3 | 3 | 2 |

## Related Information

Window Aggregate Functions [→](4.09.14.01-Window-Aggregate-Functions.md) BINNING Function (Window) [→](../4.09.01-Functions-A-Z/BINNING-Function-Window.md) CUBIC_SPLINE_APPROX Function (Window) [→](../4.09.01-Functions-A-Z/CUBIC_SPLINE_APPROX-Function-Window.md) COLLATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md) CUME_DIST Function (Window) [→](../4.09.01-Functions-A-Z/CUME_DIST-Function-Window.md) DENSE_RANK Function (Window) [→](../4.09.01-Functions-A-Z/DENSE_RANK-Function-Window.md) LAG Function (Window) [→](../4.09.01-Functions-A-Z/LAG-Function-Window.md) LEAD Function (Window) [→](../4.09.01-Functions-A-Z/LEAD-Function-Window.md) LINEAR_APPROX Function (Window) [→](../4.09.01-Functions-A-Z/LINEAR_APPROX-Function-Window.md) NTILE Function (Window) [→](../4.09.01-Functions-A-Z/NTILE-Function-Window.md) PERCENT_RANK Function (Window) [→](../4.09.01-Functions-A-Z/PERCENT_RANK-Function-Window.md) PERCENTILE_CONT Function (Window) [→](../4.09.01-Functions-A-Z/PERCENTILE_CONT-Function-Window.md) PERCENTILE_DISC Function (Window) [→](../4.09.01-Functions-A-Z/PERCENTILE_DISC-Function-Window.md) RANDOM_PARTITION Function (Window) [→](../4.09.01-Functions-A-Z/RANDOM_PARTITION-Function-Window.md) RANK Function (Window) [→](../4.09.01-Functions-A-Z/RANK-Function-Window.md) ROW_NUMBER Function (Window) [→](../4.09.01-Functions-A-Z/ROW_NUMBER-Function-Window.md) SERIES_FILTER Function (Window) [→](../4.09.01-Functions-A-Z/SERIES_FILTER-Function-Window.md) WEIGHTED_AVG Function (Window) [→](../4.09.01-Functions-A-Z/WEIGHTED_AVG-Function-Window.md)

## Contenido de esta sección

- [4.9.14.1 Window Aggregate Functions](4.09.14.01-Window-Aggregate-Functions.md)
