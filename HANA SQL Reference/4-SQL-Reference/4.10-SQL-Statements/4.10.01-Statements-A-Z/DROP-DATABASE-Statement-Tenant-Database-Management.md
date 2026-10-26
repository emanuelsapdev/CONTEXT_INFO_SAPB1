# 4.10.1.88 DROP DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 901–902

Drops a tenant database.

## Syntax

```sql
DROP DATABASE <database_name> [ DROP BACKUPS ]
```

## Syntax Elements

#### database_name

Specifies the database name.

```sql
<database_name> ::= <identifier>
```

#### DROP BACKUPS

Drops all current backup directories for the tenant database. Backup directories that were previously in use, and backups that are written to third-party backup tools, are not deleted.

## Description

DROP DATABASE drops the specified tenant database.

## Permissions

The use of this statement requires the DATABASE ADMIN privilege.

## Example

The following example shows you how to drop the my_database database.

```sql
DROP DATABASE my_database;
```
