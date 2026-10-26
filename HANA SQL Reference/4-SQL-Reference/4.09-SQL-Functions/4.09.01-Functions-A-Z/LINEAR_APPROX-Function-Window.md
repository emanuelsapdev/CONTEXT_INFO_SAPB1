# 4.9.1.112 LINEAR_APPROX Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 234–238

Operates on an entire series to produce a new series that replaces missing values by interpolating between adjacent non-NULL values and extrapolating any leading or trailing null values.

## Syntax

```sql
LINEAR_APPROX(<expression> [, <ModeArgument> [, <Value1Argument> [,
    <Value2Argument>]]]) OVER ({ SERIES TABLE <table_schema>
[<window_partition_by_clause>]
    [<window_order_by_clause>] | SERIES(...) [<window_partition_by_clause>]
    [<window_order_by_clause>] | [<window_partition_by_clause>]
<window_order_by_clause>})
<expression> ::= <identifier>
```

## Syntax Elements

#### expression

This parameter specifies the input data column.

#### ModeArgument

This parameter defines the applied extrapolation mode. The table below lists the possible values for `<ModeArgument>`.

```sql
<ModeArgument> ::= EXTRAPOLATION_NONE
    | EXTRAPOLATION_LINEAR
    | EXTRAPOLATION_CONSTANT
```

| **Mode** | **Description** |
| --- | --- |
| EXTRAPOLATION_NONE | Prevents the extrapolation of leading and trailing nulls. Interpolation is performed on the values in the middle.<br>Default value if `<ModeArgument>` is omitted.<br>You do not need to specify the `<Value1Argument>` and `<Value2Argument>` parameters when using this mode.<br>For example, an input of [null, null, 1, 2, null, null, 5, null, null] returns [null, null, 1, 2, 3, 4, 5, null, null]. |
| EXTRAPOLATION_LINEAR | Performs linear extrapolation where `<Value1Argument>` is the minimum value and `<Value2Argument>` is the maximum value.<br>During the extrapolation of leading and trailing nulls, this function checks that the extrapolation results are within |
|   | range of the minimum and maximum values; otherwise, values are replaced by the minimum or maximum value, whichever is appropriate.<br>An exception is thrown if `<Value1Argument>` is greater than `<Value2Argument>`. |
| EXTRAPOLATION_CONSTANT | Performs linear extrapolation where leading and trailing nulls values are replaced by the values specified by the `<Value1Argument>` and `<Value2Argument>` parameters, respectively.<br>When `<Value1Argument>` is not specified or null, the first non-null value is used to replace leading null values. When `<Value2Argument>` is not specified or null, the last non-null is used to replace trailing null values. |

Linear interpolation can be applied to all number types if they can be cast into a long double type, such as INT, LONG, DOUBLE, or FLOAT.

#### Value1Argument and Value2Argument

These parameters define arguments for the extrapolation and can be any numeric type.

```sql
<Value1Argument> ::= <identifier>
<Value2Argument> ::= <identifier>
```

#### table_schema

```sql
<table_schema> ::= [<schema_name>.]<table_name>
<schema_name> ::= <unicode_name>
<table_name> ::= <identifier>
```

`<table_schema>` must be a base table name and not a correlation name.

#### window_order_by_clause

Determines the sort order. This expression must not contain any NULL values or duplicates. See the syntax of this clause located in the Window Functions topic.

## Description

Operates on an entire series to produce a new series that replaces missing values by interpolating between adjacent non-NULL values and extrapolating any leading or trailing null values.

When using the SERIES TABLE syntax, the properties of the series table are used to determine the partitioning and ordering of rows before linear approximation is performed.

When using this function, the input is assumed to be equidistant. The SERIES definition must be equidistant.

When only null values are contained in the input, only null values appear in the output unless the null values are replaced by an extrapolation via the EXTRAPOLATION_CONSTANT mode.

When using the SERIES syntax, this function uses the properties in the following table to perform linear approximation.

