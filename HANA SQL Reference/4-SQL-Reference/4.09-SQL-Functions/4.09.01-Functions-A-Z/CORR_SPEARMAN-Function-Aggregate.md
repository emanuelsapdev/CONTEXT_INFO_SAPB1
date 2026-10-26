# 4.9.1.42 CORR_SPEARMAN Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 143–148

Returns the Spearman's rank correlation coefficient of the values found in the corresponding rows of two columns. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
CORR_SPEARMAN(<column1>, <column2>)
```

### Window function:

```sql
CORR_SPEARMAN(<column1>, <column2>) <window_specification>
```

## Syntax Elements

#### column1 and column2

Specifies the columns providing the input data for the correlation.

The values of `<column1>` and `<column2>` can contain number or character types.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Returns the Spearman's rank correlation coefficient of the values found in the corresponding rows of `<column1>` and `<column2>`.

Although this function is grouped with the aggregate functions, its optional OVER clause positions it as a windows function as well.

The result ranges from -1 to 1, depending on the correlation, or NULL if a correlation could not be computed.

The result can return NULL for one of the following reasons:

- Less than two value pairs are correlated after NULLs have been removed
- There is zero variance in at least one of the two columns

Whenever a NULL value is found then both the NULL value and the corresponding value of the other input column are ignored.

## Examples

The example below returns `-1`.

```sql
CREATE COLUMN TABLE A (date DAYDATE, val INT);
INSERT INTO A VALUES ('2014-10-01', 100);
INSERT INTO A VALUES ('2014-10-02', 200);
INSERT INTO A VALUES ('2014-10-03', 300);
CREATE COLUMN TABLE B (date DAYDATE, val INT);
INSERT INTO B VALUES ('2014-10-01', 300);
INSERT INTO B VALUES ('2014-10-02', 200);
INSERT INTO B VALUES ('2014-10-03', 100);
SELECT CORR_SPEARMAN(A.val, B.val) "corr" FROM A, B WHERE A.date = B.date;
```

The examples below assume that the correlation table has been created with the following values:

```sql
CREATE COLUMN TABLE correlationSpearmanTable (
    ts_id VARCHAR(20),
    date DAYDATE,
    value1 DOUBLE,
    value2 DOUBLE);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-01', 34.345, 45.345);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-02', 27.145, 28.893);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-02', 48.312, 28.865);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-03', 94.213, 58.854);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-03', 16.567, 28.231);
INSERT INTO correlationSpearmanTable VALUES ('A', '2014-10-03', 38.894, 94.378);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-04', 45.643, 76.987);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-04', 53.345, 50.893);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-04', 66.342, 48.342);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-04', 76.432, 37.234);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-05', 88.432, 23.242);
INSERT INTO correlationSpearmanTable VALUES ('B', '2014-10-05', 93.234, 13.132);
```

1. Execute the aggregate function example below:

```sql
SELECT ts_id, CORR_spearman(value1, value2) FROM correlationSpearmanTable
GROUP BY ts_id;
```

The results are as follows:

| **TS_ID** | **CORR_SPEARMAN(VALUE1,VALUE2)** |
| --- | --- |
| A | 0.542857 |
| B | -1 |

2. Execute the window function below:

```sql
SELECT ts_id, CORR_spearman(value1, value2) OVER (PARTITION BY ts_id) FROM
correlationSpearmanTable;
```

The results are as follows:

| **TS_ID** | **CORR_SPEARMAN(VALUE1,VALUE2)OVER(PARTITIONBYTS_ID)** |
| --- | --- |
| A | 0.542857 |
| A | 0.542857 |
| A | 0.542857 |
| A | 0.542857 |
| A | 0.542857 |
| A | 0.542857 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |

3. Execute the sliding window example below:

```sql
SELECT ts_id, CORR_spearman(value1, value2) OVER (PARTITION BY ts_id ORDER BY
date) FROM correlationSpearmanTable ORDER BY ts_id;
```

The results are as follows:

| **TS_ID** | **CORR_SPEARMAN(VALUE1,VALUE2)OVER(PARTITIONBYTS_IDORDERBYDATE)** |
| --- | --- |
| A | ? |
| A | -0.5 |
| A | -0.5 |
| A | 0.5428571428571428 |
| A | 0.5428571428571428 |
| A | 0.5428571428571428 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |

4. Execute the ROWS BETWEEN example below:

```sql
SELECT ts_id, CORR_spearman(value1, value2) OVER (PARTITION BY ts_id ORDER BY
date
    ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) from
correlationSpearmanTable;
```

The results are as follows:

| **TS_ID** | **CORR_SPEARMAN(VALUE1,VALUE2)OVER(PARTITIONBYTS_IDORDERBYDATEROWS)** |
| --- | --- |
| A | ? |
| A | 1 |
| A | -0.5 |
| A | 0.4 |
| A | 0.7 |
| A | 0.5428571428571428 |
| B | ? |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |

5. Execute the group example below:

```sql
SELECT ts_id, CORR_spearman(value1, value2) OVER (PARTITION BY ts_id ORDER BY
date GROUPS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) FROM
correlationSpearmanTable;
```

The results are as follows:

| **TS_ID** | **CORR_SPEARMAN(VALUE1,VALUE2)OVER(PARTITIONBYTS_IDORDERBYDATEGROUPS)** |
| --- | --- |
| A | ? |
| A | -0.5 |
| A | -0.5 |
| A | 0.5428571428571428 |
| A | 0.5428571428571428 |
| A | 0.5428571428571428 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |
| B | -1 |

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) AUTO_CORR Function (Aggregate) [→](AUTO_CORR-Function-Aggregate.md) CORR Function (Aggregate) [→](CORR-Function-Aggregate.md) CROSS_CORR Function (Aggregate) [→](CROSS_CORR-Function-Aggregate.md)
