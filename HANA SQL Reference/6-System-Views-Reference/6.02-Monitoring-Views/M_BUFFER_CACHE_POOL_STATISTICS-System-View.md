# 6.2.22 M_BUFFER_CACHE_POOL_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1664–1665

Provides statistics for each buffer pool in a cache.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the volume identifier for the index server. |
| CACHE_NAME | VARCHAR(16) | Displays the cache name: C/S, R/S. |
| BUFFER_SIZE | BIGINT | Displays the size of the buffer in the pool in bytes. |
| REPLACEMENT_POLICY | VARCHAR(16) | Displays the type of replacement policy used by the cache. |
| GROWTH_PERCENT | INTEGER | Displays the rate, as a percentage, at which the buffer pool can grow:<br> `TOTAL_BUFFER_COUNT =TOTAL_BUFFER_COUNT +GROWTH PERCENT / 100 *MAX_SIZE` |
| TOTAL_BUFFER_COUNT | BIGINT | Displays the number of buffers allocated to the pool. |
| FREE_BUFFER_COUNT | BIGINT | Displays the number of free buffers for the pool. |
| LRU_LIST_BUFFER_COUNT | BIGINT | Displays the number of buffers in the LRU chain for the pool. |
| HOT_BUFFER_COUNT | BIGINT | Displays the number of buffers in the hot buffer list for the pool. |
| BUFFER_REUSE_COUNT | BIGINT | Displays the number of buffers released from the LRU list for the pool so that a requested page can be cached. |
| OUT_OF_BUFFER_COUNT | BIGINT | Displays the number of times that an outofbuffer situation occurred while requesting buffers from the pool. |

## Related Information

M_BUFFER_CACHE_POOL_STATISTICS_RESET System View [→](M_BUFFER_CACHE_POOL_STATISTICS_RESET-System-View.md) M_BUFFER_CACHE_STATISTICS System View [→](M_BUFFER_CACHE_STATISTICS-System-View.md) M_BUFFER_CACHE_STATISTICS_RESET System View [→](M_BUFFER_CACHE_STATISTICS_RESET-System-View.md) M_LOG_BUFFERS System View [→](M_LOG_BUFFERS-System-View.md)
