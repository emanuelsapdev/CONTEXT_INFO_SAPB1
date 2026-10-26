# 4.10.1.135 RENAME DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1022–1023

Changes the name of a tenant database.

## Syntax

```sql
RENAME DATABASE <current_database_name> TO <new_database_name>
```

## Syntax Elements

#### current_database_name

Specifies the current database name with an optional schema name.

```sql
<current_database_name> ::= <identifier>
```

#### new_database_name

Specifies the new database name.

```sql
<new_database_name> ::= <identifier>
```

## Description

The RENAME DATABASE statement changes the name of a tenant database.

Renaming tenant databases is not supported on systems running SAP HANA dynamic tiering.

## Permissions

You must be in SYSTEMDB and have the DATABASE ADMIN privilege to change the name of a tenant database.

## Example

The following example renames the tenant database MYOPS to MYOPSDEV.

```sql
RENAME DATABASE MYOPS TO MYOPSDEV;
```
