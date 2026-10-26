# 6.2.177 M_MEMORY_RECLAIM_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1897–1900

Provides statistics for reclaiming memory (for example, defragmentation, unloading of memory objects, and so on).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| MEMORY_RECLAIM_COUNT | BIGINT | Displays the number of memory re claims. |
| LAST_MEMORY_RECLAIM_DURATION | BIGINT | Displays the time needed in milliseconds to reclaim memory for the last allocation. |
| MAX_MEMORY_RECLAIM_DURATION | BIGINT | Displays the longest time needed in milliseconds to reclaim memory for the allocation. |
| MIN_MEMORY_RECLAIM_DURATION | BIGINT | Displays the shortest time needed in milliseconds to reclaim memory for the allocation. |
| SUM_MEMORY_RECLAIM_DURATION | BIGINT | Displays the total time needed in milliseconds to reclaim memory for all allocations. |
| AVG_MEMORY_RECLAIM_DURATION | BIGINT | Displays the average time needed in milliseconds to reclaim memory for the allocation. |
| LAST_SYNCHRONIZATION_DURATION | BIGINT | Displays the last wait time in milliseconds while other thread/process re claims memory. |
| MAX_SYNCHRONIZATION_DURATION | BIGINT | Displays the longest wait time in milliseconds while other thread/process re claims memory. |
| MIN_SYNCHRONIZATION_DURATION | BIGINT | Displays the shortest wait time in milliseconds while other thread/process re claims memory. |
| SUM_SYNCHRONIZATION_DURATION | BIGINT | Displays the total wait time in milliseconds while other thread/process re claims memory. |
| AVG_SYNCHRONIZATION_DURATION | BIGINT | Displays the average wait time in milliseconds while other thread/process re claims memory. |
| LAST_DEFRAGMENTATION_DURATION | BIGINT | Displays the duration in milliseconds of the last defragmentation. |
| MAX_DEFRAGMENTATION_DURATION | BIGINT | Displays the longest duration in milliseconds of defragmentation. |
| MIN_DEFRAGMENTATION_DURATION | BIGINT | Displays the shortest duration in milliseconds of defragmentation. |
| SUM_DEFRAGMENTATION_DURATION | BIGINT | Displays the total duration in milliseconds of defragmentation. |
| AVG_DEFRAGMENTATION_DURATION | BIGINT | Displays the average duration in milliseconds of defragmentation. |
| LAST_DEFRAGMENTATION_SIZE | BIGINT | Displays the size in bytes freed by the last defragmentation. |
| MAX_DEFRAGMENTATION_SIZE | BIGINT | Displays the largest size in bytes freed by defragmentation. |
| MIN_DEFRAGMENTATION_SIZE | BIGINT | Displays the smallest size in bytes freed by defragmentation. |
| SUM_DEFRAGMENTATION_SIZE | BIGINT | Displays the total size freed in bytes by defragmentation). |
| AVG_DEFRAGMENTATION_SIZE | BIGINT | Displays the average size in bytes freed by defragmentation. |
| LAST_MEMORY_OBJECT_UNLOAD_DURATION | BIGINT | Displays the duration in milliseconds of the last unload. Also see view M_MEMORY_OBJECTS. |
| MAX_MEMORY_OBJECT_UNLOAD_DURATION | BIGINT | Displays the longest duration in milliseconds of all unloads. Also see view M_MEMORY_OBJECTS. |
| MIN_MEMORY_OBJECT_UNLOAD_DURATION | BIGINT | Displays the shortest duration in milliseconds of all unloads. Also see view M_MEMORY_OBJECTS. |
| SUM_MEMORY_OBJECT_UNLOAD_DURATION | BIGINT | Displays the total duration in milliseconds of all unloads. Also see view M_MEMORY_OBJECTS. |
| AVG_MEMORY_OBJECT_UNLOAD_DURATION | BIGINT | Displays the average duration in milliseconds of all unloads. Also see view M_MEMORY_OBJECTS. |
| LAST_MEMORY_OBJECT_UNLOAD_SIZE | BIGINT | Displays the size in bytes freed by the last unloading of memory objects. Also see view M_MEMORY_OBJECTS. |
| MAX_MEMORY_OBJECT_UNLOAD_SIZE | BIGINT | Displays the largest size in bytes freed by unloading memory objects. Also see view M_MEMORY_OBJECTS. |
| MIN_MEMORY_OBJECT_UNLOAD_SIZE | BIGINT | Displays the smallest size in bytes freed by unloading memory objects. Also see view M_MEMORY_OBJECTS. |
| SUM_MEMORY_OBJECT_UNLOAD_SIZE | BIGINT | Displays the total size in bytes freed by unloading memory objects. Also see view M_MEMORY_OBJECTS. |
| AVG_MEMORY_OBJECT_UNLOAD_SIZE | BIGINT | Displays the average size in bytes freed by unloading memory objects. also see view M_MEMORY_OBJECTS. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_MEMORY_RECLAIM_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_MEMORY_RECLAIM_STATISTICS_RESET;`.

## Related Information

M_MEMORY_RECLAIM_STATISTICS_RESET System View [→](M_MEMORY_RECLAIM_STATISTICS_RESET-System-View.md) M_MEMORY System View [→](M_MEMORY-System-View.md) CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md)

REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md)
