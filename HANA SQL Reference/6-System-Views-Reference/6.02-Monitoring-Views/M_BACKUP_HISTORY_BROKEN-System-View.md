# 6.2.18 M_BACKUP_HISTORY_BROKEN System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1658–1660

Provides information about broken backup history entries.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| BACKUP_ID | BIGINT | Displays the unique ID of the broken backup history entry. |
| SYS_TIME | TIMESTAMP | Displays the time at which the broken backup history was detected. The time is provided in the system's local time. |
| UTC_TIME | TIMESTAMP | Displays the time at which the broken backup history was detected. The time is given in UTC time. |
| SOURCE_ID | INTEGER | Displays the persistence volume ID. |
| HOST | VARCHAR(64) | Displays the host name. |
| SERVICE_TYPE_NAME | VARCHAR(64) | Displays the type of database service. |
| REDO_LOG_POSITION | BIGINT | Displays the redo log position of the broken backup history entry. |
| REASON | VARCHAR(64) | Displays the reason for the broken backup history:<br>• Unknown reason<br>• Redo log writing disabled on persistence session<br>• Redo log flush partially turned OFF<br>• Redo log flush turned ON<br>• Migration to "level 2 delta"<br>• General reason for persistence factory<br>• Extended storage persistence encryption key changed |
| MESSAGE | VARCHAR(256) | Displays any additional information. |

## Related Information

M_BACKUP_CATALOG System View [→](M_BACKUP_CATALOG-System-View.md) M_BACKUP_CATALOG_FILES System View [→](M_BACKUP_CATALOG_FILES-System-View.md) BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_CONFIGURATION System View [→](M_BACKUP_CONFIGURATION-System-View.md) M_BACKUP_SIZE_ESTIMATIONS System View [→](M_BACKUP_SIZE_ESTIMATIONS-System-View.md) M_BACKUP_PROGRESS System View [→](M_BACKUP_PROGRESS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
