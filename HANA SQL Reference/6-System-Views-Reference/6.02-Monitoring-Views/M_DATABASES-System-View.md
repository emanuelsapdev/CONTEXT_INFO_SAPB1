# 6.2.72 M_DATABASES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1737–1739

Provides information about all databases in the system. The full content of this view is only accessible from the system database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | NVARCHAR (256) | Displays the database name. |
| DESCRIPTION | NVARCHAR (2000) | Displays the database description. |
| ACTIVE_STATUS | VARCHAR (16) | Displays the database status. |
| ACTIVE_STATUS_DETAILS | VARCHAR (128) | Displays the database status details. Possible values include: stopped by user, stopped due to broken recovery, or stopped by takeover. |
| OS_USER | NVARCHAR(256) | Displays the database isolation operation system user. |
| OS_GROUP | NVARCHAR(256) | Displays the database isolation operation system group. |
| RESTART_MODE | VARCHAR(16) | Displays the restart behavior after a system restart. Possible values are NO (do not restart the database after a system restart) or DEFAULT (restore the database to the state it had before the system restart). |
| FALLBACK_SNAPSHOT_CREATE_TIME | TIMESTAMP | Displays the timestamp for when the fallback snapshot was created, or NULL if there is no fallback snapshot for the database. The value for this column is always NULL for SYSTEMDB. |

## Related Information

M_DATABASE System View [→](M_DATABASE-System-View.md) M_SNAPSHOTS System View [→](M_SNAPSHOTS-System-View.md) M_DATABASE_HISTORY System View [→](M_DATABASE_HISTORY-System-View.md) M_DATABASE_REPLICAS System View [→](M_DATABASE_REPLICAS-System-View.md) M_DATABASE_REPLICA_STATISTICS System View [→](M_DATABASE_REPLICA_STATISTICS-System-View.md) CREATE DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-DATABASE-Statement-Tenant-Database-Management.md) ALTER DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-DATABASE-Statement-Tenant-Database-Management.md) RENAME DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-DATABASE-Statement-Tenant-Database-Management.md) DROP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-DATABASE-Statement-Tenant-Database-Management.md) ALTER SYSTEM START DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-DATABASE-Statement-Tenant-Database.md) ALTER SYSTEM STOP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-STOP-DATABASE-Statement-Tenant-Database.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md)
