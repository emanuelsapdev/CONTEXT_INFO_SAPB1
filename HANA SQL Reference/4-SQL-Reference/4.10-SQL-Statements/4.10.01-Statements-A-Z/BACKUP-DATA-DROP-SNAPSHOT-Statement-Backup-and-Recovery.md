# 4.10.1.36 BACKUP DATA DROP SNAPSHOT Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 672–673

Physically deletes a data snapshot.

## Syntax

```sql
BACKUP DATA FOR FULL SYSTEM DROP SNAPSHOT
```

## Syntax elements

#### FOR FULL SYSTEM

Specifies that the data snapshot of the system database and all the tenant databases is deleted.

`FOR FULL SYSTEM` is mandatory.

## Description

If an error occurs executing `BACKUP DATA CLOSE SNAPSHOT`, use `BACKUP DATA DROP SNAPSHOT` to remove the latest data snapshot completely from persistence.

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

## Example

Delete the data snapshot in the system database and all the tenant databases.

```sql
BACKUP DATA FOR FULL SYSTEM DROP SNAPSHOT;
```

## Related Information

BACKUP DATA CLOSE SNAPSHOT Statement (Backup and Recovery) [→](BACKUP-DATA-CLOSE-SNAPSHOT-Statement-Backup-and-Recovery.md) BACKUP DATA CREATE SNAPSHOT Statement (Backup and Recovery) [→](BACKUP-DATA-CREATE-SNAPSHOT-Statement-Backup-and-Recovery.md)
