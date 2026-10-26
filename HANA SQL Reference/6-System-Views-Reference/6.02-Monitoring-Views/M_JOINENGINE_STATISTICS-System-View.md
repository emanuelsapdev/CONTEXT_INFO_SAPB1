# 6.2.140 M_JOINENGINE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1835–1836

Provides statistics about join engine runtime objects used for column store join operations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| TRANSLATION_TABLE_COUNT | BIGINT | Displays the number of translation tables. |
| TRANSLATION_TABLE_MEMORY_SIZE | BIGINT | Displays the memory used by translation tables in bytes. |
| TRANSLATION_TABLE_UNLOAD_COUNT | BIGINT | Displays the number of translation table unloads. |

## Related Information

M_JOIN_DATA_STATISTICS System View [→](M_JOIN_DATA_STATISTICS-System-View.md) M_JOIN_TRANSLATION_TABLES System View [→](M_JOIN_TRANSLATION_TABLES-System-View.md) M_TABLE_PRUNING_STATISTICS System View [→](M_TABLE_PRUNING_STATISTICS-System-View.md)
