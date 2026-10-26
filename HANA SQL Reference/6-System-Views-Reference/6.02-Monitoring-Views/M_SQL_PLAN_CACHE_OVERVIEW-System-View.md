# 6.2.278 M_SQL_PLAN_CACHE_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2030–2033

Provides overall statistics of evicted and cached plans

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| PLAN_CACHE_ENABLED | INTEGER | Displays whether the SQL Plan Cash is enabled (TRUE/FALSE).<br>ALTER SYSTEM ALTER CONFIGURA TION ('indexserver.ini','system') SET('sql', 'plan_cache_enabled') = <'True' or 'False'> WITH RECONFIG URE. |
| STATISTICS_COLLECTION_ENABLED | VARCHAR(5) | Displays whether the runtime statistics are being collected (TRUE/FALSE).<br>ALTER SYSTEM ALTER CONFIGURA TION ('indexserver.ini','system') SET('sql', 'plan_cache_statistics_ena bled') = <'True' or 'False'> WITH RE CONFIGURE. |
| PLAN_CACHE_CAPACITY | BIGINT | Displays the maximum SQL Plan Cache size in bytes.<br>ALTER SYSTEM ALTER CONFIGURA TION ('indexserver.ini','system') SET('sql', 'plan_cache_size') = '268435456' WITH RECONFIGURE. |
| CACHED_PLAN_SIZE | BIGINT | Displays the total size of SQL Plan Cache in bytes. |
| PLAN_CACHE_HIT_RATIO | REAL | Displays the SQL Plan Cache hit ratio. |
| PLAN_CACHE_LOOKUP_COUNT | BIGINT | Displays the number of plan lookup counts from SQL Plan Cache. |
| PLAN_CACHE_HIT_COUNT | BIGINT | Displays the number of hit counts from SQL Plan Cache. |
| EVICTED_PLAN_AVG_CACHE_TIME | BIGINT | Displays the average duration in microseconds between plan cache insertion and eviction. |
| EVICTED_PLAN_COUNT | BIGINT | Displays the number of evicted plans from SQL Plan Cache. |
| EVICTED_PLAN_PREPARATION_COUNT | BIGINT | Displays the total plan preparation count for evicted plans. |
| EVICTED_PLAN_EXECUTION_COUNT | BIGINT | Displays the total plan execution count for evicted plans. |
| EVICTED_PLAN_PREPARATION_TIME | BIGINT | Displays the total duration in microseconds for plan preparation for all evicted plans. It is the sum of the evicted plan's TOTAL_PREPARATION_TIME. |
| EVICTED_PLAN_CURSOR_DURATION | BIGINT | Displays the total cursor duration in microseconds for evicted plans. It is the sum of the evicted plan's TOTAL_CURSOR_DURATION. |
| EVICTED_PLAN_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time in microseconds for evicted plans. It is the sum of th evicted plan's TOTAL_EXECUTION_TIME. |
| EVICTED_PLAN_SIZE | BIGINT | Displays the accumulated total size of evicted plans in bytes. |
| CACHED_PLAN_COUNT | BIGINT | Displays the total cached plan count in SQL Plan Cache. |
| CACHED_PLAN_PREPARATION_COUNT | BIGINT | Displays the total plan preparation count for cached plans. |
| CACHED_PLAN_EXECUTION_COUNT | BIGINT | Displays the total execution count for cached plans. |
| CACHED_PLAN_PREPARATION_TIME | BIGINT | Displays the total plan preparation duration for cached plans in microseconds. |
| CACHED_PLAN_CURSOR_DURATION | BIGINT | Displays the total cursor duration for cached plans in microseconds. |
| CACHED_PLAN_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time for cached plans in microseconds. |
| CLEAR_TIMESTAMP | TIMESTAMP | Displays the timestamp when SQL Plan Cache was cleared for the last time using ALTER SYSTEM CLEAR SQL PLAN CACHE. |

## Additional Information

M_SQL_PLAN_CACHE_OVERVIEW shows the overall statistics of evicted and cached plans. It shows information such as how many times plan eviction occurred and how long it takes to execute currently cached plans. You can check the eviction rate with the EVICTED_PLAN_COUNT column. If EVICTED_PLAN_COUNT is too high, it means SQL plan cache capacity is not enough and too many compilations occurs.

In addition to statistics, the current status and flags of the SQL plan cache are shown in this view.

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_SQL_PLAN_CACHE_RESET System View [→](M_SQL_PLAN_CACHE_RESET-System-View.md) M_CONNECTIONS System View [→](M_CONNECTIONS-System-View.md)
