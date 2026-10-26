# 4.10.1.134 RENAME COLUMN Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1021–1022

Changes the name of a column.

## Syntax

```sql
RENAME COLUMN <table_name>.<old_column_name> TO <new_column_name>
```

## Syntax Elements

#### table_name

Specifies the name of the table where the column is to be renamed.

```sql
<table_name> ::= <identifier>
```

#### old_column_name

Specifies the old column name.

```sql
<old_column_name> ::= <identifier>
```

#### new_column_name

Specifies the new column name.

```sql
<new_column_name> ::= <identifier>
```

## Description

Changes the name of a column.

## Example

Create table tab with two columns named A and B.

```sql
CREATE ROW TABLE tab (A INT PRIMARY KEY, B INT);
```

Display the column names for table tab stored in the SAP HANA database.

```sql
SELECT COLUMN_NAME, POSITION FROM TABLE_COLUMNS WHERE SCHEMA_NAME =
CURRENT_SCHEMA AND TABLE_NAME = 'tab' ORDER BY POSITION;
```

Rename column A to C.

```sql
RENAME COLUMN tab.A TO C;
```

Display the column names for table tab after the renaming.

```sql
SELECT COLUMN_NAME, POSITION FROM TABLE_COLUMNS WHERE SCHEMA_NAME =
CURRENT_SCHEMA AND TABLE_NAME = 'tab' ORDER BY POSITION;
```

## Related Information

[Introduction to SQL](../../4.01-Introduction-to-SQL.md)
