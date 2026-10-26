# 6.2.53 M_CONVERTER_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1704–1706

Provides converter statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| TYPE | VARCHAR(32) | Displays the type of converter. |
| MAX_LEVEL | BIGINT | Displays the maximum level. For example, the root page level. |
| MAX_PAGENUMBER | BIGINT | Displays the maximum page number in HEXID. |
| ALLOCATED_PAGE_COUNT | BIGINT | Displays the number of currently allocated pages. |
| ALLOCATED_PAGE_SIZE | BIGINT | Displays the total size, in bytes, of the currently allocated pages. |
| MAX_ALLOCATED_PAGE_COUNT | BIGINT | Displays the maximum number of allocated pages. |
| MAX_ALLOCATED_PAGE_SIZE | BIGINT | Displays the maximum size, in bytes, of the allocated pages. |
| ALLOCATE_PAGE_COUNT | BIGINT | Displays the number of page allocations. |
| ALLOCATE_OR_GET_STATIC_PAGE_COUNT | BIGINT | Displays the number of page allocations or retrievals during the static phase. |
| DEALLOCATE_PAGE_COUNT | BIGINT | Displays the number of page deallocations. |
| ASSIGN_PHYSICAL_PAGE_COUNT | BIGINT | Displays the number of physical page assignments. |
| UNASSIGN_PHYSICAL_PAGE_COUNT | BIGINT | Displays the number of physical page unassignments. |
| UNASSIGN_PHYSICAL_PAGE_COUNT_DURING_DROP_SNAPSHOT | BIGINT | Displays the number of physical page unassignments during a drop snapshot. |
| CREATE_SNAPSHOT_COUNT | BIGINT | Displays the number of created snapshots. |
| DROP_SNAPSHOT_COUNT | BIGINT | Displays the number of dropped snapshots. |
| WRITE_CONVERTERPAGE_LEVEL0_COUNT | BIGINT | Displays the number of level 0 converter pages written to the disk. |
| WRITE_CONVERTERPAGE_LEVEL1_COUNT | BIGINT | Displays the number of level 1 converter pages written to the disk. |
| WRITE_CONVERTERPAGE_LEVEL2_COUNT | BIGINT | Displays the number of level 2 converter pages written to the disk. |
| WRITE_CONVERTERPAGE_LEVEL3_COUNT | BIGINT | Displays the number of level 3 converter pages written to the disk. |
| WRITE_CONVERTERPAGE_LEVEL4_COUNT | BIGINT | Displays the number of level 4 converter pages written to the disk. |

## Additional Information

This view contains information about the converter, which administers logical page numbers and maps them to physical pages within the DataVolumes.

This view has a resettable counterpart; you can see the values since the last reset in the M_CONVERTER_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_CONVERTER_STATISTICS_RESET;`.

## Related Information

M_CONVERTER_STATISTICS_RESET System View [→](M_CONVERTER_STATISTICS_RESET-System-View.md) M_PAGEACCESS_STATISTICS System View [→](M_PAGEACCESS_STATISTICS-System-View.md) M_DATA_VOLUME_PAGE_STATISTICS System View [→](M_DATA_VOLUME_PAGE_STATISTICS-System-View.md) CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md) CONVERT_INTERNAL_TYPE_INTO_NAME System View [→](../6.01-System-Views/CONVERT_INTERNAL_TYPE_INTO_NAME-System-View.md)
