# 6.2.19 M_BACKUP_PROGRESS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1660–1661

Provides the progress of the most recent backup.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| BACKUP_ID | BIGINT | Displays the unique ID of a data backup. All backup files of a single data backup share the same BACKUP_ID. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the name of the service. |
| ENTRY_TYPE_NAME | VARCHAR(64) | Displays the classification of the type of backup. |
| SYS_START_TIME | TIMESTAMP | Displays the local server time that the backup started. |
| UTC_START_TIME | TIMESTAMP | Displays the time that the backup started. |
| SYS_END_TIME | TIMESTAMP | Displays the local server time that the backup was terminated. |
| UTC_END_TIME | TIMESTAMP | Displays the time that the backup was terminated. |
| STATE_NAME | VARCHAR(64) | Displays the current state of the backup. |
| BACKUP_SIZE | BIGINT | Displays the total amount of data in bytes. |
| TRANSFERRED_SIZE | BIGINT | Displays the amount of data transferred in bytes. |

## Related Information

M_BACKUP_CATALOG System View [→](M_BACKUP_CATALOG-System-View.md) M_BACKUP_CATALOG_FILES System View [→](M_BACKUP_CATALOG_FILES-System-View.md)

BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_CONFIGURATION System View [→](M_BACKUP_CONFIGURATION-System-View.md) M_BACKUP_HISTORY_BROKEN System View [→](M_BACKUP_HISTORY_BROKEN-System-View.md) M_BACKUP_SIZE_ESTIMATIONS System View [→](M_BACKUP_SIZE_ESTIMATIONS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
