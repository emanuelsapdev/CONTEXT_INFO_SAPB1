# 6.2.180 M_METADATA_CACHE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1902–1903

Provides information regarding the efficiency and use of the metadata cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the port number. |
| CACHE_GROUP_NAME | VARCHAR(64) | Displays the category name of the cache group. |
| ORIGIN_DATABASE_NAME | NVARCHAR(256) | Displays the name of the original data base that the cache group belongs to. |
| ACCESS_COUNT | BIGINT | Displays the access count of the cache group. |
| HIT_COUNT | BIGINT | Displays the cache hit count of the cache group. |
| EMPTY_HIT_COUNT | BIGINT | Displays the empty cache hit count of the cache group. |
| LATE_HIT_COUNT | BIGINT | Displays the duplicated metadata request count to the master node. This count only occurs in the race conditions of the thread. |
| NOT_FOUND_COUNT | BIGINT | Displays the empty result response count of the master node. |
| REVALIDATION_COUNT | BIGINT | Displays the revalidation count of old cache items. |
| MISS_COUNT | BIGINT | Displays the cache miss count of the cache group. |
| ENTRY_COUNT | BIGINT | Displays the total number of items in the cache group. |
| INVALID_ENTRY_COUNT | BIGINT | Displays the number of invalid cache items. These items are set to invalid and removed during the next garbage collection. |
| VALID_ENTRY_COUNT | BIGINT | Displays the number of valid cache items. |
| STALE_ENTRY_COUNT | BIGINT | Displays the number of stale cache items. These are set as expired by default at the expiration time. These items can be revalidated later or removed at the next garbage collection. |
| USED_MEMORY_SIZE | BIGINT | Displays the size of the memory occupied by the cache group in bytes. |

## Related Information

ALTER SYSTEM CLEAR CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-CACHE-Statement-System-Management.md) ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md)
