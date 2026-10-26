# 6.2.20 M_BACKUP_SIZE_ESTIMATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1661–1662

Provides the estimated size of the next data backup.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | NVARCHAR(32) | Displays the name of the service. |
| ENTRY_TYPE_NAME | NVARCHAR(64) | Displays the classification of the type of backup. The following types are supported: complete data backup, differential, and incremental backups. |
| ESTIMATED_SIZE | BIGINT | Displays the estimated size of the backup in bytes. |

## Additional Information

> **Note**
>
> The actual backup size may differ from the estimation shown in this view.

The ENTRY_TYPE_NAME column is equivalent to the column in the M_BACKUP_CATALOG view. The table contains records for each service with a volume for all the supported backup types. You cannot create a differential or incremental backup or view estimation of a differential or incremental backup if a complete backup does not exist. However, once a complete backup exists, you can view estimations for differential or incremental backups, even if these backups have not been created.

## Related Information

M_BACKUP_CATALOG System View [→](M_BACKUP_CATALOG-System-View.md) M_BACKUP_CATALOG_FILES System View [→](M_BACKUP_CATALOG_FILES-System-View.md) BACKUP CATALOG DELETE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-CATALOG-DELETE-Statement-Backup-and-Recovery.md) M_BACKUP_CONFIGURATION System View [→](M_BACKUP_CONFIGURATION-System-View.md) M_BACKUP_HISTORY_BROKEN System View [→](M_BACKUP_HISTORY_BROKEN-System-View.md) M_BACKUP_PROGRESS System View [→](M_BACKUP_PROGRESS-System-View.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) RECOVER DATA Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATA-Statement-Backup-and-Recovery.md)
