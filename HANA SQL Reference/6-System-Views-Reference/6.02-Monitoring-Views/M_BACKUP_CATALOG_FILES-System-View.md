# 6.2.16 M_BACKUP_CATALOG_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1655–1657

Provides location information for all backup catalog entries.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ENTRY_ID | BIGINT | Displays the unique ID of a backup catalog entry. |
| BACKUP_ID | BIGINT | Displays the unique ID of a data backup and log backup respectively. All backup files of a single data backup share the same backup ID. |
| SOURCE_ID | BIGINT | Displays the persistence volume ID. |
| SOURCE_TYPE_NAME | VARCHAR(64) | Displays the type of persistence to be backed up: volume or topology. |
| HOST | VARCHAR(64) | Displays the host name. |
| SERVICE_TYPE_NAME | VARCHAR(64) | Displays the type of database service: indexserver, nameserver, or statistics server. |
| REDO_LOG_POSITION | BIGINT | In the case of a data backup, this value displays the log position that must be processed next when a log recovery is requested after restoring the data backup. |
| FIRST_REDO_LOG_POSITION | BIGINT | In the case of a log backup, this value displays the log position of the oldest log entry contained in the backup. |
| LAST_REDO_LOG_POSITION | BIGINT | In the case of a log backup, this value displays the log position of the newest log entry contained in the backup. |
| BACKUP_SIZE | BIGINT | Displays the size of the backup in bytes. |
| DESTINATION_PATH | VARCHAR(512) | Displays that the data or log backup was written to this location. |
| DESTINATION_TYPE_NAME | VARCHAR(16) | Displays the type of location: file or backint. |
| EXTERNAL_BACKUP_ID | VARCHAR(64) | Displays the identifier of the backup received from a backup tool. |
| LOG_SEGMENT_COUNT | INTEGER | In the case of a log backup, this value displays the number of log segments contained in the backup.<br>For non-log backups, this column always contains the SQL NULL value. |
| BACKUP_CATALOG_BACKUP_ID | BIGINT | Displays the unique ID of the backup of the backup catalog that was triggered after a particular data or log backup.<br>This ID indicates which backup of the backup catalog is the first one that contains that backup operation. |
| UTC_LAST_COMMIT_TIME | INTEGER | Displays the most recent commit time in UTC for log backups only.<br>This time shows the most recent point in time, to which this backup can be used to recover the database.<br>The times of a backup's start and completion do not indicate the point in time that can be reached in a recovery using that backup. This is because the most recent database commit is older. |

## Related Information

M_BACKUP_CATALOG System View [→](M_BACKUP_CATALOG-System-View.md) BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_CONFIGURATION System View [→](M_BACKUP_CONFIGURATION-System-View.md) M_BACKUP_HISTORY_BROKEN System View [→](M_BACKUP_HISTORY_BROKEN-System-View.md) M_BACKUP_SIZE_ESTIMATIONS System View [→](M_BACKUP_SIZE_ESTIMATIONS-System-View.md) M_BACKUP_PROGRESS System View [→](M_BACKUP_PROGRESS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
