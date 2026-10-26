# 4.10.1.152 TRUNCATE TABLE Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1107–1109

Deletes all rows from a table or projection view.

## Syntax

```sql
TRUNCATE TABLE <table_name>
```

## Syntax Elements

#### table_name

Specifies the name of a table or projection view.

```sql
<table_name> ::= [[<database_name>.]<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

For linked database, `<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

## Description

TRUNCATE TABLE is faster than DELETE FROM when deleting all records from a table, but TRUNCATE TABLE cannot be rolled back. To roll back from record deletion, use the DELETE statement.

HISTORY tables can also be truncated by using this statement. All parts of the history table (main, delta, history main, and history delta) are truncated and the content is permanently deleted.

TRUNCATE TABLE causes an implicit commit.

TRUNCATE TABLE is also supported in DDL auto commit mode OFF, except for local and global temporary column tables. A TRUNCATE TABLE on temporary column tables cannot be rolled back, but it does not commit changes on other database objects.

In the documentation, TRUNCATE TABLE is included with the DML statements because its purpose is to delete table data and users typically associate it with a DML statement. However, TRUNCATE TABLE behaves as a DDL statement (that is, it causes an implicit commit) if run when the transaction mode AUTOCOMMIT DDL is set to ON (SET TRANSACTION statement).

SQLScript transactions normally run in AUTOCOMMIT DDL OFF, so an implicit commit is not performed for TRUNCATE TABLE.

TRUNCATE TABLE is allowed on a history table associated with a system-versioned table. When you execute a TRUNCATE TABLE statement on the system-versioned table, truncated records are not archived in the associated history table.

## Example

Create table A.

```sql
CREATE TABLE A (A INT PRIMARY KEY, B INT);
```

Truncate the contents of table A.

```sql
TRUNCATE TABLE A;
```

## Related Information

[DELETE Statement (Data Manipulation)](DELETE-Statement-Data-Manipulation.md)
