# 6.2.123 M_HEAP_MEMORY_AREAS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1812

Provides memory fragmentation details.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| AREA | STRING | Identifies the part of the memory management being used, for example, the PoolAllocator. |
| USED_SIZED | BIGINT | Displays the bytes in use. |
| TOTAL_SIZE | BIGINT | Displays the total bytes in the area. |

## Related Information

M_HEAP_MEMORY System View [→](M_HEAP_MEMORY-System-View.md) M_CONTEXT_MEMORY System View [→](M_CONTEXT_MEMORY-System-View.md) M_SERVICE_MEMORY System View [→](M_SERVICE_MEMORY-System-View.md)
