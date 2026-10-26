# 6.2.175 M_MEMORY_OBJECT_DISPOSITIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1894–1896

Displays the dispositionspecific memory object statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| TYPE | VARCHAR(128) | Displays the object statistic type. |
| CATEGORY | VARCHAR(128) | Displays the allocator category, the corresponding allocator, and some of its sub-allocators that were used to allocate the memory objects. |
| TEMPORARY_OBJECT_COUNT | BIGINT | Displays the number of temporary objects. |
| PAGE_LOADABLE_COLUMNS_OBJECT_COUNT | BIGINT | Displays the number of page loadable column objects. |
| EARLY_UNLOAD_OBJECT_COUNT | BIGINT | Displays the number of early unload objects. |
| INTERNAL_SHORT_TERM_OBJECT_COUNT | BIGINT | Displays the number of internal short term objects. |
| SHORT_TERM_OBJECT_COUNT | BIGINT | Displays the number of short term objects. |
| MID_TERM_OBJECT_COUNT | BIGINT | Displays the number of mid term objects. |
| LONG_TERM_OBJECT_COUNT | BIGINT | Displays the number of long term objects. |
| NON_SWAPPABLE_OBJECT_COUNT | BIGINT | Displays the number of non-swappable objects. |
| TEMPORARY_OBJECT_SIZE | BIGINT | Displays the size of the temporary objects in bytes. |
| PAGE_LOADABLE_COLUMNS_OBJECT_SIZE | BIGINT | Displays the size of page loadable column objects in bytes. |
| EARLY_UNLOAD_OBJECT_SIZE | BIGINT | Displays the size of the early unload objects in bytes. |
| INTERNAL_SHORT_TERM_OBJECT_SIZE | BIGINT | Displays the size of the internal short term objects in bytes. |
| SHORT_TERM_OBJECT_SIZE | BIGINT | Displays the size of the short term objects in bytes. |
| MID_TERM_OBJECT_SIZE | BIGINT | Displays the size of the mid term objects in bytes. |
| LONG_TERM_OBJECT_SIZE | BIGINT | Displays the size of the long term objects in bytes. |
| NON_SWAPPABLE_OBJECT_SIZE | BIGINT | Displays the size of the non swappable objects in bytes. |
| SHRINKABLE_OBJECT_COUNT | BIGINT | Displays the number of shrinkable objects. |
| SHRINKABLE_OBJECT_SIZE | BIGINT | Displays the size of the shrinkable objects in bytes. |

## Additional Information

The number and the size of the resources in the resource container are shown depending on their specific disposition (whether the memory objects are short, mid, long term, or non-swappable). For each type of resource that is specified by the resource statistic, which is currently in the resource container, one row is added to this view. The tree structure of the resource statistics is not considered here, therefore the values are not aggregated.

Reading this view may take some time as the entire resource container must be traversed to generate this view.

## Related Information

M_MEMORY_OBJECTS System View [→](M_MEMORY_OBJECTS-System-View.md) M_MEMORY_OBJECTS_RESET System View [→](M_MEMORY_OBJECTS_RESET-System-View.md) M_MEMORY System View [→](M_MEMORY-System-View.md)
