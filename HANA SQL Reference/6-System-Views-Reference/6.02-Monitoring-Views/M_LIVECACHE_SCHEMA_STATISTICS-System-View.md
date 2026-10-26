# 6.2.158 M_LIVECACHE_SCHEMA_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1870–1871

Provides accumulated liveCache schema statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| OMS_SCHEMA_HANDLE | INTEGER | Displays the OMS schema ID. |
| OMS_SCHEMA_NAME | NVARCHAR(96) | Displays the OMS schema name. |
| CREATE_TIME | TIMESTAMP | Displays the created timestamp. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_LIVECACHE_SCHEMA_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LIVECACHE_SCHEMA_STATISTICS_RESET;`.

## Related Information

M_LIVECACHE_SCHEMA_STATISTICS_RESET System View [→](M_LIVECACHE_SCHEMA_STATISTICS_RESET-System-View.md) SCHEMAS System View [→](../6.01-System-Views/SCHEMAS-System-View.md) CREATE SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SCHEMA-Statement-Data-Definition.md) RENAME SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-SCHEMA-Statement-Data-Definition.md) SET SCHEMA Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SCHEMA-Statement-Session-Management.md) DROP SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SCHEMA-Statement-Data-Definition.md)
