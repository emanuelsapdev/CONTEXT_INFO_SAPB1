# 4.10.1.30 BACKUP CATALOG DELETE Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 657–659

Deletes the records of all backups (both filebased and Backint) from the backup catalog. Optionally, also deletes the associated physical backups.

## Syntax

```sql
BACKUP CATALOG DELETE [ FOR <database_name> ]
   { ALL BEFORE BACKUP_ID <backup_id> [ WITH FILE | WITH BACKINT | COMPLETE ]
     | BACKUP_ID <backup_id> [ COMPLETE ]
   }
```

## Syntax Elements

#### FOR database_name

Specifies the name of the tenant database whose backups will be deleted.

```sql
<database_name> ::= <identifier>
```

FOR `<database_name>` can only be used through the system database.

If FOR `<database_name>` is omitted, then the local database is assumed. The local database can be either the system database or a tenant database.

#### backup_id

Specifies the ID of a specific backup to be deleted.

ALL BEFORE `<backup_id>` removes the backup catalog records of backups that are older than the specified backup.

#### WITH FILE

In addition to deleting the records in the backup catalog (for both filebased and Backint backups), WITH FILE also deletes the associated physical backups in the file system.

> **Note**
>
> SAP HANA can only physically delete filebased backups that are at the location specified in the backup catalog.

#### WITH BACKINT

In addition to deleting the records in the backup catalog (for both filebased and Backint backups), WITH BACKINT also deletes the associated physical backups in the third-party backup tool.

#### COMPLETE

In addition to deleting the records in the backup catalog (for both filebased and Backint backups), COMPLETE also deletes the associated physical backups in the file system and the third-party backup tool.

> **Note**
>
> SAP HANA can only delete filebased physical backups that are at the location specified in the backup catalog.

## Description

`BACKUP CATALOG DELETE` can be executed on the system database or on a tenant database.

From the system database, you can execute BACKUP CATALOG DELETE on a tenant database, which is specified using the `FOR <database_name>` clause.

If you omit COMPLETE, WITH FILE, or WITH BACKINT, then only the specified records in the backup catalog are deleted. The physical backups are retained.

If a tenant database is specified (using `FOR <database_name>`), that database must be online.

Only the `ALL BEFORE` option deletes the log backups and the log backup records in the backup catalog.

At least one data backup must remain in the backup catalog. For this reason, if a selected data backup is the last and only backup, it cannot be deleted.

The records in the backup catalog are deleted synchronously. Physical backups are deleted asynchronously. The deletion process continues even after a service shutdown or restart.

> **Tip**
>
> It is recommended to regularly delete backups that are no longer needed.
>
> It is important to regularly truncate the backup catalog because, as the backup catalog increases in size, it takes longer to record each new backup.

> **Note**
>
> If a data backup is physically available, but not recorded in the backup catalog, that data backup can still be used to recover the database.
>
> Third-party data backups that are not recorded in the backup catalog must have a unique prefix to be able to be used for a recovery.

For more information about the `BACKUP CATALOG DELETE` statement, see Housekeeping for Backup Catalog and Backup Storage in the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery).

## Permissions

Privileges needed:

BACKUP ADMIN

`FOR <database_name>`: DATABASE BACKUP ADMIN or DATABASE ADMIN

## Examples

**Example 1:** The following example truncates the backup catalog and removes all the physical backups older than the data backup specified by BACKUP_ID `1496915612668`. It deletes the associated data backups, delta backups, log backups, and backups of the backup catalog in both the file system and in the third-party backup tool.

```sql
BACKUP CATALOG DELETE ALL BEFORE BACKUP_ID 1496915612668 COMPLETE;
```

This statement can be executed from the system database or the tenant database.

**Example 2:** For the tenant database `PR1`, the following example truncates the backup catalog and removes all the physical backups older than the data backup specified by BACKUP_ID `1496915612668`. It deletes the associated data backups, delta backups, log backups, and backups of the backup catalog in both the file system and in the third-party backup tool.

```sql
BACKUP CATALOG DELETE FOR PR1 ALL BEFORE BACKUP_ID 1496915612668 COMPLETE;
```

This statement can be executed from the system database.

**Example 3:** The following example only deletes the record of the data backup specified by BACKUP_ID `1496915612668` in the backup catalog. The physical data backup itself is not deleted.

```sql
BACKUP CATALOG DELETE BACKUP_ID 1496915612668;
```

This statement can be executed from the system database or the tenant database.
