# 4.10.1.24 ALTER VIRTUAL TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 644–646

Modifies a virtual table's column properties, and lets you refresh the metadata of a virtual table.

## Syntax

```sql
ALTER VIRTUAL TABLE <virtual_table_name>
  { SET PROPERTY 'name' = 'value'[, 'name2' = 'value2'[, ...] ]
    | UNSET PROPERTY 'name'[, 'name2', ...]
    | ALTER <column_name> SET PROPERTY 'name' = 'value' [, 'name2' = 'value2'
[, ...] ]
    | ALTER <column_name> UNSET PROPERTY 'name'[, 'name2'[, ...] ]
    | REFRESH DEFINITION }
```

## Syntax Elements

#### virtual_table_name

Specifies a virtual table.

```sql
<virtual_table_name> ::= [ <schema_name>.]<identifier>
```

#### column_name

Specifies a virtual column.

```sql
<column_name> ::= <identifier>
```

**REFRESH DEFINITION** Updates a virtual table to reflect metadata changes in the corresponding remote table.

## Description

Any properties that are not set by using the ALTER VIRTUAL TABLE statement are marked as read-only, which cannot be updated by the ALTER VIRTUAL TABLE statement.

Use the DROP TABLE `<table_name>` to drop a virtual table.

## Permissions

This statement requires the CREATE VIRTUAL TABLE object privilege.

## Examples

Set a new property for the virtual table REMOTE1_VT, then update and unset it.

```sql
ALTER VIRTUAL TABLE REMOTE1_VT SET PROPERTY 'name1' = 'value1';
ALTER VIRTUAL TABLE REMOTE1_VT SET PROPERTY 'name1' = 'value2';
ALTER VIRTUAL TABLE REMOTE1_VT UNSET PROPERTY 'name1';
```

Set a new property for the virtual column A in virtual table REMOTE1_VT, then update and unset it.

```sql
ALTER VIRTUAL TABLE REMOTE1_VT ALTER A SET PROPERTY 'name1' = 'value1';
ALTER VIRTUAL TABLE REMOTE1_VT ALTER A SET PROPERTY 'name1' = 'value2';
ALTER VIRTUAL TABLE REMOTE1_VT ALTER A UNSET PROPERTY 'name1';
```

## Related Information

DROP TABLE Statement (Data Definition) [→](DROP-TABLE-Statement-Data-Definition.md) VIRTUAL_TABLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIRTUAL_TABLES-System-View.md) M_EXPENSIVE_STATEMENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_EXPENSIVE_STATEMENTS-System-View.md)
