# 6.1.165 TABLE_PLACEMENT System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1594–1595

Provides table placement information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| GROUP_NAME | NVARCHAR(256) | Displays the group name. |
| GROUP_TYPE | NVARCHAR(256) | Displays the group type. |
| SUBTYPE | NVARCHAR(256) | Displays the subtype. |
| MIN_ROWS_FOR_PARTITIONING | BIGINT | Displays the minimum number of rows for partitioning. |
| INITIAL_PARTITIONS | INTEGER | Displays the initial number of partitions. |
| REPARTITIONING_THRESHOLD | BIGINT | Displays the repartitioning threshold. |
| LOCATION | VARCHAR(256) | Displays the location. |
| DYNAMIC_RANGE_THRESHOLD | BIGINT | Displays the dynamic range threshold. |
| SAME_PARTITION_COUNT | VARCHAR(5) | Displays whether to use the same count of partitions for each table belonging to the group: TRUE/FALSE. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays whether or not the data is loaded in persistent memory: TRUE/ FALSE. |
| PAGE_LOADABLE | VARCHAR(5) | Displays whether or not the data is page loadable: TRUE/FALSE. |
| REPLICA_COUNT | INTEGER | Sets the required number of replicas. |
| NUMA_NODE_INDEXES | NVARCHAR(5000) | Sets the allowed numa nodes. |

## Related Information

ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md) TABLES System View [→](TABLES-System-View.md) TABLE_PLACEMENT System View [→](TABLE_PLACEMENT-System-View.md) TABLE_PLACEMENT_LOCATIONS System View [→](TABLE_PLACEMENT_LOCATIONS-System-View.md) M_TABLE_PLACEMENT_LOCATIONS System View [→](../6.02-Monitoring-Views/M_TABLE_PLACEMENT_LOCATIONS-System-View.md) M_TABLE_LOCATIONS System View [→](../6.02-Monitoring-Views/M_TABLE_LOCATIONS-System-View.md)
