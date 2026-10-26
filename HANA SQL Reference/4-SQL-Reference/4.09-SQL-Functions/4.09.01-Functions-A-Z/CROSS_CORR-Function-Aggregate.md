# 4.9.1.47 CROSS_CORR Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 152–154

Computes all cross-correlation coefficients between two given expressions.

## Syntax

```sql
CROSS_CORR(<expression1>, <expression2>, <maxLag>
    { <series_orderby> | <order_by_clause> } ).{ POSITIVE_LAGS | NEGATIVE_LAGS |
ZERO_LAG }
```

## Syntax Elements

#### expression1 and expression2

Numeric values between which the cross-correlation is calculated.

#### maxLag

The `<maxLag>` parameter must be a positive integer that defines the number of cross-correlation coefficients to be returned.

```sql
<maxLag> ::= INTEGER
```

#### series_orderby

The SERIES clause can only be used with an equidistant series. For more information about the SERIES clause, see the CREATE TABLE statement and the SERIES_GENERATE function.

```sql
<series_orderby> ::= SERIES (<series_period> <series_equidistant_definition>)
```

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

Computes all cross-correlation coefficients between two given expressions.

The result is an array of cross-correlation coefficients of length `<maxLag>`.

If POSITIVE_LAGS is specified, then the cross-correlation coefficients with lags 1`<maxLag>` are returned.

If NEGATIVE_LAGS is specified, then the cross-correlation coefficients with lags -1 `<maxLag>` are returned.

If ZERO_LAG is specified, a single value associated with lag 0 is returned.

This function output can be non-deterministic among tie values.

## Example

### Example 1 - Cross correlation

Execute the cross correlation example below:

```sql
CREATE COLUMN TABLE table1 ( ts_id INTEGER, number1 DOUBLE, number2 DOUBLE );
INSERT INTO table1 VALUES ('1', 1, 2);
INSERT INTO table1 VALUES ('2', 2 ,1);
INSERT INTO table1 VALUES ('3', 1 ,2);
SELECT CROSS_CORR(number1, number2, 10 ORDER BY ts_id) FROM table1;
```

The results are as follows:

| **CROSS_CORR(NUMBER1,NUMBER2,10ORDERBYTS_ID)** |
| --- |
| 1.0, -1.0, 1.0 |

### Example 2 - Cross correlation using a series descriptor

Execute the example below:

```sql
CREATE COLUMN TABLE TSeries( key INTEGER, ts TIMESTAMP, val1 DOUBLE, val2
DOUBLE, PRIMARY KEY(key, ts) )
    SERIES( SERIES KEY (key) EQUIDISTANT INCREMENT BY INTERVAL 1 DAY PERIOD FOR
SERIES(ts) );
INSERT INTO TSeries VALUES (1, '2014-1-1', 1, 3);
INSERT INTO TSeries VALUES (2, '2014-1-3', 2, 4);
INSERT INTO TSeries VALUES (3, '2014-1-4', 4, 2);
INSERT INTO TSeries VALUES (4, '2014-1-5', 3, 1);
SELECT CROSS_CORR(val1, val2, 10 ORDER BY ts) FROM TSeries;
```

The results are as follows:

| **CROSS_CORR(VAL1,VAL2,10ORDERBYTS)** |
| --- |
| -1.0, -0.928571, -0.6, 0.5, -1.0 |

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) AUTO_CORR Function (Aggregate) [→](AUTO_CORR-Function-Aggregate.md) CORR Function (Aggregate) [→](CORR-Function-Aggregate.md) CORR_SPEARMAN Function (Aggregate) [→](CORR_SPEARMAN-Function-Aggregate.md) Expressions [→](../../4.06-Expressions.md) CREATE TABLE Statement (Data Definition) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md)
