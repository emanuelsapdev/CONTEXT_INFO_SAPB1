# 6.2.311 M_TABLE_PERSISTENCE_LOCATION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2084–2085

Provides persistence storage statistics for tables partitions and services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that the table schema is currently in being modified. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| DISK_SIZE | BIGINT | Displays the total disk size, in bytes, of all table parts. |
| PAGE_COUNT | BIGINT | Displays the total number of pages of all table parts. |
| BYTES_WRITTEN | BIGINT | Displays the number of bytes written to the table. |
| BYTES_APPENDED | BIGINT | Displays the number of bytes appended to the table. |
| BYTES_READ | BIGINT | Displays the number of bytes read from the table. |
| BYTESTREAM_WRITTEN | BIGINT | Displays the number of bytes written to the table via the streaming interface. |
| APPEND_COUNT | BIGINT | Displays the number of times the table was appended to. |
| WRITE_COUNT | BIGINT | Displays the number of times the table was written to. |
| OPTIMIZE_COUNT | BIGINT | Displays the number of times the table was written to be optimized. |
| READ_COUNT | BIGINT | Displays the number of times the table was read from. |
| TRUNCATE_COUNT | BIGINT | Displays the number of times the table was truncated. |
| COPY_COUNT | BIGINT | Displays the number of times the table was copied. |

## Related Information

M_TABLE_PERSISTENCE_STATISTICS System View [→](M_TABLE_PERSISTENCE_STATISTICS-System-View.md) M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS System View [→](M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS-System.md)
