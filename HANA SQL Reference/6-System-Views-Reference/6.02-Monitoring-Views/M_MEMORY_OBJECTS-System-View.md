# 6.2.173 M_MEMORY_OBJECTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1891–1893

Returns memory object statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| TYPE | VARCHAR(128) | Displays the object (statistic) type. |
| OBJECT_COUNT | BIGINT | Displays the number of objects currently in the memory object container. |
| OBJECT_SIZE | BIGINT | Displays the size of the objects that are currently in the memory object container in bytes. |
| NON_SWAPPABLE_SIZE | BIGINT | Displays the size of the non-swappable objects that are currently in the memory object container in bytes. |
| SWAPPABLE_SIZE | BIGINT | Displays the size of the swappable objects that are currently in the memory object container in bytes. |
| PUT_COUNT | BIGINT | Displays the total number of put objects. |
| PUT_SIZE | BIGINT | Displays the total size of put objects in bytes. |
| MOVE_IN_COUNT | BIGINT | Displays the total number of objects moved in from a different statistic. |
| MOVE_IN_SIZE | BIGINT | Displays the total size of objects moved in from a different statistic in bytes. |
| MOVE_OUT_COUNT | BIGINT | Displays the total number of objects moved out to a different statistic. |
| MOVE_OUT_SIZE | BIGINT | Displays the total size of objects moved out to a different statistic in bytes. |
| EVICT_COUNT | BIGINT | Displays the total number of evicted objects. |
| EVICT_SIZE | BIGINT | Displays the total size of evicted objects in bytes. |
| TEMP_EVICT_COUNT | BIGINT | Displays the total number of temp-evicted objects. |
| TEMP_EVICT_SIZE | BIGINT | Displays the total size of temp-evicted objects in bytes. |
| RESIZE_COUNT | BIGINT | Displays the total number of resizes of objects. |
| RESIZE_DELTA_SIZE | BIGINT | Displays the total size delta changed by the resize of the objects in bytes. |
| SHRINK_COUNT | BIGINT | Displays the total number of shrunken objects. |
| SHRINK_SIZE | BIGINT | Displays the total size of shrunken objects in bytes. |
| RETENTION_PERIOD_SHRINK_COUNT | BIGINT | Displays the total number of shrunken objects due to an unused retention period. |
| RETENTION_PERIOD_SHRINK_SIZE | BIGINT | Displays the total size of shrunken objects due to an unused retention period in bytes. |
| PAGE_LOADABLE_COLUMNS_LIMIT_SHRINK_COUNT | BIGINT | Displays the total number of shrunken objects due to a paged attribute limit violation. |
| PAGE_LOADABLE_COLUMNS_LIMIT_SHRINK_SIZE | BIGINT | Displays the total size of shrunken objects due to paged attribute limit violation in bytes. |
| FAILED_SHRINK_COUNT | BIGINT | Displays the total number of the objects that the shrink failed to remove. |
| FAILED_SHRINK_SIZE | BIGINT | Displays the total size of the objects that the shrink failed to remove in bytes. |

## Additional Information

This view provides information about the number and size of resources in the resource container and about the throughput of the resource container. One row in this view represents one resource type (the type is specified by the resource statistic). The resource statistics are kept in a tree data structure and this view represents this tree in a human-readable form. Each value (except for HOST, PORT, VOLUME_ID, and STATISTICS_NAME) is the AGGREGATED value of the subtree (including the current node).

This view has a resettable counterpart; you can see the values since the last reset in the M_MEMORY_OBJECTS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_MEMORY_OBJECTS_RESET;`.

## Related Information

M_MEMORY_OBJECTS_RESET System View [→](M_MEMORY_OBJECTS_RESET-System-View.md) M_MEMORY_OBJECT_DISPOSITIONS System View [→](M_MEMORY_OBJECT_DISPOSITIONS-System-View.md) M_MEMORY System View [→](M_MEMORY-System-View.md)
