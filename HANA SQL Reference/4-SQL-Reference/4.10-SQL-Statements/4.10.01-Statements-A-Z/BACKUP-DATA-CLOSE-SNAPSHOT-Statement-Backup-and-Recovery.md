# 4.10.1.34 BACKUP DATA CLOSE SNAPSHOT Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 668–670

Confirms that a data snapshot has been created or that the data snapshot has been abandoned.

## Syntax

```sql
BACKUP DATA FOR FULL SYSTEM CLOSE SNAPSHOT BACKUP_ID <backup_id>
 { SUCCESSFUL <external_id> | UNSUCCESSFUL [ <string> ] }
```

## Syntax Elements

#### FOR FULL SYSTEM

Closes a data snapshot of the system database and all the tenant databases.

`FOR FULL SYSTEM` is mandatory.

#### BACKUP_ID backup_id

Specifies the unique ID of a data snapshot to be confirmed or abandoned.

#### SUCCESSFUL external_id

Specifies an ID for the data snapshot to help to identify a specific snapshot.

TIMESTAMP is supported for `<external_id>`. The maximum length of the external ID is 64 characters.

#### UNSUCCESSFUL [string ]

UNSUCCESSFUL `<string>` flags the data snapshot as unsuccessful in the backup catalog, and includes the comment specified in `<string>`. UNSUCCESSFUL without `<string>` flags the data snapshot as unsuccessful in the backup catalog without a comment.

The maximum length of `<string>` is 256 characters.

## Description

To close a data snapshot:

| **To Confirm or Abandon...** | **Perform the Following Steps** |
| --- | --- |
| Confirm the data snapshot | A data snapshot can be used to recover a database provided that it was completed successfully.<br>If you wish to retain the data snapshot to use for a recovery later, you must first manually copy the data snapshot (the content of the data area) to a separate storage location. Then, you need to close (confirm) the data snapshot.<br>Closing the data snapshot confirms that a data snapshot has been created and stored in a separate storage location, or that the data snapshot has been abandoned. When the data snapshot has been confirmed or abandoned, it is deleted from the data area. After that, it is possible to create further data snapshots or full backups.<br>To identify the data snapshot during a subsequent recovery, you can specify an external ID. To find the backup ID, search in the monitoring view M_BACKUP_CATALOG. The comment that was used when creating the backup is displayed in the COMMENT column of M_BACKUP_CATALOG.<br>If BACKUP DATA CLOSE SNAPSHOT returns an error, the data snapshot cannot be used.<br>If an error occurs executing BACKUP DATA CLOSE SNAP SHOT, use **BACKUP DATA DROP SNAPSHOT** to remove the latest data snapshot completely from persistence. |
| Abandon the data snapshot | If you do not wish to retain the data snapshot, you only need to close (abandon) it. |

After you have confirmed or abandoned a data snapshot, it is recorded in the backup catalog as either successful or unsuccessful.

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

## Examples

**Example 1**: Confirm that a data snapshot has been successfully created.

```sql
BACKUP DATA FOR FULL SYSTEM CLOSE SNAPSHOT BACKUP_ID 1400761459486 SUCCESSFUL
'External_ID_23';
```

**Example 2**: Abandon a data snapshot.

If the data snapshot was not created successfully, or if you do not want to use it, you can add a comment to help identify the data snapshot in the backup catalog. It can be helpful to add the reason for abandoning the snapshot.

```sql
BACKUP DATA FOR FULL SYSTEM CLOSE SNAPSHOT BACKUP_ID 1400761459486 UNSUCCESSFUL
'Do not use - was manually terminated';
```

## Related Information

BACKUP DATA DROP SNAPSHOT Statement (Backup and Recovery) [→](BACKUP-DATA-DROP-SNAPSHOT-Statement-Backup-and-Recovery.md) BACKUP DATA CREATE SNAPSHOT Statement (Backup and Recovery) [→](BACKUP-DATA-CREATE-SNAPSHOT-Statement-Backup-and-Recovery.md)
