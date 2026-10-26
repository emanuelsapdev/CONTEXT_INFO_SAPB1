# 6.1.59 DYNAMIC_RESULT_CACHE_INDEX_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1469

Provides information about the indexes of dynamic result caches.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_OID | BIGINT | Displays the object ID. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the indexed column. |

## Related Information

DYNAMIC_RESULT_CACHE System View [→](DYNAMIC_RESULT_CACHE-System-View.md) M_DYNAMIC_RESULT_CACHE System View [→](../6.02-Monitoring-Views/M_DYNAMIC_RESULT_CACHE-System-View.md) M_DYNAMIC_RESULT_CACHE_EXCLUSIONS System View [→](../6.02-Monitoring-Views/M_DYNAMIC_RESULT_CACHE_EXCLUSIONS-System-View.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md)
