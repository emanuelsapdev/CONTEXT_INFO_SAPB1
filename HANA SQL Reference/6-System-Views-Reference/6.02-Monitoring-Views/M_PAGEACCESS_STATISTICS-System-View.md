# 6.2.196 M_PAGEACCESS_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1920–1921

Provides PageAccess statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| TYPE | VARCHAR(32) | Displays the type of pageaccess. |
| CHUNK_SIZE | INTEGER | Displays the chunk size in bytes. |
| ALLOCATE_COUNT | BIGINT | Displays the number of allocations. |
| GET_COUNT | BIGINT | Displays the number of gets. |
| LOAD_COUNT | BIGINT | Displays the number of synchronous loads. |
| TRIGGER_LOAD_COUNT | BIGINT | Displays the number of asynchronous loads. |
| DEALLOCATE_COUNT | BIGINT | Displays the number of deallocations. |

## Additional Information

This view contains information about pages accessed:

- TYPE specifies the pageaccess.
- The \*_COUNT values are the number of the respective operations on the page access.
- CHUNK_SIZE is the number of pages accessed by one operation (CHUNK_SIZE is 1 except for RowStorePageAccess, where blocks of pages are accessed. For example, LOAD_COUNT=4 and CHUNK_SIZE=1024 means that 2\*1024=4096 pages had been loaded). the corresponding Converter is accessed on allocation and deallocation.

This view has a resettable counterpart; you can see the values since the last reset in the M_PAGEACCESS_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_PAGEACCESS_STATISTICS_RESET;`.

## Related Information

M_PAGEACCESS_STATISTICS_RESET System View [→](M_PAGEACCESS_STATISTICS_RESET-System-View.md) ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_CONVERTER_STATISTICS System View [→](M_CONVERTER_STATISTICS-System-View.md)
