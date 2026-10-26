# 6.1.108 PARTITIONED_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1525–1527

Provides general partitioning information for all partitions of a table.

## Structure

| **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| LEVEL_1_EXPRESSION | NVARCHAR(5000) | Displays the partitioning expression for firstlevel partitions. |
| LEVEL_1_COUNT | INTEGER | Displays the total number of partitions at the first level. |
| LEVEL_1_TYPE | VARCHAR(16) | Displays the partitioning type at the first level: HASH, RANGE, ROUNDRO BIN, REPLICATE, or RANGE HETERO GENEOUS. |
| LEVEL_2_EXPRESSION | NVARCHAR(5000) | Displays the partitioning expression for second-level partitions. |
| LEVEL_2_COUNT | INTEGER | Displays the total number of partitions at the second level. |
| LEVEL_2_TYPE | VARCHAR(16) | Displays the partitioning type at the second level: HASH, RANGE, RANGE HETEROGENEOUS, or HASH HETERO GENEOUS. Heterogeneous indicates an unbalanced partitioning scheme. |
| CROSS_STORAGE_UNIQUE_CONSTRAINTS | VARCHAR(5) | Displays whether constraint checking is done across stores: TRUE/FALSE. |
| PARTITIONING_ON_NON_PRIMARY_KEY_COLUMNS | VARCHAR(5) | Displays whether partitioning is allowed on a non-primary key column: TRUE/ FALSE. This value is only relevant for tables with time-selection partitioning. |
| PRIMARY_KEY_UPDATE | VARCHAR(5) | Displays whether UPDATE statements are allowed on primary key columns: TRUE/FALSE. |
| DYNAMIC_RANGE_THRESHOLD | BIGINT | Displays the threshold after which a new partition is created dynamically. |
| EXTENDED_STORAGE_ENABLE_DELTA | VARCHAR(5) | Displays whether extended storage is enabled to use a delta store: TRUE, FALSE, or NULL. NULL means that the system couldn't retrieve the status from extended storage. |

## Additional Information

If you are using the dynamic tiering feature, then this monitoring view shows information for the extended storage corresponding to the connected SAP HANA database. The partitioning type is at the first level. Valid values are: HASH, RANGE, ROUNDROBIN, or REPLICATE.

You need the DATA ADMIN system privilege see information for tables owned by other users, unless you have SELECT permission on those tables.

## Related Information

TABLE_PARTITIONS System View [→](TABLE_PARTITIONS-System-View.md) M_TABLE_PARTITIONS System View [→](../6.02-Monitoring-Views/M_TABLE_PARTITIONS-System-View.md) M_TABLE_PARTITION_STATISTICS System View [→](../6.02-Monitoring-Views/M_TABLE_PARTITION_STATISTICS-System-View.md) M_CS_PARTITIONS System View - Deprecated [→](../6.02-Monitoring-Views/M_CS_PARTITIONS-System-View-Deprecated.md) TABLES System View [→](TABLES-System-View.md) M_TABLES System View [→](../6.02-Monitoring-Views/M_TABLES-System-View.md) Heterogeneous Create Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.02-Heterogeneous-Create-Partition-Clauses.md)
