# 6.2.17 M_BACKUP_CONFIGURATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1657–1658

Provides backup configuration statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| MAX_RECOVERY_FILE_AGE | BIGINT | Displays the maximum recovery file age in seconds. |
| LOG_REPLAY_STEP_SIZE | BIGINT | Displays the log replay step size in bytes. |
| MAX_RECOVERY_BACKINT_CHANNELS | BIGINT | Displays the maximum number of parallel backint channels per request during recovery. |
| BACKINT_EXECUTABLE_LINK | VARCHAR(256) | Displays the backint executable link name. |
| BACKINT_EXECUTABLE | VARCHAR(256) | Displays the backint executable file name. |
| BACKINT_DATA_BACKUP_PATH | VARCHAR(256) | Displays the data backup directory for the backint. |
| BACKINT_LOG_BACKUP_PATH | VARCHAR(256) | Displays the log backup directory for the backint. |
| BACKINT_CATALOG_BACKUP_PATH | VARCHAR(256) | Displays the directory for backint-based catalog backups. |
| FILE_DATA_BACKUP_PATH | VARCHAR(256) | Displays the default directory for file based data backups. |
| FILE_LOG_BACKUP_PATH | VARCHAR(256) | Displays the current directory for file based log backups. |
| FILE_CATALOG_BACKUP_PATH | VARCHAR(256) | Displays the directory for filebased catalog backups. |
| FILE_ROOTKEY_BACKUP_PATH | VARCHAR(256) | Displays the directory for filebased rootkey backups. |
| LOG_BACKUP_TIMEOUT | BIGINT | Displays the log backup timeout in seconds. |
| LOG_BACKUP_INTERVAL_MODE | VARCHAR(16) | Displays the log backup interval mode. |
| IS_ROOT_KEY_BACKUP_PASSWORD_SET | VARCHAR(5) | Displays if the root key backup pass word is set for the specified database: TRUE/FALSE. |
| ROOT_KEY_ENCRYPTION_CONTROL | VARCHAR(16) | Displays whether encryption is configured at the system or local database level: SYSTEM DATABASE/LOCAL DA TABASE. |
| ROOT_KEY_BACKUP_PASSWORD_LAST_CHANGE_TIME | TIMESTAMP | Displays when the root key backup password was last changed. |

## Related Information

M_BACKUP_CATALOG System View [→](M_BACKUP_CATALOG-System-View.md) M_BACKUP_CATALOG_FILES System View [→](M_BACKUP_CATALOG_FILES-System-View.md) BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_HISTORY_BROKEN System View [→](M_BACKUP_HISTORY_BROKEN-System-View.md) M_BACKUP_SIZE_ESTIMATIONS System View [→](M_BACKUP_SIZE_ESTIMATIONS-System-View.md) M_BACKUP_PROGRESS System View [→](M_BACKUP_PROGRESS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
