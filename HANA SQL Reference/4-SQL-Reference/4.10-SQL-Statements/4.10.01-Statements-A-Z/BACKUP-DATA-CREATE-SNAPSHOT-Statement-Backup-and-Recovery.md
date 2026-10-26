# 4.10.1.35 BACKUP DATA CREATE SNAPSHOT Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 670–672

Creates an internal database snapshot for a database instance.

## Syntax

```sql
BACKUP DATA FOR FULL SYSTEM CREATE SNAPSHOT [ COMMENT <string> ] [ TIMEOUT
<integer> ]
```

## Syntax elements

#### FOR FULL SYSTEM

Creates an internal database snapshot of the system database and all the tenant databases.

`FOR FULL SYSTEM` is mandatory.

#### COMMENT string

Specifies a comment that is added for the data snapshot.

The maximum comment length is 256 characters and the comment appears in the COMMENT column of the monitoring view M_BACKUP_CATALOG.

#### TIMEOUT integer

Specifies a timeout (in seconds) for the operation.

## Description

Creates an internal database snapshot that reflects a consistent database state at the point in time when the snapshot was created.

To use a data snapshot for a subsequent recovery, you then need to copy the data area of the system database and all the tenant database to a separate storage location, then close (confirm) the data snapshot.

If an internal database snapshot exists, no new data backups or new database snapshots can be created. Conversely, while a data backup is running, you cannot create a database snapshot.

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

## Example

Prepare the database for a data snapshot by creating an internal database snapshot.

The comment `MySnapshot` helps to identify the data database snapshot in the backup catalog.

```sql
BACKUP DATA FOR FULL SYSTEM CREATE SNAPSHOT COMMENT 'MySnapshot';
```

## Related Information

[BACKUP DATA CLOSE SNAPSHOT Statement (Backup and Recovery)](BACKUP-DATA-CLOSE-SNAPSHOT-Statement-Backup-and-Recovery.md)
