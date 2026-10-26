# 6.1.164 TABLE_PARTITIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1591–1594

Partitionspecific information for partitioned tables.

## Structure

| **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| NODE_ID | INTEGER | Displays the ID of the partition node. |
| PARENT_NODE_ID | INTEGER | Displays the ID of the parent node. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| LEVEL_1_PARTITION | INTEGER | Displays the first level partition ID. Possible values are 1 through the number of firstlevel partitions. First-level partitions (those used in ALTER TA BLE...MOVE) may have subpartitions. Displays the logical partition ID. Possible values are 1 through the number of partitions for partitioned tables. This is the ID shown in all monitoring views. |
| LEVEL_2_PARTITION | INTEGER | Displays the subpartition ID. Possible values are 0 for tables without multilevel partitioning and 1 through the number of subpartitions for partitioned tables with multilevel partitioning. |
| LEVEL_1_RANGE_MIN_VALUE | NVARCHAR(5000) | Displays the minimum value of the range partition at the first level for a range-partitioned table; empty other wise. |
| LEVEL_1_RANGE_MAX_VALUE | NVARCHAR(5000) | Displays the exclusive maximum value of the range partition at the first level for a range-partitioned table; empty otherwise. This value is not included in the range. |
| LEVEL_2_RANGE_MIN_VALUE | NVARCHAR(5000) | Displays the minimum value of the range partition at the second level for a range-partitioned table; empty other wise. |
| LEVEL_2_RANGE_MAX_VALUE | NVARCHAR(5000) | Displays the exclusive maximum value of the range partition at the second level for a range-partitioned table; empty otherwise. This value is not included in the range. |
| IS_CURRENT | VARCHAR(5) | Displays whether the partition is the current partition: TRUE/FALSE. |
| UNIQUE_CONSTRAINTS | VARCHAR(5) | Displays if unique constraints are checked for this partition or not: TRUE/ FALSE. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for partition: PAGE (when the partition uses page loadable storage), COLUMN (when the partition uses column loadable storage), or DEFAULT. |
| INSERT | VARCHAR(5) | Displays whether INSERT statements are allowed on the partition: TRUE/ FALSE. |
| STORAGE_TYPE | VARCHAR(8) | Displays the storage type for the partition: DEFAULT/EXTENDED. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays the userspecified persistent memory preference: TRUE (persistent memory is ON)/FALSE (persistent memory OFF). If the user has not speci fied a persistent memory preference, or if the preference is set to the default, then the value is NULL. |
| NUMA_NODE_INDEXES | VARCHAR (1024) | Displays a comma-separated list of userspecified logical NUMA node indexes for the table partition. The elements of the list are either individual nodes indexes or ranges of index nodes, or a mixture of both. For example, the value `0, 1 TO 3, 6` indicates node indexes 0, 1, 2, 3, and 6. |
| GROUP_TYPE | NVARCHAR(256) | Displays the group type. |
| SUBTYPE | NVARCHAR(256) | Displays the group subtype. |
| GROUP_NAME | NVARCHAR(256) | Displays the group name. |

## Additional Information

You must have the DATA ADMIN system privilege to see table information, unless you own or have SELECT permission on the tables.

## Related Information

TABLES System View [→](TABLES-System-View.md) M_TABLE_PARTITIONS System View [→](../6.02-Monitoring-Views/M_TABLE_PARTITIONS-System-View.md) M_TABLE_PARTITION_STATISTICS System View [→](../6.02-Monitoring-Views/M_TABLE_PARTITION_STATISTICS-System-View.md) Heterogeneous Create Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.02-Heterogeneous-Create-Partition-Clauses.md) Heterogeneous Alter Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/4.10.01.20.02-Heterogeneous-Alter-Partition-Clauses.md) Non-heterogeneous Create Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.01-Non-heterogeneous-Create-Partition-Clauses.md) Non-heterogeneous Alter Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/4.10.01.20.01-Non-heterogeneous-Alter-Partition-Clauses.md)
