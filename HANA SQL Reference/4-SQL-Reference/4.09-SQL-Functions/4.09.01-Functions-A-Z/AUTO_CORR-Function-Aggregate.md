# 4.9.1.19 AUTO_CORR Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 104–106

Computes all autocorrelation coefficients for a given input expression and returns an array of values.

## Syntax

```sql
AUTO_CORR( <expression>, <maxTimeLag> { <series_order_by_clause> |
<order_by_clause> })
```

## Syntax Elements

**expression** Specifies the input expression. `<expression>` values can be of any numeric type. **maxTimeLag** The time frame size is limited by the maxTimeLag parameter. This parameter must be a positive integer. The result size is the minimum of maxTimeLag and column size - 2 for dense series data.

#### series_orderby

`<series_orderby>` can only be used with an equidistant series.

```sql
<series_orderby> ::= SERIES( <series_period> <series_equidistant_definition> )
```

The use of SQLScript variables in this clause is not supported. The series \* must not contain missing elements. For more information about this clause, see the SERIES_GENERATE function.

#### order_by_clause

Specifies the sort order of the input rows.

```sql
<order_by_clause> ::= ORDER BY <order_by_expression> [, <order_by_expression>
[,...] ]
<order_by_expression> ::=
 <column_name> [ ASC | DESC ] [ NULLS FIRST | NULLS LAST ]
[ <collate_clause> ]
 | <column_position> [ ASC | DESC ] [ NULLS FIRST | NULLS LAST ]
[ <collate_clause> ]
<collate_clause> ::= COLLATE <collation_name>
```

`<collate_clause>` specifies the collation to use for ordering values in the results. `<collate_clause>` can only be used on columns defined as NVARCHAR or VARCHAR.`<collation_name>` is one of the supported collation names listed in the COLLATIONS system view.

## Description

Computes all autocorrelation coefficients for a given input expression and returns an array of values.

Pairs that contain at least one null are removed. Even though AUTO_CORR can handle null input values, it is highly recommended to replace null values first (e.g. by using LINEAR_APPROX), which allows for much faster processing.

The output is empty if there are fewer than two rows.

## Examples

The example below shows autocorrelation of dense series data and returns `[0.285714,-0.351351,-0.5625,-0.25,1,1,1,1]`.

```sql
CREATE COLUMN TABLE correlationTable (TS_ID VARCHAR(10), DATE DAYDATE, VALUE
DOUBLE);
INSERT INTO correlationTable VALUES ('A', '2014-10-01', 1);
INSERT INTO correlationTable VALUES ('A', '2014-10-02', 2);
INSERT INTO correlationTable VALUES ('A', '2014-10-03', 3);
INSERT INTO correlationTable VALUES ('A', '2014-10-04', 4);
INSERT INTO correlationTable VALUES ('A', '2014-10-05', 5);
INSERT INTO correlationTable VALUES ('A', '2014-10-06', 1);
INSERT INTO correlationTable VALUES ('A', '2014-10-07', 2);
INSERT INTO correlationTable VALUES ('A', '2014-10-08', 3);
INSERT INTO correlationTable VALUES ('A', '2014-10-09', 4);
INSERT INTO correlationTable VALUES ('A', '2014-10-10', 5);
SELECT TS_ID, AUTO_CORR(VALUE, 8 SERIES (PERIOD FOR SERIES(DATE)
        EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS NOT ALLOWED))
    FROM correlationTable
    GROUP BY TS_ID ORDER BY TS_ID;
```

The example below shows autocorrelation of sparse series data without considering missing entries, and returns `[1,1,1,1,1]`.

```sql
CREATE COLUMN TABLE correlationTable (ts_id VARCHAR(20), date DAYDATE, val
DOUBLE);
INSERT INTO correlationTable VALUES ('A', '2014-10-01', 1);
INSERT INTO correlationTable VALUES ('A', '2014-10-02', 2);
INSERT INTO correlationTable VALUES ('A', '2014-10-04', 3);
INSERT INTO correlationTable VALUES ('A', '2014-10-07', 4);
INSERT INTO correlationTable VALUES ('A', '2014-10-11', 5);
INSERT INTO correlationTable VALUES ('A', '2014-10-21', 6);
INSERT INTO correlationTable VALUES ('A', '2014-10-22', 7);
SELECT ts_id, AUTO_CORR(val, 999 SERIES (PERIOD FOR SERIES(DATE)
        EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS NOT ALLOWED))
    FROM correlationTable
    GROUP BY ts_id ORDER BY ts_id;
```

The correlationTable has missing entries, such as '2014-10-03', but the WITHIN GROUP clause considers the series to be equidistant with one day intervals, where missing elements are not allowed.

Since the series data is assumed to be dense, the autocorrelation of the data set [1..7] is calculated.

The example below shows autocorrelation of sparse series data considering the missing entries, and returns `[1.0, null, 1.0, null, null, null, null, null, null, * 1.0, null, null, null, null, null, null, null, null, null, 1.0]`.

```sql
CREATE COLUMN TABLE correlationTable (ts_id VARCHAR(20), date DAYDATE, val
DOUBLE);
INSERT INTO correlationTable VALUES ('A', '2014-10-01', 1);
INSERT INTO correlationTable VALUES ('A', '2014-10-02', 2);
INSERT INTO correlationTable VALUES ('A', '2014-10-04', 3);
INSERT INTO correlationTable VALUES ('A', '2014-10-07', 4);
INSERT INTO correlationTable VALUES ('A', '2014-10-11', 5);
INSERT INTO correlationTable VALUES ('A', '2014-10-21', 6);
INSERT INTO correlationTable VALUES ('A', '2014-10-22', 7);
SELECT ts_id, AUTO_CORR(val, 999 SERIES (PERIOD FOR SERIES(DATE)
        EQUIDISTANT INCREMENT BY INTERVAL 1 DAY MISSING ELEMENTS ALLOWED))
    FROM correlationTable
    GROUP BY ts_id ORDER BY ts_id;
```

Autocorrelation works as if there were nulls instead of the missing elements in the column.

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) CORR Function (Aggregate) [→](CORR-Function-Aggregate.md) CORR_SPEARMAN Function (Aggregate) [→](CORR_SPEARMAN-Function-Aggregate.md) CROSS_CORR Function (Aggregate) [→](CROSS_CORR-Function-Aggregate.md) Expressions [→](../../4.06-Expressions.md)
