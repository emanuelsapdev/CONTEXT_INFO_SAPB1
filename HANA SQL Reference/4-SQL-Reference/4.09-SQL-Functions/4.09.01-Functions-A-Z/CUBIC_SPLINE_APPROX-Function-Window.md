# 4.9.1.48 CUBIC_SPLINE_APPROX Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 154–159

Replaces null values by interpolating the gaps based on calculated cubic splines and linearly extrapolating any leading or trailing null values.

## Syntax

```sql
CUBIC_SPLINE_APPROX ( <expression> [, <BoundaryConditionArgument> [,
<ExtrapolationModeArgument> [, <Value1Argument> [, <Value2Argument> ] ] ] ] )
 [ OVER ( {
     SERIES TABLE <series_table> [ PARTITION BY <col1> [,...]
[ <window_order_by_clause> ]
   | SERIES(...) [ PARTITION BY <col1> [,...] [ <window_order_by_clause> ]
   | [ PARTITION BY <col1>[,...] <window_order_by_clause>
     } ) ]
```

## Syntax Elements

#### expression

Specifies the input data expression

#### series_table

Defines the series table.

```sql
<series_table> ::= [<schema_name>.]<table_name>
<schema_name> ::= <unicode_name>
<table_name> ::= <identifier>
```

`<table_schema>` must be a base table name, and not a correlation name.

#### BoundaryConditionArgument

Specifies the boundary conditions that are used for the cubic spline calculation. The default value is SPLINE_TYPE_NATURAL. If this parameter is omitted, then natural boundary conditions are used to calculate the interpolating cubic splines.

```sql
<BoundaryConditionArgument> ::= SPLINE_TYPE_NATURAL | SPLINE_TYPE_NOT_A_KNOT
```

#### ExtrapolationModeArgument

Defines the applied extrapolation mode. The default value is EXTRAPOLATION_NONE, which indicates that extrapolation does not occur if this parameter is omitted.

```sql
<ExtrapolationModeArgument> ::= EXTRAPOLATION_NONE
 | EXTRAPOLATION_LINEAR
 | EXTRAPOLATION_CONSTANT
```

The definition, default value, and use of ExtrapolationModeArgument in conjunction with the Value1Argument and Value2Argument is identical to the LINEAR_APPROX function except from the calculation of the slope.

When using EXTRAPOLATION_LINEAR mode, the slope of the extrapolation line is set equal to the slope of the calculated cubic splines at the boundary points. For example, the slope of the calculated spline at the first non-null value is taken as the slope of the extrapolating line for leading nulls. Similarly, the slope of the calculated spline at the last non-null value is taken as the slope of the extrapolating line for trailing nulls.

Cubic spline interpolation can be applied to all number types that can be cast into long double type, such as INT, LONG, DOUBLE, or FLOAT.

#### window_order_by_clause

Determines the sort order. This expression must not contain any NULL values or duplicates. See the syntax of this clause located in the Window Functions topic.

## Description

Replaces null values by interpolating the gaps based on calculated cubic splines and linearly extrapolating any leading or trailing null values.

## Examples

### Natural cubic spline interpolation

Perform natural cubic spline interpolation:

```sql
SELECT CUBIC_SPLINE_APPROX(temperature, 'SPLINE_TYPE_NATURAL') OVER (PARTITION
BY station ORDER BY ts)
  FROM WEATHER;
```

For natural boundary conditions, the BoundaryConditionArgument can be omitted. The following query returns identical results to the above one:

```sql
SELECT CUBIC_SPLINE_APPROX(temperature)
    OVER(PARTITION BY station ORDER BY ts) FROM WEATHER;
```

Perform cubic spline interpolation by using not-a-knot boundary conditions:

```sql
SELECT CUBIC_SPLINE_APPROX(temperature, 'SPLINE_TYPE_NOT_A_KNOT')
    OVER(PARTITION BY station ORDER BY ts) FROM WEATHER;
```

### Cubic spline interpolation using series table

Perform cubic spline interpolation on a series by using a series table. In this example, the not-a-knot boundary condition is used, and it returns [?, 1, 2, 7, 10, 5, ?].

