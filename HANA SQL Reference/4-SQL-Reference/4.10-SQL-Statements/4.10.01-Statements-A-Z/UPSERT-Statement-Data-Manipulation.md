# 4.10.1.158 UPSERT Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1120–1124

Updates rows in a table or inserts new rows. This UPSERT and REPLACE statements are synonymous and have similar syntax and purpose.

## Syntax

```sql
UPSERT <table_name> [ <partition_restriction> ] [ <column_list_clause> ]
   {
     <value_list_clause> [ WHERE <condition> | WITH PRIMARY KEY ]
     | <subquery>
   }
```

## Syntax Elements

#### table_name

Specifies the table to update, with the optional schema name.

```sql
<table_name> ::= [ [ <database_name>.]<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

For linked database, `<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

#### column_list_clause

Specifies a list of column identifiers, ordered in the order of values in the `<value_list_clause>` or `<subquery>`.

```sql
<column_list_clause> ::= ( <column_name> [,…] )
<column_name> ::= <identifier>
```

#### partition_restriction

For a partitioned table, `<partition_restriction>` specifies the partition in which the target rows are located.

```sql
<partition_restriction> ::= PARTITION ( <<partition_number> )
<partition_number> ::= <unsigned_integer>
```

If you do not specify a partition restriction, then the database checks all partitions for the update. But if there is a partition restriction, then only the rows in the specified partition are updated. Use the TABLE_PARTITIONS system view to determine the partition number.

The `<partition_restriction>` clause is supported for multistore tables but not extended store tables.

#### value_list_clause

Specifies a list of values, or expressions evaluating to values, to be inserted or updated into the table.

```sql
<value_list_clause> ::= VALUES ( <expression> [,…] )
```

#### WHERE condition

Specifies the conditions where the command should be performed.

```sql
<condition> ::=
 <condition> OR <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>
```

#### WITH PRIMARY KEY

Uses the primary key value in the `<value_list_clause>` to define the row to act upon.

#### subquery

For information on subqueries, see the SELECT statement.

## Description

When this command is used without a subquery, it functions in a similar way to the UPDATE statement. The difference with this command is that when the WHERE clause condition is false it inserts a new record into the table.

When this command is used with a table that has a primary key, the primary key column must be included in the column list. Columns defined with NOT NULL and without a default specification also have to be included in the column list. Columns that are not specified are filled with a default value or NULL.

The UPSERT (or REPLACE) statement with a subquery operates like the INSERT statement. The exception with this command is that, if an existing row in the table has the same primary key value as a new row, the row is updated with the returned record from the subquery. If the table does not have a primary key, then the command functions in an equivalent way to an INSERT statement as an index cannot be used to check for row duplication.

## Example

Create table T.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
```

Insert a new value.

```sql
UPSERT T VALUES (1, 1);
```

| KEY | VAL |
| --- | --- |
| 1 | 1 |

Insert a new value if the condition in the WHERE clause is false or update the current row values if WHERE evaluates to true.

```sql
UPSERT T VALUES (2, 2) WHERE KEY = 2;
```

| KEY | VAL |
| --- | --- |
| 1 | 1 |
| 2 | 2 |

Update the table row where KEY is equal to 1.

```sql
UPSERT T VALUES (1, 9) WHERE KEY = 1;
```

| KEY | VAL |
| --- | --- |

| 1 | 9 |
| --- | --- |
| 2 | 2 |

Use the "WITH PRIMARY KEY" keyword to update the table using the primary key value in the VALUES clause.

```sql
UPSERT T VALUES (1, 8) WITH PRIMARY KEY;
```

| KEY | VAL |
| --- | --- |
| 1 | 8 |
| 2 | 2 |

Insert values using a subquery.

```sql
UPSERT T SELECT KEY + 2, VAL FROM T;
```

| KEY | VAL |
| --- | --- |
| 1 | 8 |
| 2 | 2 |
| 3 | 8 |
| 4 | 2 |

UPSERT a table with an array value construction by enumeration.

```sql
UPSERT T1 VALUES ( 1, ARRAY ( 21, 22, 23, 24 ) ) WHERE ID = 1;
```

UPSERT a table with an array value construction by query.

```sql
UPSERT T1 VALUES ( 1, ARRAY ( SELECT C1 FROM T0 ) ) WHERE ID = 1;
```

UPSERT values into partition 1 of table T1 and then upsert values from table T1 to partition 1 in table T2.

```sql
CREATE COLUMN TABLE T1 (a int, b int) PARTITION BY RANGE (a)
     (PARTITION 0 <= VALUES < 10, PARTITION OTHERS);
CREATE COLUMN TABLE T2 (a int, b int) PARTITION BY RANGE (a)
     (PARTITION 0 <= VALUES < 10, PARTITION OTHERS);
INSERT INTO T1 PARTITION(1) VALUES(1,50);
UPSERT T1 PARTITION(1) VALUES(1,20);
UPSERT T2 PARTITION(1) SELECT * FROM T1;
Select * from T2;
```

| **A** | **B** |
| --- | --- |
| 1 | 20 |

## Related Information

SELECT Statement (Data Manipulation) [→](4.10.01.144-SELECT/README.md) REPLACE Statement (Data Manipulation) [→](REPLACE-Statement-Data-Manipulation.md) UPDATE Statement (Data Manipulation) [→](UPDATE-Statement-Data-Manipulation.md) TABLE_PARTITIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md)
