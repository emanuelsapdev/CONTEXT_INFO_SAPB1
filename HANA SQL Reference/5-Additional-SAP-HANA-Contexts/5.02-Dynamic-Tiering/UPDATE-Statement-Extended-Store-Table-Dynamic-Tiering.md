# 5.2.38 UPDATE Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1369–1372

Changes the values of the records of an extended store table.

## Syntax

```sql
UPDATE [<top_clause>] <table_name> [<alias_name>]
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

For more information about identifiers, see Introduction in Introduction to SQL [→](../../4-SQL-Reference/4.01-Introduction-to-SQL.md).

#### set_clause

The column names and associated values that are to be set by the update statement.

```sql
<set_clause> ::= SET {<column_name> = <expression>
   | ( <with_clause> <subquery> ) },...
```

For descriptions of expressions, see the Expressions [→](../../4-SQL-Reference/4.06-Expressions.md) section in this guide. For the definitions of `<with_clause>` and `<subquery>`, see SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md). The `<with_clause>` can be used with column names, not with column lists.

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

For more information about predicates, see the Predicates [→](../../4-SQL-Reference/4.07-Predicates/README.md) section in this guide.

#### hint_clause

For more information about hints, see SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md) in this guide.

#### top_clause

Allows you to limit the number of updated records, for example for chunkwise updates.

```sql
<top_clause> ::= TOP <unsigned_integer>
```

`<unsigned_integer>` defines the number of records updated in one chunk. This parameter is not supported for variants of UPDATE statements like UPDATE MERGE DELTA, UPDATE PRELOAD, UPDATE UNLOAD and UPDATE MOVE.

## Permissions

You must have the UPDATE object privilege.

## Description

The UPDATE statement changes the values of the records of an extended store table.

If the WHERE condition is used and is true for a specific row, the update is performed on that row. If the WHERE clause is omitted, the UPDATE command updates all records of a table.

## Examples

You create table T, and insert two rows into it.

```sql
 CREATE COLUMN TABLE T (KEY INT PRIMARY KEY, VAL INT);
INSERT INTO T VALUES (1, 1);
INSERT INTO T VALUES (2, 2);
```

You update the rows of table T if the condition in the WHERE clause is true.

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 2 |

You update all rows of table T because a where clause is not specified as part of the update statement.

```sql
UPDATE T SET VAL = KEY + 10;
```

| KEY | VAL |
| --- | --- |
| 1 | 11 |
| 2 | 12 |

You create table T2, and insert two rows into it.

```sql
 CREATE COLUMN TABLE T2 (KEY INT PRIMARY KEY, VAR INT);
INSERT INTO T2 VALUES (1, 2);
INSERT INTO T2 VALUES (3, 6);
```

You update the values of table T by joining the target table T with table T2.

```sql
UPDATE T SET VAL = T2.VAR FROM T, T2 WHERE T.KEY = T2.KEY;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 2 |

You update a chunk of 100,000 records of the table `testtab` that contain 'XXX' in the `request` column and the value 0 in the `updated` column. For each row processed, the `updated` column is set to 1.

```sql
update top 100000 testtab set updated = 1 where request = 'XXX' and updated = 0
```

You UPDATE a table with an array value construction by enumeration.

```sql
UPDATE T1 SET C1 = ARRAY ( 11, 12, 13, 14 ) WHERE ID = 1
```

You UPDATE a table with an array value construction by query.

```sql
UPDATE T1 SET C1 = ARRAY( SELECT C1 FROM T0 ) WHERE ID = 1
```
