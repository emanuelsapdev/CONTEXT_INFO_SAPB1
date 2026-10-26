# 4.10.1.127 MERGE INTO Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 995–1000

Merges data into an existing column store table.

## Syntax

```sql
MERGE INTO <target_table> [ <partition_restriction> ] [ [ AS ] <alias> ]
 USING <table_reference>
 ON <search_condition> <merge_operation_specification>
```

## Syntax Elements

#### target_table

Specifies the target table (identifier) on which to perform the merge operation.

#### partition_restriction

For a partitioned table, `<partition_restriction>` specifies the partition number in which the target rows are located.

```sql
<partition_restriction> ::= PARTITION ( <partition_number> )
<partition_number> ::= <unsigned_integer>
```

If you do not specify a partition restriction, then the database checks all partitions for the merge. But if there is a partition restriction, then only the rows in the specified partition are merged. Use the TABLE_PARTITIONS system view to determine the partition number.

The `<partition_restriction>` clause is supported for multistore tables but not extended store tables.

#### AS alias

Specifies the alias to be used to refer to the table defined by `<target_table>`.

#### USING table_reference

Specifies the source (identifier) of the data to be updated or inserted.

#### search_condition

Specifies the criteria to use for matching values between `<table_reference>` and `<target_table>`.

#### merge_operation_specification

Specifies merge operations to perform on `<table_reference>`.

```sql
<merge_operation_specification> ::=
 { <when_matched_clause>
 | <when_not_matched_clause>
 | <when_matched_clause> <when_not_matched_clause> }
```

`<when_matched_clause>` must precede `<when_not_matched_clause>` if you specify both; otherwise, an error is returned.

##### when_matched_clause

Specifies the update to perform when values match.

```sql
<when_matched_clause> ::=
 WHEN MATCHED [ AND <search_condition> ] THEN <when_matched_specification>
<when_matched_specification> ::=
 <update_specification>
 | <delete_specification>
<update_specification> ::= UPDATE SET <set_clause_list>
<delete_specification> ::= DELETE
```

##### when_not_matched_clause

Specifies the insert to perform when values do not match.

```sql
<when_not_matched_clause> ::=
 WHEN NOT MATCHED [ AND <search_condition> ] THEN
<when_not_matched_specification>
<when_not_matched_specification> ::=
 INSERT [ ( <insert_column_list> ) ] VALUES <insert_value_list>
<insert_value_list> ::=
 ( <insert_value_element> [ {, <insert_value_element> } … ] )
<insert_value_element> ::=
 <value_expression>
 | <contextually_typed_value_specification>
```

## Description

A MERGE INTO statement conditionally updates the rows of a table and/or inserts new rows into a table. The MERGE INTO statement differs from the REPLACE statement in the following ways:

- You must specify a data source.
- You can omit the update or the insert specifications.

MULTIDRAG

When you specify the WHEN MATCHED clause, a row must satisfy the join condition to be updated or deleted. If you specify the optional AND `<search_condition>` THEN … clause, then a row must match both the join condition and the `<search_condition>` to be updated or deleted.

When you specify the WHEN NOT MATCHED clause, a row must not satisfy the join condition to be updated or deleted. If you specify the optional AND `<search condition>` THEN INSERT … clause, then a row must not satisfy the join condition but match the search condition to be inserted.

The existing SAP HANA `<update_from>` syntax can also be replaced by the MERGE INTO statement by omitting the MERGE WHEN NOT MATCHED clause.

On SAP HANA systems with dynamic tiering, the MERGE INTO statement is fully supported for multistore tables. It is not, however, supported in dynamic tiering extended store tables.

## Examples

The following example shows a simple merge operation:

```sql
CREATE SCHEMA "my_schema";
DROP TABLE "my_schema".t1;
DROP TABLE "my_schema".t2;
CREATE ROW TABLE "my_schema".t1 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t1 VALUES(1,1);
CREATE ROW TABLE "my_schema".t2 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t2 VALUES(1,2);
INSERT INTO "my_schema".t2 VALUES(2,3);
MERGE INTO "my_schema".t1 USING "my_schema".t2 ON "my_schema".t1.a =
"my_schema".t2.a
 WHEN MATCHED THEN UPDATE SET "my_schema".t1.b = "my_schema".t2.b
 WHEN NOT MATCHED THEN INSERT VALUES("my_schema".t2.a, "my_schema".t2.b);
SELECT * FROM "my_schema".t1;
```

| **A** | **B** |
| --- | --- |
| 1 | 2 |
| 2 | 3 |

