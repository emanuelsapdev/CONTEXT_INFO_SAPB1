# 4.9.1.151 RANDOM_PARTITION Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 283–286

Partitions an input set randomly into three disjoint subsets by assigning a set number to each row of the input set.

## Syntax

```sql
RANDOM_PARTITION(<training_set_size>, <validation_set_size>, <test_set_size>,
<seed>) <window_specification>
```

## Syntax Elements

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The three subsets that RANDOM_PARTITION partitions the set into are called **training**, **validation**, and **testing**. The union of these three subsets may not be the complete initial dataset.

`<training_set_size>`, `<validation_set_size>`, and `<test_set_size>` can be numeric values that specify the sizes of the training, validation, and testing sets, respectively. When all three values are less than one, the sizes are expressed as fractions of the total input size. When all three values are greater than or equal to one, they represent the actual number of elements in the different partitions. `<seed>` specifies the seed for the random number generation. When set to zero, the `<seed>` is initialized with the current time.

The set numbers are defined as follows:

| **Set number** | **Set** |
| --- | --- |
| 0 | The value is not assigned to a set |
| 1 | The training set |
| 2 | The validation set |
| 3 | The test set |

Stratified partitions are supported via the PARTITION BY clause.

To generate reproducible partitions by providing a value for the `<seed>`, ensure that the input set is ordered in the same way in each call to the function. The `<seed>` value must be larger than zero to generate reproducible partitions; a value of zero does not create reproducible partitions. Do not use `<seed>` without the ORDER BY clause. The partitions can be non-deterministic among tie values in the `<window_order_by_expression>`.

## Examples

### Stratified partitions

The following example creates stratified partitions (random partitions per station with fractional partition sizes). Since the partition numbers are randomly assigned to the rows, the result might differ from call to call.

```sql
CREATE TABLE weather (station INT, ts DATE, temperature FLOAT);
INSERT INTO weather VALUES (1, '2014-01-01', 0);
INSERT INTO weather VALUES (1, '2014-01-02', 3);
INSERT INTO weather VALUES (1, '2014-01-03', 4.5);
INSERT INTO weather VALUES (1, '2014-01-04', 6);
INSERT INTO weather VALUES (1, '2014-01-05', 6.3);
INSERT INTO weather VALUES (1, '2014-01-06', 5.9);
INSERT INTO weather VALUES (2, '2014-01-01', 1);
INSERT INTO weather VALUES (2, '2014-01-02', 3.4);
INSERT INTO weather VALUES (2, '2014-01-03', 5);
INSERT INTO weather VALUES (2, '2014-01-04', 6.7);
INSERT INTO weather VALUES (2, '2014-01-05', 4.6);
INSERT INTO weather VALUES (2, '2014-01-06', 6.9);

SELECT *, RANDOM_PARTITION(0.5, 0.2, 0.3, 0) OVER (PARTITION BY station ORDER BY
ts) AS part_num FROM weather;
```

| **STATION** | **TS** | **TEMPERATURE** | **PART_NUM** |
| --- | --- | --- | --- |
| 1 | 01.01.2014 | 0.0 | 1 |
| 1 | 02.01.2014 | 3.0 | 1 |
| 1 | 03.01.2014 | 4.5 | 2 |

| 1 | 04.01.2014 | 6.0 |
| --- | --- | --- |

3

| 1 | 05.01.2014 | 6.3 | 1 |
| --- | --- | --- | --- |
| 1 | 06.01.2014 | 5.9 | 3 |

| **STATION** | **TS** | **TEMPERATURE** | **PART_NUM** |
| --- | --- | --- | --- |
| 2 | 01.01.2014 | 1.0 | 1 |
| 2 | 02.01.2014 | 3.4 | 1 |
| 2 | 03.01.2014 | 5.0 | 2 |
| 2 | 04.01.2014 | 6.7 | 3 |
| 2 | 05.01.2014 | 4.9 | 1 |
| 2 | 06.01.2014 | 6.9 | 3 |

### Random partitions with explicit partition sizes

The following example creates random partitions with explicit partition sizes:

```sql
DROP TABLE weather;
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
SELECT *, RANDOM_PARTITION(5, 2, 3, 0) OVER (ORDER BY temperature) AS part_num
FROM weather;
```

| **STATION** | **TS** | **TEMPERATURE** | **PART_NUM** |
| --- | --- | --- | --- |
| 1 | 01.01.2014 | 0 | 0 |
| 2 | 01.01.2014 | 1 | 1 |
| 1 | 02.01.2014 | 3 | 1 |
| 2 | 02.01.2014 | 3.4 | 1 |
| 1 | 03.01.2014 | 4.5 | 1 |
| 2 | 05.01.2014 | 4.6 | 1 |
| 2 | 03.01.2014 | 5 | 2 |
| 1 | 06.01.2014 | 5.9 | 0 |
| 1 | 04.01.2014 | 6 | 2 |
| 1 | 05.01.2014 | 6.3 | 3 |
| 2 | 04.01.2014 | 6.7 | 3 |
| 2 | 06.01.2014 | 6.9 | 3 |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
