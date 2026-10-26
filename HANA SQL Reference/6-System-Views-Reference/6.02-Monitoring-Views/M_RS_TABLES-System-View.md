# 6.2.242 M_RS_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1970–1972

Provides information about row tables, including detailed table sizes and record count.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| RECORD_COUNT | BIGINT | Displays the number of records in this table. |
| ALLOCATED_FIXED_PART_SIZE | BIGINT | Displays the allocated memory size in bytes for the fixedsize part. |
| FIXED_PAGE_HEADER_SIZE | BIGINT | Displays the allocated and used memory size in bytes for the page headers of the fixedsize part. |
| FIXED_PAGE_FRAGMENT_SIZE | BIGINT | Displays the fragmented memory size in bytes of the fixedsize part. |
| USED_FIXED_PART_SIZE | BIGINT | Displays the used memory size in bytes for the fixedsize part. |
| FIXED_PART_FRAGMENT_SIZE | BIGINT | Displays the fragmented memory size in bytes of the used fixedsize part. |
| FIXED_PART_FREE_SIZE | BIGINT | Displays the free memory size in bytes in the pages of the fixedsize part. |
| ALLOCATED_VARIABLE_PART_SIZE | BIGINT | Displays the allocated memory size in bytes for the variable-size part. |
| USED_VARIABLE_PART_SIZE | BIGINT | Displays the used memory size in bytes for the variable-size part. |
| VARIABLE_PART_FRAGMENT_SIZE | BIGINT | Displays the fragmented memory size in bytes of the used variable-size part. |
| LOAD_STATUS | VARCHAR(32) | Displays the loading state of the table: LOADED, NOW_LOADING, PREPARING_UNLOAD, NOW_UNLOADING, UN LOADED, or NOT_SUPPORTED |
| IS_REPLICA | VARCHAR(5) | Displays the flag to indicate a replica. |
| CREATE_TIME | TIMESTAMP | Displays the create time of the table. |
| CONTAINER_COUNT | INTEGER | Displays the number of containers for the table. |
| SCAN_COUNT | BIGINT | Displays the number of table scans. |
