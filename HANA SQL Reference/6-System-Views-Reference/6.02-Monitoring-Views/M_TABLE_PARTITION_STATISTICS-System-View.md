# 6.2.309 M_TABLE_PARTITION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2081–2082

Returns the table partition runtime statistics for column store partition tables only. This view is empty if the partition_statistics_select_enabled property in the `indexserver.ini` configuration file is disabled.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that the table schema is currently in being modified. |
| SELECT_COUNT | BIGINT | Displays the number of times a partition has been selected. |
| LAST_SELECT_TIME | TIMESTAMP | Displays the last time that this partition was selected. |

## Related Information

M_TABLE_PARTITIONS System View [→](M_TABLE_PARTITIONS-System-View.md) M_EXPENSIVE_STATEMENTS System View [→](M_EXPENSIVE_STATEMENTS-System-View.md) TABLE_PARTITIONS System View [→](../6.01-System-Views/TABLE_PARTITIONS-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md)
