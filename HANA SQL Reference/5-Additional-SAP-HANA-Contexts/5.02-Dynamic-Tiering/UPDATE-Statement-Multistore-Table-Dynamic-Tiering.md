# 5.2.39 UPDATE Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1372–1375

Changes the values of the records of a multistore table.

## Syntax

```sql
UPDATE [<top_clause>] <table_name> [<alias_name>] [<partition_restriction>]
<set_clause>  [ WHERE <condition> ] [<hint_clause>]
```

## Syntax Elements

#### table_name

The table name where the UPDATE is to be performed, with optional schema name.

```sql
<table_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### alias_name

An alias that can be used to refer to the table defined by `<table_name>`.

```sql
<alias_name> ::= [AS] <identifier>
```

[For more information about identifiers, see Introduction in Introduction to SQL](../../4-SQL-Reference/4.01-Introduction-to-SQL.md)

#### partition_restriction

For the default (column store) partitions of multistore tables, `<partition_restriction>` specifies the partition in which the target updated rows are located.

```sql
<partition_restriction> ::= PARTITION ( <partition_number> )
<partition_number> ::= <unsigned_integer>
```

If you do not specify a partition restriction, then the database checks all partitions for the update. But if there is partition restriction, only the rows in specified partition are updated.

Functional restrictions:

- An UPDATE statement with a partition restriction is blocked if the following are true:
  1. Partitioning key column update
  2. UNIQUE constraint column update
  3. PRIMARY KEY column update
- Updates that change the updated rows partition are not allowed.
- `<partition_restriction>` is not supported if the partition number in the list contains a partition ID of the extended store.

#### set_clause

The column names and associated values that are to be set by the update statement.

```sql
<set_clause> ::= SET {<column_name> = <expression> | ( <with_clause>
<subquery> ) },...
```

For descriptions of expressions, see Expressions [→](../../4-SQL-Reference/4.06-Expressions.md). For the definitions of `<with_clause>` and `<subquery>`, see SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md). The `<with_clause>` can be used with column names, not with column lists.

#### condition

Specifies the conditions where the command should be performed.

```sql
 WHERE <condition>
<condition> ::= <condition> OR  <condition>
   | <condition> AND <condition>
   | NOT <condition>
   | ( <condition> )
   | <predicate>
```

For more information about predicates, see Predicates [→](../../4-SQL-Reference/4.07-Predicates/README.md).

For multistore tables, UPDATE supports only simple set expressions, and disallows complex expressions. UPDATE on multistore tables allows only simple predicates in the WHERE clause, and disallows subqueries in the WHERE clause.

#### hint_clause

For more information about hints, see SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md).

#### top_clause

Limits the number of updated records.

```sql
<top_clause> ::= TOP <unsigned_integer>
```

For example, for chunkwise updates, `<unsigned_integer>` defines the number of records updated in one chunk. Variants of UPDATE statements like UPDATE MERGE DELTA, UPDATE PRELOAD, UPDATE UNLOAD and UPDATE MOVE do not support this parameter.

## Permissions

You must have the UPDATE object privilege.

## Description

The UPDATE statement changes the values of the records of a table.

If the WHERE condition is used and is true for a specific row, the update is performed on that row. If the WHERE clause is omitted, the UPDATE command updates all records of a table.

You can update non-partitioning columns in a multistore table. You can update aging columns, partition keys, and primary key columns without restriction.

You can use UPDATE to move data from the catalog store to the extended store and back. Any update statement for a column store table works for a multistore table.

## Examples

Create table T, and insert two rows into it.

```sql
 CREATE COLUMN TABLE T (KEY INT PRIMARY KEY, VAL INT)
 PARTITION BY RANGE (KEY) ( USING DEFAULT STORAGE
(PARTITION  '0' <= VALUES < '40') USING EXTENDED STORAGE
(PARTITION '40' <= VALUES < '80') ) ;
 INSERT INTO T VALUES (1, 1);
 INSERT INTO T VALUES (2, 2);
```

Update the rows of table T if the condition in the WHERE clause is true.

```sql
UPDATE T SET VAL = VAL + 1 WHERE KEY = 1;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 2 |

Update all rows of table T because a where clause is not specified as part of the update statement.

```sql
UPDATE T SET VAL = KEY + 10;
```

| KEY | VAL |
| --- | --- |
| 1 | 11 |
| 2 | 12 |

Create table T2, and insert two rows into it.

```sql
 CREATE COLUMN TABLE T2 (KEY INT PRIMARY KEY, VAL INT)
 PARTITION BY RANGE (KEY) ( USING DEFAULT STORAGE
(PARTITION  '0' <= VALUES < '40') USING EXTENDED STORAGE
(PARTITION '40' <= VALUES < '80') ) ;
 INSERT INTO T2 VALUES (1, 2);
 INSERT INTO T2 VALUES (3, 6);
```

Update the values of table T by joining the target table T with table T2.

```sql
UPDATE T SET VAL = T2.VAR FROM T, T2 WHERE T.KEY = T2.KEY;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 2 |

Update a chunk of 100,000 records of the table `testtab` that contain 'XXX' in the `request` column and the value 0 in the `updated` column. For each row processed, the `updated` column is set to 1.

```sql
update top 100000 testtab set updated = 1 where request = 'XXX' and updated = 0
```

Update an aging column.

```sql
update table t1 set c = 10 where t1.temperature = '0000000'
```
