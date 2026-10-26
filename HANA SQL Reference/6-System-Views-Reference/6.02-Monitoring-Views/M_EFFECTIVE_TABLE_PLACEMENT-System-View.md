# 6.2.92 M_EFFECTIVE_TABLE_PLACEMENT System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1768–1769

Provides information about effective placement of tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema. |
| TABLE_NAME | NVARCHAR(256) | Displays the table. |
| RECORD_COUNT | BIGINT | Displays the record count. |
| TABLE_TYPE | NVARCHAR(256) | Displays the type. |
| GROUP_NAME | NVARCHAR(256) | Displays the group name. |
| GROUP_TYPE | NVARCHAR(256) | Displays the group type. |
| SUBTYPE | NVARCHAR(256) | Displays the sub type. |
| LOCATION | VARCHAR(75) | Displays the location. |
| POSSIBLE_LOCATION | VARCHAR(5000) | Displays the possible location. |
| LOCATION_MATCH | VARCHAR(41) | Displays a string representing the matching rule for the possible location. |
| MIN_ROWS_FOR_PARTITIONING | BIGINT | Displays the minimum row count for partitioning. |
| MIN_ROWS_FOR_PARTITIONING_MATCH | VARCHAR(41) | Displays a string representing the matching rule for the minimum row count for partitioning. |
| PARTITIONING_THRESHOLD | BIGINT | Displays the repartitioning threshold. |
| PARTITIONING_THRESHOLD_MATCH | VARCHAR(41) | Displays a string representing the matching rule for the repartitioning threshold. |
| INITIAL_PARTITION | INTEGER | Displays the initial partitions. |
| INITIAL_PARTITION_MATCH | VARCHAR(41) | Displays a string representing the matching rule for the initial partitions. |
| DYNAMIC_RANGE_THRESHOLD | BIGINT | Displays the dynamic range threshold. |
| DYNAMIC_RANGE_THRESHOLD_MATCH | VARCHAR(41) | Displays a string representing the matching rule for the dynamic range threshold. |

## Related Information

ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md) TABLE_PLACEMENT_LOCATIONS System View [→](../6.01-System-Views/TABLE_PLACEMENT_LOCATIONS-System-View.md) TABLE_PLACEMENT System View [→](../6.01-System-Views/TABLE_PLACEMENT-System-View.md)
