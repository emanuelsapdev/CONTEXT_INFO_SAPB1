# 6.2.213 M_QUERY_CACHED_PLANS System View - Deprecated

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1941–1942

Provides query cached plan information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ABAP_VARCHAR_MODE | VARCHAR(5) | Displays whether or not ABAP VAR CHAR mode is enabled: TRUE/FALSE. |
| IS_REMOTE | VARCHAR(5) | Displays whether or not REMOTE is supported: TRUE/FALSE. |
| STATEMENT_STRING | NLCOB | Displays the SQL statement. |
| PLAN_ID | BIGINT | Displays the logical plan ID. |
| REFERENCE_COUNT | BIGINT | Displays the number of statements using the plan. |
| USED_MEMORY_SIZE | BIGINT | Displays the current snapshot of the used memory size for executing this statement in bytes. |
| SHARING_TYPE | VARCHAR(128) | Displays the sharing type. |
| OWNER_CONNECTION_ID | INTEGER | Displays the connection ID of the owner. |

## Related Information

ALTER SYSTEM CLEAR SQL PLAN CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-SQL-PLAN-CACHE-Statement-System.md) ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECOMPILE-SQL-PLAN-CACHE-ENTRY-Statement.md) ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PIN-UNPIN-SQL-PLAN-CACHE-ENTRY-Statement.md)
