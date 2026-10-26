# 6.2.89 M_DYNAMIC_RESULT_CACHE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1763–1765

Lists statistics for the dynamic result cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CACHE_ID | BIGINT | Displays the unique ID for each dynamic result cache entry. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the dynamic result cache entry belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name that the dynamic result cache entry belongs to. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type that the dynamic result cache entry belongs to. |
| DETAILS | NVARCHAR(5000) | Displays the details of all of the constituents of the cache key. |
| LAST_MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the last cached MVCC snapshot timestamp. |
| MEMORY_SIZE | BIGINT | Displays the size, in bytes, of the memory occupied by the dynamic result cache entry. |
| MEMORY_SIZE_IN_INDEX | BIGINT | Displays the size, in bytes, of the memory occupied by the dynamic result cache entry's indexes. |
| RECORD_COUNT | BIGINT | Displays the number of records in the cache entry. |
| DELTA_RECORD_COUNT | BIGINT | Displays the number of records in the cache entry created by a delta refresh. |
| IS_REFRESHING | VARCHAR(5) | Displays the status of the asynchronous cache entry refresh job. The result is TRUE if the refresh job is currently running and FALSE otherwise. |
| CURRENT_REFRESH_DURATION | BIGINT | Displays the duration, in milliseconds, of the currently running cache entry refresh job. The value is 1 when IS_REFRESHING is FALSE. |
| CURRENT_REFRESH_REASON | VARCHAR(32) | Displays the reason why the refresh job was triggered. The value is empty when IS_REFRESHING is FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the timestamp when the dynamic result cache entry was created. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the timestamp when the last cache entry refresh job finished. |
| LAST_REFRESH_DURATION | BIGINT | Displays the duration, in milliseconds, of the last cache entry refresh job. |
| LAST_REFRESH_REASON | VARCHAR(32) | Displays the reason why the last refresh job was triggered. |
| LAST_DELTA_REFRESH_TIME | TIMESTAMP | Displays the timestamp when the last delta refresh on the cache entry finished. |
| LAST_ACCESS_TIME | TIMESTAMP | Displays the timestamp of the last cache entry access. |
| REFRESH_COUNT | BIGINT | Displays the number of refreshes on the cache entry. |
| DELTA_REFRESH_COUNT | BIGINT | Displays the number of delta refreshes on the cache entry. |
| ACCESS_COUNT | BIGINT | Displays the number of read accesses on the cache entry. |
| MISS_COUNT | BIGINT | Displays the number of cache miss read accesses on the cache entry. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

DYNAMIC_RESULT_CACHE System View [→](../6.01-System-Views/DYNAMIC_RESULT_CACHE-System-View.md) M_DYNAMIC_RESULT_CACHE_EXCLUSIONS System View [→](M_DYNAMIC_RESULT_CACHE_EXCLUSIONS-System-View.md) DYNAMIC_RESULT_CACHE_INDEX_COLUMNS System View [→](../6.01-System-Views/DYNAMIC_RESULT_CACHE_INDEX_COLUMNS-System-View.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md)
