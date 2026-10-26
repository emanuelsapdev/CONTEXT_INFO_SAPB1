# 6.2.194 M_OUT_OF_MEMORY_EVENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1918–1919

Provides a list of the last 20 out-of-memory (OOM) events.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR (64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| TIME | TIMESTAMP | Displays the time of the OOM event. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| STATEMENT_ID | VARCHAR (20) | Displays the statement ID. |
| STATEMENT_HASH | VARCHAR (32) | Displays the identifier for an SQL string. |
| HEAP_MEMORY_CATEGORY | VARCHAR (128) | Displays the allocator name in case of a heap memory failure. |
| MEMORY_REQUEST_SIZE | BIGINT | Displays the size, in bytes, of the failed memory allocation. |
| MEMORY_USED_SIZE | BIGINT | Displays the size, in bytes, currently allocated. This value depends on the EVENT_REASON. |
| EVENT_REASON | VARCHAR (32) | Displays the reason for the OOM event: GLOBAL ALLOCATION LIMIT, PROCESS ALLOCATION LIMIT, or STATEMENT MEMORY LIMIT. |
| MEMORY_LIMIT_SIZE | BIGINT | Displays the size of the limit in bytes. This value depends on the EVENT_REASON. |
| TRACEFILE_NAME | VARCHAR (256) | Displays the OOM trace file name. |

## Related Information

[M_MEMORY System View](M_MEMORY-System-View.md)
