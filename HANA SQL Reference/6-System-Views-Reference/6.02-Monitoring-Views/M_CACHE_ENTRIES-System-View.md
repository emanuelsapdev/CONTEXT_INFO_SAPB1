# 6.2.28 M_CACHE_ENTRIES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1669–1670

Provides cache entry information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| CACHE_ID | VARCHAR(128) | Displays the ID of the cache that created the entry. |
| ENTRY_ID | VARCHAR(128) | Displays the ID of the cached entry. |
| ENTRY_DESCRIPTION | NVARCHAR(5000) | Displays the description of the cached entry. |
| COMPONENT | VARCHAR(128) | Displays the information about the component that created the cached en try. |
| USER_NAME | NVARCHAR(256) | Displays the information about the user that created the cached entry. |
| MEMORY_SIZE | BIGINT | Displays the used memory to store the cached entry in the cache in bytes. |
| CREATE_TIME | TIMESTAMP | Displays the point in time when the cache entry was inserted into the cache in bytes. |
| READ_COUNT | BIGINT | Determines how often the cache entry was read successfully from the cache. |

## Related Information

M_CACHES System View [→](M_CACHES-System-View.md) ALTER SYSTEM CLEAR CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR SQL PLAN CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-SQL-PLAN-CACHE-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REMOVE SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-SQL-PLAN-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR TIMEZONE CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TIMEZONE-CACHE-Statement-System.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-Statement-System.md) ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECOMPILE-SQL-PLAN-CACHE-ENTRY-Statement.md) ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PIN-UNPIN-SQL-PLAN-CACHE-ENTRY-Statement.md) M_DYNAMIC_RESULT_CACHE System View [→](M_DYNAMIC_RESULT_CACHE-System-View.md) M_SQL_PLAN_CACHE_PARAMETERS System View [→](M_SQL_PLAN_CACHE_PARAMETERS-System-View.md)