```sql
DROP TABLE InterpolationTable;
 CREATE COLUMN TABLE InterpolationTable (ts_id VARCHAR(20), date DAYDATE, val
DOUBLE)
    SERIES(SERIES KEY(ts_id) PERIOD FOR SERIES(date)
    EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS ALLOWED);
INSERT INTO InterpolationTable VALUES('A','2013-09-29', null);
INSERT INTO InterpolationTable VALUES('A','2013-09-30', 1);
INSERT INTO InterpolationTable VALUES('A','2013-10-01', 2);
INSERT INTO InterpolationTable VALUES('A','2013-10-02', null);
INSERT INTO InterpolationTable VALUES('A','2013-10-03', 10);
INSERT INTO InterpolationTable VALUES('A','2013-10-04', 5);
INSERT INTO InterpolationTable VALUES('A','2013-10-05', null);
SELECT CUBIC_SPLINE_APPROX(val, 'SPLINE_TYPE_NOT_A_KNOT')
    OVER(SERIES TABLE InterpolationTable) AS MyResult
 FROM InterpolationTable;
```

| **MYRESULT** |
| --- |
| ? |
| 1 |
| 2 |
| 7 |
| 10 |
| 5 |
| ? |

### Cubic spline interpolation together with linear extrapolation

This example extrapolates leading and trailing nulls, besides cubic spline interpolation. The slope of the line extrapolating the leading nulls is equal to the slope of the cubic spline at the first non-null value (which is '2013-09-29'). The slope of the line extrapolating the trailing nulls is equal to the slope of the cubic spline at the last non-null value (which is '2013-10-04'). This example refers to the InterpolationTable, as defined and populated in the previous example. This query returns [4, 1, 2, 7, 10, 5, -6].

```sql
SELECT date, val, CUBIC_SPLINE_APPROX(val, 'SPLINE_TYPE_NOT_A_KNOT') OVER(
    SERIES TABLE InterpolationTable) FROM InterpolationTable;
```

| **DATE** | **VAL** | **MYRESULT** |
| --- | --- | --- |
| Sep 29, 2013 | ? | ? |
| Sep 30, 2013 | 1 | 1 |
| Oct 1, 2013 | 2 | 2 |
| Oct 2, 2013 | ? | 7 |
| Oct 3, 2013 | 10 | 10 |
| Oct 4, 2013 | 5 | 5 |
| Oct 5, 2013 | ? | ? |

### Linear extrapolation

Extrapolate leading and trailing nulls, besides cubic spline interpolation. The slope of the line extrapolating the leading nulls is equal to the slope of the cubic spline at the first non-null value ('2013-09-29'). The slope of the line extrapolating the trailing nulls is equal to the slope of the cubic spline at the last non-null value ( '2013-10-04'). This example refers to the InterpolationTable as defined and populated in the previous example. This query returns [?, 1, 2, 7, 10, 5, ?].

```sql
SELECT date, val, CUBIC_SPLINE_APPROX(val, 'SPLINE_TYPE_NOT_A_KNOT') OVER(
    SERIES TABLE InterpolationTable) FROM InterpolationTable;
```

| **DATE** | **VAL** | **LINEAR_APPROX(VAL,'EXTRAPOLATION_LINEAR')OVER(SERIES())** |
| --- | --- | --- |
| Sep 29, 2013 | ? | 0 |
| Sep 30, 2013 | 1 | 1 |
| Oct 1, 2013 | 2 | 2 |
| Oct 2, 2013 | ? | 6 |
| Oct 3, 2013 | 10 | 10 |
| Oct 4, 2013 | 5 | 5 |
| Oct 5, 2013 | ? | 0 |

This example performs linear extrapolation on a series.

```sql
SELECT date, val, LINEAR_APPROX(val, 'EXTRAPOLATION_LINEAR') OVER(
    SERIES(SERIES KEY(ts_id) PERIOD FOR SERIES(date)
        EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS ALLOWED))
    FROM InterpolationTable;
```

This example performs linear extrapolation on a series using a series table.

```sql
DROP TABLE InterpolationTable;
CREATE COLUMN TABLE InterpolationTable (ts_id VARCHAR(20), date DAYDATE, val
DOUBLE)
    SERIES(SERIES KEY(ts_id) PERIOD FOR SERIES(date)
    EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS ALLOWED);
SELECT date, val, LINEAR_APPROX(val, 'EXTRAPOLATION_LINEAR') OVER(
    SERIES TABLE InterpolationTable) FROM InterpolationTable;
```

This example performs linear extrapolation on a series using a series table and returns [1, 2, 6, 10].

