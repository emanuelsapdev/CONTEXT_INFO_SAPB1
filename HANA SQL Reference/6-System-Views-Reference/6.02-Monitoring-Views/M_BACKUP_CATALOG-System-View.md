# 6.2.15 M_BACKUP_CATALOG System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1653–1655

Provides common data for all backup catalog entries.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ENTRY_ID | BIGINT | Dislays the unique ID of the backup catalog entry. |
| ENTRY_TYPE_NAME | VARCHAR(64) | Displays the classification of backup catalog entries. The following types are supported: complete data backup, data snapshot, log backup, log missing, differential, and incremental backups. |
| BACKUP_ID | BIGINT | Displays the unique ID of a data backup or a log backup, respectively. All backup files of a single data backup share the same BACKUP_ID. |
| SYS_START_TIME | TIMESTAMP | Displays the start time given in the server's local time. |
| UTC_START_TIME | TIMESTAMP | Displays the start time given in UTC. |
| SYS_END_TIME | TIMESTAMP | Displays the stop time given in the server's local time. |
| UTC_END_TIME | TIMESTAMP | Displays the stop time given in UTC. |
| STATE_NAME | VARCHAR(64) | Displays the result of the corresponding action: successful, failed, running, cancel pending, or canceled. |
| COMMENT | VARCHAR(256) | Displays any additional information. |
| MESSAGE | VARCHAR(512) | Displays any additional information. |
| SYSTEM_ID | VARCHAR(3) | Displays the system identifier (SID) of the SAP HANA database. |
| ENCRYPTION_ROOT_KEY_HASH | VARCHAR(64) | Displays the key hash used, if any, to locate the encryption root key in the key store. |
| SOURCE_DATABASE_NAME | NVARCHAR(256) | Displays the name of the database that created the backup. |
| ES_ENCRYPTION_CHANGE_ENABLED | VARCHAR(5) | This column applies to SAP HANA dynamic tiering only. Displays if the backup can be used to change the volume encryption key during recovery. Set to TRUE if DISABLE ES ENCRYP TION CHANGE is shown at backup time and if extended storage is in the topology. Displays NULL if extended storage does not exist in the topology. |

## Related Information

M_BACKUP_CATALOG_FILES System View [→](M_BACKUP_CATALOG_FILES-System-View.md) BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_CONFIGURATION System View [→](M_BACKUP_CONFIGURATION-System-View.md) M_BACKUP_HISTORY_BROKEN System View [→](M_BACKUP_HISTORY_BROKEN-System-View.md) M_BACKUP_SIZE_ESTIMATIONS System View [→](M_BACKUP_SIZE_ESTIMATIONS-System-View.md) M_BACKUP_PROGRESS System View [→](M_BACKUP_PROGRESS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
