# 6.2.93 M_ENCRYPTION_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1769–1770

Reports the encryption status for all data at rest where encryption is supported.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCOPE | VARCHAR(16) | Displays whether the scope includes PERSISTENCE (data volumes), LOG (redo log), or BACKUP. |
| IS_ENCRYPTION_ACTIVE | VARCHAR(5) | Indicates if the encryption for the scope is currently active: TRUE/FALSE. |
| LAST_CHANGE_TIME | TIMESTAMP | Displays the latest timestamp, in the server's local time, when the status was changed |
| CONFIGURATION_CONTROL | VARCHAR(16) | Indicates whether encryption configuration is controlled by the local data base or the system database. |
| ENCRYPTION_CONTROL_LAST_CHANGE_TIME | TIMESTAMP | Displays the last time that the tenant encryption control was changed. |

## Related Information

ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM ENCRYPTION CONFIGURATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENCRYPTION-CONFIGURATION-Statement-System.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md)
