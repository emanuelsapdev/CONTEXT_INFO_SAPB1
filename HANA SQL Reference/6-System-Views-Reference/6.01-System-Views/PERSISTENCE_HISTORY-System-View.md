# 6.1.109 PERSISTENCE_HISTORY System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1527–1528

Records the database version history.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CHANGE_ID | INTEGER | Displays the order of database installations. |
| CHANGE_TIME | TIMESTAMP | Displays the timestamp when the data base was upgraded or recovered to the current version. |
| VERSION | VARCHAR(32) | Displays the version. |
| SYSTEM_ID | VARCHAR(3) | Displays the system ID of the SAP HANA instance. |
| HOST | VARCHAR(64) | Displays the host name of the catalog master. Only users with INIFILE ADMIN or CATALOG READ privileges are able to view this column. |

## Related Information

SET HISTORY SESSION Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-HISTORY-SESSION-Statement-Session-Management.md) M_BACKUP_HISTORY_BROKEN System View [→](../6.02-Monitoring-Views/M_BACKUP_HISTORY_BROKEN-System-View.md) M_JOB_HISTORY_INFO System View [→](../6.02-Monitoring-Views/M_JOB_HISTORY_INFO-System-View.md)
