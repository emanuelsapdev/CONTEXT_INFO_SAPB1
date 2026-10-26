# 4.9.1.155 RECORD_ID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 290–291

Generates an ID for each row of the results.

## Syntax

```sql
RECORD_ID( <table> )
```

## Syntax Elements

#### table

Specifies the column store or row store table to generate row IDs for.

`<t>` should be located in the FROM clause that is syntactically closest, and cannot be a temporary table, derived table, or any other type of subquery. For example, these syntaxes are supported:

```sql
SELECT RECORD_ID(t) FROM t;
SELECT RECORD_ID(tab) FROM t AS tab;
```

However, these syntaxes are not supported:

```sql
SELECT RECORD_ID(v) FROM (SELECT * FROM t) AS v;
SELECT a, RECORD_ID(st) FROM (SELECT * FROM t) AS st;
```

## Description

Returns a result set with a unique BIGINT value for each row of the results. These values remain valid for the current transaction.

## Examples

The following example shows the use of the RECORD_ID function to select a value from a specified row ID:

```sql
CREATE COLUMN TABLE T1 (column1 INT);
INSERT INTO T1 VALUES (5);
INSERT INTO T1 VALUES (10);
SELECT RECORD_ID(T1) AS RECORD_ID FROM T1;
```

The SELECT query returns the following result:

| **RECORD_ID** |
| --- |
| 1 |
| 2 |

This SELECT query returns the following result:

```sql
SELECT * FROM T1 WHERE RECORD_ID(T1) = 2;
```

| **COLUMN1** |
| --- |
| 10 |
