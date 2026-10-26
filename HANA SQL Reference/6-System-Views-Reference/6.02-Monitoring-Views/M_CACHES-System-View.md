# 6.2.26 M_CACHES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1667–1669

Provides aggregated information on caches.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| CACHE_ID | VARCHAR(128) | Displays the unique identifier for the cache. |
| TOTAL_SIZE | BIGINT | Displays the maximum available memory budget in bytes available for the cache instance. |
| USED_SIZE | BIGINT | Displays the memory in bytes used by the cache instance. |
| ENTRY_COUNT | BIGINT | Displays the number of entries in the cache instance. |
| INSERT_COUNT | BIGINT | Displays the number of insertions into the cache instance. |
| INVALIDATE_COUNT | BIGINT | Displays the number of invalidations in the cache instance. |
| HIT_COUNT | BIGINT | Displays the number of cache hits for the cache instance. |
| MISS_COUNT | BIGINT | Displays the number of cache misses for the cache instance. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_CACHES_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_CACHES_RESET;`.

## Related Information

ALTER SYSTEM CLEAR CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-CACHE-Statement-System-Management.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR SQL PLAN CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-SQL-PLAN-CACHE-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REMOVE SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-SQL-PLAN-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR TIMEZONE CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TIMEZONE-CACHE-Statement-System.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md) ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-Statement-System.md) ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECOMPILE-SQL-PLAN-CACHE-ENTRY-Statement.md) ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PIN-UNPIN-SQL-PLAN-CACHE-ENTRY-Statement.md) M_DYNAMIC_RESULT_CACHE System View [→](M_DYNAMIC_RESULT_CACHE-System-View.md) M_SQL_PLAN_CACHE_PARAMETERS System View [→](M_SQL_PLAN_CACHE_PARAMETERS-System-View.md) M_CACHE_ENTRIES System View [→](M_CACHE_ENTRIES-System-View.md)