```sql
DROP TABLE InterpolationTable;
CREATE COLUMN TABLE InterpolationTable
    (TS_ID VARCHAR(20), date DAYDATE, val DOUBLE);
INSERT INTO InterpolationTable VALUES('A','2013-09-30', 1);
INSERT INTO InterpolationTable VALUES('A','2013-10-01', 2);
INSERT INTO InterpolationTable VALUES('A','2013-10-02', null);
INSERT INTO InterpolationTable VALUES('A','2013-10-03', 10);
SELECT date, val, LINEAR_APPROX (val, 'EXTRAPOLATION_LINEAR')
    OVER (PARTITION BY TS_ID ORDER BY date) FROM InterpolationTable;
```

| **DATE** | **VAL** | **LINEAR_APPROX(VAL,'EXTRAPOLATION_LINEAR')OVER(SERIES())** |
| --- | --- | --- |
| Sep 30, 2013 | 1 | 1 |
| Oct 1, 2013 | 2 | 2 |
| Oct 2, 2013 | ? | 6 |
| Oct 3, 2013 | 10 | 10 |

If Value1Argument and Value2Argument are null or not specified, an input of [null, null, 1, null, 3, null, null] returns [-1, 0, 1, 2, 3, 4, 5]. If the input contains only one non-null value, then all entries are replaced with copies of the non-null value. For example, an input of [null, null, 3, null] returns [3, 3, 3, 3].

If Value1Argument is set to 2 and Value2Argument is set to null then, an input of [null, null, 3, 4, 3, null, null] returns [2, 2, 3, 4, 3, 2, 2]. If Value1Argument is set to 5 and Value2Argument is set to null and the input contains only one non-null value, then the higher value of Value1Argument and the non-null value from the input is used. For example, [null, null, 4, null, null] returns [5, 5, 4, 5, 5].

If Value1Argument is set to null and Value2Argument is set to 5, an input of [null, null, 4, 3, 4, null, null] returns [5, 5, 4, 3, 4, 5, 5]. If Value1Argument is set to null and Value2Argument is set to 2 and the input contains only one non-null value, the lower value of Value2Argument and the non-null value from the input is used. For example, [null, null, 4, null, null] returns [2, 2, 4, 2, 2].

If Value1Argument is set to 2 and Value2Argument is set to 5, then an input of [null, null, 4, 3, null, null] returns [5, 5, 4, 3, 2, 2]. If the input contains only one non-null value, the following conditions are checked.

- If Value1Argument is less than or equal to the non-null value, or if the non-null value is less than or equal to Value2Argument, then the non-null value is used.
- If the non-null value is less than Value1Argument, then Value1Argument is used.
- If the non-null value is greater than Value2Argument, then Value2Argument is used. For example, [null, null, 4, null, null] returns [3, 3, 4, 3, 3].

For example, [null, null, 4, null, null] returns [3, 3, 4, 3, 3].

If Value1Argument and Value2Argument are null or not specified, then any leading nulls are replaced by the first non-null value, and any trailing nulls are replaced by the last non-null value. For example, an input of [null, null, 1, 2, null, null] returns [1, 1, 1, 2, 2, 2]. If the input only has one non-null value, then all the null values are replaced with the non-null value.

If Value1Argument is set to 5 and Value2Argument is set to null, then any leading nulls are replaced by Value1Argument, and the trailing nulls are replaced by the last non-null value. For example, an input of [null, null, 1, 2, null, null] returns [5, 5, 1, 2, 2, 2]. If the input only has one non-null value, then the leading nulls are replaced by Value1Argument and the trailing nulls are replaced by the non-null value. For example, an input of [null, null, 3, null] returns [5, 5, 3, 3]. If the input only has null values, then all null values are replaced with Value1Argument.

If Value1Argument is set to null and Value2Argument is set to 5, then any leading nulls are replaced by the first non-null value, and the trailing nulls are replaced by Value2Argument. For example, an input of [null, null, 1, 2, null, null] returns [1, 1, 1, 2, 5, 5]. If the input only has one non-null value, then the leading nulls are replaced by the non-null value and the trailing nulls are replaced by Value2Argument. For example, an input of [null, null, 3, null] returns [3, 3, 3, 5]. If the input only has null values, then all null values are replaced with Value2Argument.

If Value1Argument is set to 3 and Value2Argument is set to 4, any leading nulls are replaced by Value1Argument, and the trailing nulls are replaced by Value2Argument. For example, an input of [null, null, 1, 2, null, null] returns [3, 3, 1, 2, 4, 4]. If the input only has null values, then all null values are replaced with Value2Argument.

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
