# 6.2.29 M_CATALOG_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1670–1671

Provides memory usage information by catalog manager.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| CATEGORY | VARCHAR(128) | Displays the category of the catalog data. |
| ALLOCATION_COUNT | BIGINT | Displays the number of allocated en tries. |
| ALLOCATED_FIXED_PART_SIZE | BIGINT | Displays the allocated memory size in bytes for the fixedsize part. |
| USED_FIXED_PART_SIZE | BIGINT | Displays the used memory size in bytes for the fixedsize part. |
| ALLOCATED_VARIABLE_PART_SIZE | BIGINT | Displays the allocated memory size in bytes for the variable-size part. |
| USED_VARIABLE_PART_SIZE | BIGINT | Displays the used memory size in bytes for the variable-size part. |

## Related Information

[M_MEMORY System View](M_MEMORY-System-View.md)
