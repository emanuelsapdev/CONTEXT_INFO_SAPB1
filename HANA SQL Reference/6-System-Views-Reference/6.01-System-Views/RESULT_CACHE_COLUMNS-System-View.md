# 6.1.140 RESULT_CACHE_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1560–1561

Provides information about columns available to use the result cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| CACHE_AGGREGATION_TYPE | VARCHAR(20) | Indicates the required aggregation type in a query to use cache or indicate an aggregation type for caching the column: SUM, MIN, MAX, or COUNT. |

## Related Information

RESULT_CACHE System View [→](RESULT_CACHE-System-View.md) M_RESULT_CACHE System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md) M_RESULT_CACHE_RESET System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE_RESET-System-View.md) M_RESULT_CACHE_EXCLUSIONS System View [→](../6.02-Monitoring-Views/M_RESULT_CACHE_EXCLUSIONS-System-View.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-Statement-System.md)
