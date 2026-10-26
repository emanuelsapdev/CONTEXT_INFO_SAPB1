# 6.2.71 M_DATABASE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1736–1737

Provides database information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SYSTEM_ID | VARCHAR(3) | Displays the system SID. |
| DATABASE_NAME | NVARCHAR(256) | Displays the database name. |
| HOST | VARCHAR(64) | Displays the default master host. |
| START_TIME | TIMESTAMP | Displays the start time. |
| VERSION | VARCHAR(32) | Displays the version: major.mi nor.patch.build. |
| USAGE | VARCHAR(32) | Database usage type. Recommended values: production, test, development, or custom. Any value is allowed, but recommended values may be used by clients to alter behavior. |

## Related Information

M_DATABASES System View [→](M_DATABASES-System-View.md) M_DATABASE_HISTORY System View [→](M_DATABASE_HISTORY-System-View.md) M_DATABASE_REPLICAS System View [→](M_DATABASE_REPLICAS-System-View.md) M_DATABASE_REPLICA_STATISTICS System View [→](M_DATABASE_REPLICA_STATISTICS-System-View.md) CREATE DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-DATABASE-Statement-Tenant-Database-Management.md) ALTER DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-DATABASE-Statement-Tenant-Database-Management.md) RENAME DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-DATABASE-Statement-Tenant-Database-Management.md) DROP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-DATABASE-Statement-Tenant-Database-Management.md) ALTER SYSTEM START DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-DATABASE-Statement-Tenant-Database.md) ALTER SYSTEM STOP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-STOP-DATABASE-Statement-Tenant-Database.md) RECOVER DATABASE Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RECOVER-DATABASE-Statement-Backup-and-Recovery.md) Log On to a Database