The following merge example is equivalent to executing `UPDATE t1 FROM t1,t2 SET b = t2.b WHERE t1.a = t2.a;`

```sql
CREATE SCHEMA "my_schema";
DROP TABLE "my_schema".t1;
DROP TABLE "my_schema".t2;
CREATE ROW TABLE "my_schema".t1 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t1 VALUES(1,1);
CREATE ROW TABLE "my_schema".t2 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t2 VALUES(1,2);
INSERT INTO "my_schema".t2 VALUES(2,3);
MERGE INTO "my_schema".t1 USING "my_schema".t2 ON "my_schema".t1.a =
"my_schema".t2.a
 WHEN MATCHED THEN UPDATE SET t1.b = "my_schema".t2.b;
SELECT * FROM "my_schema".t1;
```

| **A** | **B** |
| --- | --- |
| 1 | 2 |

The following example only inserts values:

```sql
CREATE SCHEMA "my_schema";
DROP TABLE "my_schema".t1;
DROP TABLE "my_schema".t2;
CREATE ROW TABLE "my_schema"t1 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t1 VALUES(1,1);
CREATE ROW TABLE "my_schema".t2 (a INTEGER, b INTEGER);
INSERT INTO "my_schema".t2 VALUES(1,2);
INSERT INTO "my_schema".t2 VALUES(2,3);
MERGE INTO "my_schema".t1 USING "my_schema".t2 ON "my_schema".t1.a =
"my_schema".t2.a
 WHEN NOT MATCHED THEN INSERT VALUES("my_schema".t2.a, "my_schema".t2.b);
SELECT * FROM "my_schema".t1;
```

| **A** | **B** |
| --- | --- |
| 1 | 1 |
| 2 | 3 |

The following example deletes matched rows and returns an empty result:

```sql
CREATE ROW TABLE T1 (A INTEGER, B INTEGER);
INSERT INTO T1 VALUES (1,0);
INSERT INTO T1 VALUES (2,0);
CREATE ROW TABLE T2 (A INTEGER, B INTEGER);
INSERT INTO T2 VALUES (1,1);
INSERT INTO T2 VALUES (2,2);
INSERT INTO T2 VALUES (3,3);
INSERT INTO T2 VALUES (4,4);
MERGE INTO T1 USING T2 ON T1.A = T2.A
 WHEN MATCHED THEN DELETE;
SELECT * FROM T1;
```

The following example has search conditions applied and returns the table below:

```sql
CREATE COLUMN TABLE T1 (A INTEGER, B INTEGER);
INSERT INTO T1 VALUES (1,0);
INSERT INTO T1 VALUES (2,0);
CREATE COLUMN TABLE T2 (A INTEGER, B INTEGER);
INSERT INTO T2 VALUES (1,1);
INSERT INTO T2 VALUES (2,2);
INSERT INTO T2 VALUES (3,3);
INSERT INTO T2 VALUES (4,4);
MERGE INTO T1 USING T2 ON T1.A = T2.A
 WHEN MATCHED AND T1.A > 1 THEN UPDATE SET B = T2.B
 WHEN NOT MATCHED AND T2.A > 3 THEN INSERT VALUES (T2.A, T2.B);
SELECT * FROM T1;
```

| **A** | **B** |
| --- | --- |
| 1 | 0 |
| 2 | 2 |
| 4 | 4 |

The following example inserts data into specific partitions in tables T1 and T2 and then merges data matched data in table T2 into partition 1 on table T1:

```sql
CREATE COLUMN TABLE T1 (a INT, b INT) PARTITION BY RANGE(a) (PARTITION 0 <=
VALUES < 10, PARTITION OTHERS);
CREATE COLUMN TABLE T2 (a INT, b INT) PARTITION BY RANGE(a) (PARTITION 0 <=
VALUES < 10, PARTITION OTHERS);
INSERT INTO T1 PARTITION(1) VALUES(1, 1);
INSERT INTO T1 PARTITION(2) VALUES(10, 1);
INSERT INTO T2 PARTITION(2) VALUES(10, 1);
MERGE INTO T1 PARTITION(1) USING T2 ON T1.b = T2.b
    WHEN MATCHED THEN UPDATE SET T1.b = 2
    WHEN NOT MATCHED THEN INSERT VALUES (10, 1)
SELECT * from T1;
```

| **A** | **B** |
| --- | --- |
| 1 | 2 |
| 10 | 1 |

## Related Information

[TABLE_PARTITIONS System View](../../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md)
