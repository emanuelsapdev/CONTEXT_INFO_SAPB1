# 4.10.1.153 UNLOAD Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1109–1111

Unloads the column store table from memory.

## Syntax

```sql
UNLOAD <table_name> [ { <partition_restriction> | <persistent_memory_clause> } ]
```

## Syntax Elements

#### table_name

Unloads the specified table from memory.

```sql
<table_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### partition_restriction

Unloads the specified partition(s) from memory. This option is supported for partitioned column store tables. For multistore tables, only partitions in default storage are supported. Partitions in extended storage are not supported and return an error if specified.

```sql
<partition_restriction> ::=
 PARTITION ( <partition_number> [ <persistent_memory_clause> ] [,
<partition_number> [ <persistent_memory_clause> ] [, ...] ] )
```

`<partition_number>` is the logical partition ID and is stored in the M_CS_PARTITIONS system view.

If `<partition_restriction>` is not specified, then all partitions are unloaded by default. **persistent_memory_clause** Specifies whether persistent memory is deleted or retained when unloading a table.

```sql
<persistent_memory_clause> ::= { DELETE | RETAIN } PERSISTENT MEMORY
```

The default behavior is to retain the data files for real persistent memory and to delete the data files when persistent memory is configured on tmpfs.

**DELETE** Deletes persistent memory for the column as part unloading the table. **RETAIN** Retains persistent memory for the column as part of unload table.

## Description

To free up memory, use the UNLOAD statement to unload the column store table from memory. The table is loaded again on next access.

While the UNLOAD statement allows you to specify partitioned tables, the LOAD statement does not.

For more information on table partitioning, see the SAP HANA Administration Guide.

## Permissions

You must have either the UPDATE privilege or the system privilege TABLE ADMIN to execute the UNLOAD statement on a table.

## Example

Create column table A1.

```sql
CREATE COLUMN TABLE A1 (A INT, B INT);
```

Load table A1 into memory.

```sql
LOAD A1 all;
```

Unload table A1 from memory.

```sql
UNLOAD A1;
```

Check the load status of table A1.

```sql
SELECT loaded FROM m_cs_tables WHERE table_name = 'A1';
```

Delete persistent memory on partitions 1, but retain persistent memory on partition 2 when unloading g table A1.

```sql
UNLOAD A1 PARTITION (1 DELETE PERSISTENT MEMORY, 2 RETAIN PERSISTENT MEMORY);
```

Delete all persistent memory when unloading g table A1.

```sql
UNLOAD A1 DELETE PERSISTENT MEMORY;
```

## Related Information

[M_CS_PARTITIONS System View - Deprecated](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_CS_PARTITIONS-System-View-Deprecated.md)
