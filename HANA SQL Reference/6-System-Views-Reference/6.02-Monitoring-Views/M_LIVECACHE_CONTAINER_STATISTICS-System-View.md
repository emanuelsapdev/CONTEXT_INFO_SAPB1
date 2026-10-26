# 6.2.150 M_LIVECACHE_CONTAINER_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1852–1854

Provides accumulated liveCache container statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONTAINER_ID | BIGINT | Displays the container ID. |
| OMS_CLASS_ID | INTEGER | Displays the OMS class ID. |
| OMS_CLASS_NAME | VARCHAR(64) | Displays the OMS class name. |
| OMS_SCHEMA_HANDLE | INTEGER | Displays the OMS schema handle. |
| OMS_CONTAINER_NO | INTEGER | Displays the OMS container number. |
| CLASS_SIZE | BIGINT | Displays the object class size in bytes. |
| OBJECT_TYPE | VARCHAR(3) | Displays the object type: STD, KEY, or VAR. |

| INTEGER | Displays the object key size in bytes. |
| --- | --- |

KEY_SIZE

| KEY_PARTITION_COUNT | INTEGER | Displays the key partition count. |
| --- | --- | --- |
| KEY_PARTITION_PREFIX_SIZE | INTEGER | Displays the key partition prefix length in bytes. |
| CACHED_KEYS | VARCHAR(5) | Displays whether the cached keys are active: TRUE/FALSE. |

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COPY_ON_UPDATE | VARCHAR(5) | Displays whether copy on update is active: TRUE/FALSE. |
| PREFETCH | VARCHAR(5) | Indicates whether the prefetch is active: TRUE/FALSE. |
| IS_LOADED | VARCHAR(5) | Indicates whether the statistics are loaded into the memory: TRUE/FALSE. |
| OBJECT_COUNT | BIGINT | Displays the object count. |
| OBJECT_SIZE_SUM | BIGINT | Displays the object size sum in bytes. |
| GC_PENDING_OBJECT_DELETE_COUNT | BIGINT | Displays the count of objects that are deleted and not yet freed by the garbage collection. |
| GC_PENDING_OBJECT_DELETE_SIZE_SUM | BIGINT | Displays the transient size sum of the objects that are deleted and not yet freed by the garbage collection in bytes. |
| HISTORY_OBJECT_COUNT | BIGINT | Displays the number of transient history object versions that are not yet freed by the garbage collection. |
| HISTORY_SIZE_SUM | BIGINT | Displays the size sum, in bytes, of the transient history object versions that are not yet freed by the garbage collection. |
| PAGE_COUNT | BIGINT | Displays the page count. |
| PAGE_SIZE_SUM | BIGINT | Displays the page size sum in bytes. |
| OBJECT_CREATE_COUNT | BIGINT | Displays the number of objects created since the last restart. |
| OBJECT_UPDATE_COUNT | BIGINT | Displays the number of objects updated since the last restart. |
| OBJECT_DELETE_COUNT | BIGINT | Displays the number of objects delete since the last restart. |
| HEAP_USAGE | BIGINT | Displays the memory currently used by the container in bytes. |
| CREATE_TIME | TIMESTAMP | Displays the created timestamp. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_LIVECACHE_CONTAINER_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LIVECACHE_CONTAINER_STATISTICS_RESET;`.

## Related Information

M_LIVECACHE_CONTAINER_STATISTICS_RESET System View [→](M_LIVECACHE_CONTAINER_STATISTICS_RESET-System-View.md) ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md)
