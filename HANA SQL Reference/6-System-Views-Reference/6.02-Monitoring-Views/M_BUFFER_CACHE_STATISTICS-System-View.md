# 6.2.24 M_BUFFER_CACHE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1666–1667

Provides a cache level overview of the configuration, cache status, and memory usage.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the volume identifier for the index server. |
| CACHE_NAME | VARCHAR(16) | Displays the cache name: C/S or R/S. |
| STATE | VARCHAR(16) | Displays the cache state: ENABLED, DISABLING, DISABLED, or SHRINKING. |
| REPLACEMENT_POLICY | VARCHAR(16) | Displays the type of replacement policy used by the cache. |
| MAX_SIZE | BIGINT | Displays the maximum buffer cache memory capacity in bytes. |
| ALLOCATED_SIZE | BIGINT | Displays the allocated memory for the buffer cache in bytes. |
| USED_SIZE | BIGINT | Displays the used memory in buffer cache in bytes. |
| BUFFER_REUSE_COUNT | BIGINT | Displays the number of times that a buffer is released for reuse by the cache. |
| HIT_RATIO | FLOAT | Displays the ratio of pages found in the buffer cache to pages requested from the buffer cache. |

## Related Information

M_BUFFER_CACHE_POOL_STATISTICS System View [→](M_BUFFER_CACHE_POOL_STATISTICS-System-View.md) M_BUFFER_CACHE_POOL_STATISTICS_RESET System View [→](M_BUFFER_CACHE_POOL_STATISTICS_RESET-System-View.md) M_BUFFER_CACHE_STATISTICS_RESET System View [→](M_BUFFER_CACHE_STATISTICS_RESET-System-View.md)

[M_LOG_BUFFERS System View](M_LOG_BUFFERS-System-View.md)
