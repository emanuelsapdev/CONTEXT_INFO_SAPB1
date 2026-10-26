# 4.9.1.41 CORR Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 140–143

Computes the Pearson product momentum correlation coefficient between two columns. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
CORR(<column1>, <column2>)
```

### Window function:

```sql
CORR(<column1>, <column2>) <window_specification>
```

## Syntax Elements

#### column1 and column2

Specifies the columns providing the input data for the correlation.

The values of `<column1>` and `<column2>` can be of any numeric type.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Computes the Pearson product momentum correlation coefficient between two columns.

The result ranges from -1 to 1, depending on the correlation, or NULL if a correlation cannot be computed.

The result can return NULL for one of the following reasons:

- Less than two value pairs are correlated after NULLs have been removed
- There is zero variance in at least one of the two columns

## Examples

The examples below assume that a correlation table has been created with the following values:

```sql
CREATE COLUMN TABLE correlationTable (
    ts_id VARCHAR(20),
    DATE DAYDATE,
    value1 DOUBLE,
    value2 DOUBLE);
INSERT INTO correlationTable VALUES ('A', '2014-10-01', 1, 1);
INSERT INTO correlationTable VALUES ('A', '2014-10-02', 2, 2);
INSERT INTO correlationTable VALUES ('A', '2014-10-04', 3, 3);
INSERT INTO correlationTable VALUES ('B', '2014-10-07', 1, 3);
INSERT INTO correlationTable VALUES ('B', '2014-10-11', 2, 2);
INSERT INTO correlationTable VALUES ('B', '2014-10-21', 3, 1);
```

1. The following aggregate function example returns the correlation between the `ts_id` column and the columns `value1` and `value2`.

```sql
SELECT ts_id, CORR(value1, value2) FROM correlationTable GROUP BY ts_id;
```

The results are as follows:

| **TS_ID** | **CORR(VALUE1, VALUE2)** |
| --- | --- |
| A | 1 |
| B | -1 |

2. The following WHERE clause example returns the correlation between the `ts_id` column and the columns `value1` and `value2` only for rows where `ts_id` equals `A`.

```sql
SELECT ts_id, CORR(value1, value2) FROM correlationTable
    WHERE ts_id='A' GROUP BY ts_id;
```

The results are as follows:

| **TS_ID** | **CORR(VALUE1, VALUE2)** |
| --- | --- |
| A | 1 |

3. The example below uses a window function.

```sql
SELECT ts_id, CORR(value1, value2) OVER (PARTITION BY ts_id) FROM
correlationTable;
```

The results are as follows:

| **TS_ID** | **CORR(VALUE1, VALUE2)OVER(PARTITIONBYTS_ID)** |
| --- | --- |
| A | 1 |

4. The example below uses a sliding window function.

```sql
SELECT ts_id, CORR(value1, value2) OVER (PARTITION BY ts_id ORDER BY date)
    FROM correlationTable ORDER BY ts_id;
```

The results are as follows:

| **TS_ID** | **CORR(VALUE1, VALUE2)OVER(PARTITIONBYTS_IDORDERBYDATE)** |
| --- | --- |
| A | ? |
| A | 0.9999999999999998 |
| A | 0.9999999999999998 |
| B | ? |
| B | -0.9999999999999998 |
| B | -0.9999999999999998 |

5. The example below uses a ROWS BETWEEN clause.

```sql
SELECT ts_id, CORR(value1, value2) OVER (PARTITION BY ts_id ORDER BY date
    ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) from correlationTable;
```

The results are as follows:

| **TS_ID** | **CORR(VALUE1, VALUE2)OVER(PARTITIONBYTS_IDORDERBYDATEROWS)** |
| --- | --- |
| A | ? |
| A | 0.9999999999999998 |
| A | 0.9999999999999998 |
| B | ? |
| B | -0.9999999999999998 |
| B | -0.9999999999999998 |

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) AUTO_CORR Function (Aggregate) [→](AUTO_CORR-Function-Aggregate.md)

CORR_SPEARMAN Function (Aggregate) [→](CORR_SPEARMAN-Function-Aggregate.md) CROSS_CORR Function (Aggregate) [→](CROSS_CORR-Function-Aggregate.md)