| **Property** | **Description** |
| --- | --- |
| NON-EQUIDISTANT | An error occurs if the series is non-equidistant. |
| MISSING ELEMENTS ALLOWED | When specified, there must be exactly one ORDER BY column that is compatible with the type of the series period column and the INCREMENT BY value. |
| PARTITION BY | If not specified, the SERIES KEY property of the SERIES syntax is used to construct the default PARTITION BY. |
| ORDER BY | If not specified, the first PERIOD column is added as an ORDER BY. |

Other SERIES properties, such as MINVALUE and MAXVALUE, are ignored.

## Examples

### Linear approximation without a series definition

If the SERIES definition were not specified in the example above, then the result would have been different. For the same SparseApproxTable, as populated above, the example below does not specify a series. The example below returns [-1, 0, 1, 2, 3, 4, 5, 6].

```sql
SELECT LINEAR_APPROX(val, 'EXTRAPOLATION_LINEAR') OVER (PARTITION BY ts_id ORDER
BY DATE) AS approximated_value
 FROM "SparseApproxTable";
```

In the example query above, the series is assumed to be dense and equidistant, so the date column is not taken into consideration when calculating the approximations.

### Linear approximation of sparse series data

In the example below, the INCREMENT BY INTERVAL is set to 1 MONTH, meaning that at most one row is expected for each month. Apart from the null values, values are missing for several months in the table. The LINEAR_APPROX function always replaces the null values and does not insert new lines for missing values. However, if the SERIES definition is specified in the SELECT statement, then LINEAR_APPROX considers the missing months when calculating the slope between two non-null values.

```sql
CREATE COLUMN TABLE "SparseApproxTable" (ts_id VARCHAR(20), date DAYDATE, val
DOUBLE);
INSERT INTO "SparseApproxTable" VALUES('A','2013-11-01', null);
INSERT INTO "SparseApproxTable" VALUES('A','2014-01-01', null);
INSERT INTO "SparseApproxTable" VALUES('A','2014-02-05', 2);
INSERT INTO "SparseApproxTable" VALUES('A','2014-03-07', null);
INSERT INTO "SparseApproxTable" VALUES('A','2014-05-01', 5);
INSERT INTO "SparseApproxTable" VALUES('A','2014-07-27', 7);
INSERT INTO "SparseApproxTable" VALUES('A','2014-12-07', null);
INSERT INTO "SparseApproxTable" VALUES('A','2015-02-07', null);
SELECT LINEAR_APPROX(val, 'EXTRAPOLATION_LINEAR') OVER (SERIES (
    SERIES KEY(ts_id) EQUIDISTANT INCREMENT BY INTERVAL 1 MONTH
    MISSING ELEMENTS ALLOWED PERIOD FOR SERIES(date))
  PARTITION BY ts_id) AS approximated_value
 FROM "SparseApproxTable";
```

| **APPROXIMATED_VALUE** |   |   |
| --- | --- | --- |
| -1 |   |   |
| 1 |   |   |
| 2 |   |   |
| 3 |   |   |
| 5 |   |   |
| 7 |   |   |
| 9.666666666666666 |   |   |
| 11 |   |   |
| **Linear approximation of series data**<br> `CREATE COLUMN TABLE "InterpolationTable" (TS_ID VARCHAR(20), date DAYDATE, valDOUBLE); INSERT INTO "InterpolationTable"INSERT INTO "InterpolationTable"INSERT INTO "InterpolationTable"INSERT INTO "InterpolationTable"SELECT date, val, LINEAR_APPROX (val, 'EXTRAPOLATION_LINEAR') OVER (PARTITION BY TS_ID ORDER BYdate) AS LINEAR_APPROX FROM "InterpolationTable";`<br>**DATE** | `VALUES('A','2013-09-30', 1); VALUES('A','2013-10-01', 2); VALUES('A','2013-10-02', null); VALUES('A','2013-10-03', 10);`<br>**VAL** | **MYRESULT** |
| Sep 30, 2013 | 1 | 1 |
| Oct 1, 2013 | 2 | 2 |
| Oct 2, 2013 | ? | 6 |
| Oct 3, 2013 | 10 | 10 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
