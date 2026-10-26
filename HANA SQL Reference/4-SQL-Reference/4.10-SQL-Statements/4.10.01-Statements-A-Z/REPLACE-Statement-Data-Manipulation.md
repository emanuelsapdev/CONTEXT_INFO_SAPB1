# 4.10.1.139 REPLACE Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1028–1030

Updates rows in a table or inserts new rows. This UPSERT and REPLACE statements are synonymous and have identical syntax and purpose.

## Syntax

```sql
REPLACE <table_name> [ <column_list_clause> ]
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

## Examples

See the UPSERT statement for examples of how to update rows using the REPLACE/UPSERT statements.

## Related Information

SELECT Statement (Data Manipulation) [→](4.10.01.144-SELECT/README.md) UPSERT Statement (Data Manipulation) [→](UPSERT-Statement-Data-Manipulation.md) UPDATE Statement (Data Manipulation) [→](UPDATE-Statement-Data-Manipulation.md) Expressions [→](../../4.06-Expressions.md) Predicates [→](../../4.07-Predicates/README.md) EXPLAIN_PLAN_TABLE System View [→](../../../6-System-Views-Reference/6.01-System-Views/EXPLAIN_PLAN_TABLE-System-View.md) M_SQL_PLAN_CACHE System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE-System-View.md)
