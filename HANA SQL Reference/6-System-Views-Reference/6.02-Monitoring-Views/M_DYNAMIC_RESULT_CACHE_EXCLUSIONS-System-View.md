# 6.2.90 M_DYNAMIC_RESULT_CACHE_EXCLUSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1765–1767

Lists cache exclusions of the dynamic result cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the dynamic result cache entry belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name that the dynamic result cache entry belongs to. |
| DETAILS | NVARCHAR(5000) | Lists all constituents of the excluded cache key. |
| MEMORY_SIZE | BIGINT | Displays the size, in bytes, of the memory occupied by the excluded cache en try. |
| RECORD_COUNT | BIGINT | Displays the number of records in the excluded cache entry. |
| EXCLUDE_TIME | TIMESTAMP | Displays the timestamp when the dynamic result cache entry was decided. |

## Additional Information

Cache entries that exceed configurable size (defined in the `.ini` file) are automatically removed and added to M_DYNAMIC_RESULT_CACHE_EXCLUSION. If the view is marked to be excluded, then redefine the view definition rather than increasing the configurable size.

## Related Information

M_DYNAMIC_RESULT_CACHE System View [→](M_DYNAMIC_RESULT_CACHE-System-View.md) DYNAMIC_RESULT_CACHE System View [→](../6.01-System-Views/DYNAMIC_RESULT_CACHE-System-View.md) DYNAMIC_RESULT_CACHE_INDEX_COLUMNS System View [→](../6.01-System-Views/DYNAMIC_RESULT_CACHE_INDEX_COLUMNS-System-View.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md)
