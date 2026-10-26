# 4.10.1.124 LOAD Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 990–992

Explicitly loads column store table data into memory instead of upon first access.

## Syntax

```sql
LOAD <table_name> [HISTORY]
   { DELTA
     | ALL
     | (<column_name>, ...)
   }
```

## Syntax Elements

#### table_name

Specifies the name of the table to be loaded into memory, with optional schema name.

```sql
<table_name> ::= [<schema_name>.]<identifier>

<schema_name> ::= <unicode_name>
```

#### HISTORY

Use the HISTORY option when `<table_name>` is the name of a history table. The default operation of the LOAD command loads the current state of the given table into memory. If you explicitly require the table history to be loaded into memory, a separate LOAD statement with the HISTORY option enabled has to be executed. So to load a history completely into memory, two LOAD statements have to be executed, with and without HISTORY option enabled.

If you do not explicitly load table history into memory, then the SAP HANA database automatically loads this data upon first access.

#### DELTA

Specifies that the delta part of a column store table is loaded into memory. As the column store is read, optimized, and compressed, deltas are used to optimize insert or update operations.

#### ALL

Specifies that all current data of the column store table, including its delta, is loaded into memory. This option does not load the table history.

#### column_name

Specifies the name of the column to be loaded into memory.

```sql
<column_name> ::= <identifier>
```

## Description

The LOAD statement explicitly loads column store table data into memory instead of upon first access.

A LOAD statement without HISTORY option only loads the current table data and the table delta into memory, but not the history-delta and history-main.

The use of this statement requires the UPDATE privilege.

## Examples

Create column table A.

```sql
CREATE COLUMN TABLE A (A INT, B INT);
```

Load table A into memory.

```sql
LOAD A all;
```

Load the columns A and B of table A into memory.

```sql
LOAD A (A,B);
```

Query the load status of table A using the m_cs_tables monitoring view.

```sql
SELECT loaded FROM m_cs_tables WHERE table_name = 'A';
```

## Related Information

[M_CS_TABLES System View](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_CS_TABLES-System-View.md)
