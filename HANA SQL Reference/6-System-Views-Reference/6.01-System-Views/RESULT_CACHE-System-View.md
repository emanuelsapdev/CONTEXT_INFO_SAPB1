# 6.1.139 RESULT_CACHE System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1559–1560

Provides information about objects available to use the result cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type: VIEW/FUNC TION. |
| OBJECT_OID | BIGINT | Displays the object ID. |
| CACHE_TYPE | VARCHAR(44) | Displays which type of cache is enabled for the object: FULL, PARTIAL (SE LECTED COLUMNS), PARTIAL (FIL TERED), or PARTIAL (SELECTED COL UMNS, FILTERED). |
| CACHE_RETENTION | INTEGER | Displays the cache refresh interval in minutes. |
| CACHE_FILTER | NCLOB | Displays the filter condition specified to reduce the cache size. |
| CACHE_LOCATIONS | VARCHAR(5000) | Displays the cache entry locations. |
| IS_CACHE_FORCED | VARCHAR(5) | Indicates whether the cached is forced or if cachability is checked: TRUE/ FALSE. |

## Related Information

RESULT_CACHE_COLUMNS System View [→](RESULT_CACHE_COLUMNS-System-View.md) M_RESULT_CACHE System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md) M_RESULT_CACHE_RESET System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE_RESET-System-View.md) M_RESULT_CACHE_EXCLUSIONS System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE_EXCLUSIONS-System-View.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-Statement-System.md)
