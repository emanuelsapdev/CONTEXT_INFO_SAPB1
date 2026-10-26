# 6.2.122 M_HEAP_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1809–1812

Provides memory allocator statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| CATEGORY | VARCHAR(128) | Displays the allocator name. |
| DEPTH | BIGINT | Displays the depth. |
| INCLUSIVE_SIZE_IN_USE | BIGINT | Displays the current size of this allocator, including suballocators in bytes. |
| INCLUSIVE_COUNT_IN_USE | BIGINT | Displays the number of blocks currently in use, including suballocators. |
| INCLUSIVE_ALLOCATED_SIZE | BIGINT | Displays the stotal allocated size in this allocator and suballocators in bytes. |
| INCLUSIVE_DEALLOCATED_SIZE | BIGINT | Displays the total deallocated size in this allocator and suballocators in bytes. |
| INCLUSIVE_ALLOCATED_COUNT | BIGINT | Displays the number of allocations, including suballocators. |
| INCLUSIVE_DEALLOCATED_COUNT | BIGINT | Displays the number of deallocations, including suballocators. |
| INCLUSIVE_MAX_SINGLE_ALLOCATION_SIZE | BIGINT | Displays the largest block size in bytes ever alllocated in this allocator and sub allocators. |
| INCLUSIVE_PEAK_ALLOCATION_SIZE | BIGINT | Displays the largest size in bytes of this allocator and suballocators (estimate). |
| INCLUSIVE_IN_USE_INTEGRAL | BIGINT | Displays the average allocated memory in bytes by this allocator and its suballocators, multiplied by the time since the start of measurement (sample based rough estimate). Deactivated by default this value should only be activated upon request by SAP support. UOM is 1 byte times 1 second. |
| EXCLUSIVE_SIZE_IN_USE | BIGINT | Displays the current size of this allocator in bytes. |
| EXCLUSIVE_COUNT_IN_USE | BIGINT | Displays the number of blocks currently in use. |
| EXCLUSIVE_ALLOCATED_SIZE | BIGINT | Displays the total allocated size in this allocator in bytes. |
| EXCLUSIVE_DEALLOCATED_SIZE | BIGINT | Displays the total deallocated size in this allocator in bytes. |
| EXCLUSIVE_ALLOCATED_COUNT | BIGINT | Displays the number of allocations. |
| EXCLUSIVE_DEALLOCATED_COUNT | BIGINT | Displays the number of deallocations. |
| EXCLUSIVE_MAX_SINGLE_ALLOCATION_SIZE | BIGINT | Displays the largest block size in bytes ever allocated in this allocator. |
| EXCLUSIVE_PEAK_ALLOCATION_SIZE | BIGINT | Displays the largest size of this allocator (estimate) in bytes. |
| EXCLUSIVE_ALLOC_ERRORS | BIGINT | Displays the number of allocation errors. |
| EXCLUSIVE_IN_USE_INTEGRAL | BIGINT | Displays the average allocated memory in bytes by this allocator, multiplied by time since start of measurement (sam ple based rough estimate). Deactivaetd by decault, this value should only be activated upon request by SAP support. UOM is 1 byte times 1 second. |
| MALLOC_PROXY_CACHE_MISSES | BIGINT | Deprecated. |
| FLAGS | VARCHAR(64) | Displays the allocator flags. |
| COMPONENT | VARCHAR(64) | Displays the name of SAP HANA component of this allocator. |

## Additional Information

This view contains information about memory consumption of various components in the system. Parallel to heap memory, you can also query memory consumption by connection, statement, and user using the M_CONTEXT_MEMORY system view.

The overhead of allocators is not considered in this view.

This view has a resettable counterpart; you can see the values since the last reset in the M_HEAP_MEMORY_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_HEAP_MEMORY_RESET;`.

## Related Information

M_HEAP_MEMORY_RESET System View [→](M_HEAP_MEMORY_RESET-System-View.md) M_HEAP_MEMORY_AREAS System View [→](M_HEAP_MEMORY_AREAS-System-View.md)

M_CONTEXT_MEMORY System View [→](M_CONTEXT_MEMORY-System-View.md) M_SERVICE_MEMORY System View [→](M_SERVICE_MEMORY-System-View.md)
