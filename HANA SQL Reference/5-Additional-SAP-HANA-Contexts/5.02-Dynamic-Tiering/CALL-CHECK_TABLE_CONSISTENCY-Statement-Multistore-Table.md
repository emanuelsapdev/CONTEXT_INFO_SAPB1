# 5.2.13 CALL CHECK_TABLE_CONSISTENCY Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1270–1273

Performs consistency check actions in the column store partition of a multistore table.

## Syntax

```sql
CALL CHECK_TABLE_CONSISTENCY ('<action>', '<schema name>', '<table name>')
```

## Syntax Elements

#### action

The type of consistency check to perform.

```sql
<action> ::=
 CHECK
 | CHECK_COLUMN_TABLES
 | CHECK_PRIMARY_KEY
 | CHECK_ROWID
 | CHECK_PARTITIONING
 | CHECK_PARTITIONING_DATA
 | REPAIR_PARTITIONING_DATA
```

##### CHECK

Performs all available checks.

##### CHECK_COLUMN_TABLES

Performs a check restricted to default (column) store and multistore tables.

##### CHECK_PRIMARY_KEY

Checks the consistency of the primary key in the default store.

##### CHECK_ROWID

Checks the consistency of the internal `$rowid$` column only for the column store partition of a multistore table.

##### CHECK_PARTITIONING

Checks the consistency of partitioning-related metadata.

##### CHECK_PARTITIONING_DATA

Checks the assignment of rows to partitions.

##### REPAIR_PARTITIONING_DATA

Repairs the assignment to rows to partitions.

Additional `<action>` options are available for the default store.

#### schema_name

Specifies the name of the analyzed schema.

#### object_name

Specifies the name of the analyzed object.

#### table_name

Specifies the name of the analyzed table.

## Permissions

The privilege needed depends on the clause used:

- Check action – CATALOG READ or DATA ADMIN
- Repair action – DATA ADMIN

## Description

CHECK_TABLE_CONSISTENCY performs consistency check actions in the column store partition of a multistore table.

You can only perform a table consistency check for column store partitions in a multistore table.

If you have tables or schemas with names containing lowercase characters, slashes ("/"), or other special characters, enclose them in double-quotation marks to prevent CHECK_TABLE_CONSISTENCY from normalizing them, treating them as strings.

For more information about CALL and table consistency checks, see:

- SAP HANA SQL and System Views Reference > SQL Reference > SQL Statements > Procedural Statements > CALL Statement (Procedural)
- SAP HANA Administration Guide > System Administration> Table and Catalog Consistency Checks > Table Consistency Checks
- SAP Note 1977584 – Technical Consistency Checks for SAP HANA Databases

## Example

This procedure checks the consistency for a table named "ABC/abc" in the SYSTEM schema:

```sql
CALL CHECK_TABLE_CONSISTENCY ('CHECK', 'SYSTEM', '"ABC/abc"');
```

## Related Information

[SAP Note 1977584 CALL Statement (Procedural)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CALL-Statement-Procedural.md)
