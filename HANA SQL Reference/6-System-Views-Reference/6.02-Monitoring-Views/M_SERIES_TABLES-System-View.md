# 6.2.251 M_SERIES_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1986–1987

Provides statistics on the physical contents of series tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the column table name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| SERIES_KEY_COUNT | BIGINT | Displays the number of distinct series identified by the SERIES KEY columns. |
| PERIOD_COUNT | BIGINT | Displays the number of distinct periods represented in the period column. |
| ROWS_EQUIDISTANT_COUNT | BIGINT | Displays the number of rows optimized to be in a piecewise equidistant segment. |
| ROWS_NOT_EQUIDISTANT_COUNT | BIGINT | Displays the number of rows that have not been optimized to be in a piecewise equidistant segment. |
| ROWS_REORGANIZED_COUNT | BIGINT | Displays the number of rows that have been optimized by the ALTER TABLE SERIES REORGANIZE statement. |
| ROWS_NOT_REORGANIZED_COUNT | BIGINT | Displays the number of rows that have not been processed by the ALTER TA BLE SERIES REORGANIZE statement. |

## Related Information

[ALTER TABLE Statement (Data Definition)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)
