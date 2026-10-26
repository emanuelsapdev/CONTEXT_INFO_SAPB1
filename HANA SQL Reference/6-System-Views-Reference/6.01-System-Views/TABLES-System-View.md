# 6.1.160 TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1580–1585

Provides information about tables in the database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COMMENTS | NVARCHAR(5000) | Displays the table description. |
| FIXED_PART_SIZE | SMALLINT | Displays the fixed part size of the table. |
| IS_LOGGED | VARCHAR(5) | Displays whether or not logging was on for the table at last restart time: TRUE/ FALSE. |
| IS_SYSTEM_TABLE | VARCHAR(5) | Deprecated. |
| IS_COLUMN_TABLE | VARCHAR(5) | Displays whether the table is a column table: TRUE/FALSE. |
| TABLE_TYPE | VARCHAR(16) | Displays the type of the table: ROW, COLUMN, VIRTUAL, EXTENDED, or COLLECTION. |
| IS_INSERT_ONLY | VARCHAR(5) | Displays whether the table is an insert-only table: TRUE/FALSE. |
| IS_TENANT_SHARED_DATA | VARCHAR(5) | Displays whether the table can be shared among other instances: TRUE/ FALSE. |
| IS_TENANT_SHARED_METADATA | VARCHAR(5) | Displays whether the table is a global table: TRUE/FALSE. |
| SESSION_TYPE | VARCHAR(7) | Displays the session type: NONE, SIM PLE, or HISTORY. For HISTORY, time travel is possible. |
| IS_TEMPORARY | VARCHAR(5) | Displays whether the table is a temporary table: TRUE/FALSE. |
| TEMPORARY_TABLE_TYPE | VARCHAR(10) | Displays the temporary table type. |
| COMMIT_ACTION | VARCHAR(8) | Displays the setting for on commit deletion for global temporary tables. |
| IS_USER_DEFINED_TYPE | VARCHAR(5) | Displays whether or not this is a user defined table type: TRUE/FALSE. |
| HAS_PRIMARY_KEY | VARCHAR(5) | Displays whether or not the table has a primary key: TRUE/FALSE. Only valid for column store tables. |
| PARTITION_SPEC | NCLOB | Displays the detail specification of table partitioning. Only valid for column store tables. |
| USES_EXTKEY | VARCHAR(5) | Displays whether or not the table uses an external key: TRUE/FALSE. Only valid for column store tables. |
| AUTO_MERGE_ON | VARCHAR(5) | Displays whether or not automatic delta table merge is activated for the table: TRUE/FALSE. Only valid for column store tables. |
| USES_DIMFN_CACHE | VARCHAR(5) | Displays whether or not the table uses the DimFunctionCache feature: TRUE/ FALSE. Only valid for column store tables. |
| IS_PUBLIC | VARCHAR(5) | Displays whether or not the table is public: TRUE/FALSE. Only valid for column store tables. |
| AUTO_OPTIMIZE_COMPRESSION_ON | VARCHAR(5) | Displays whether or not automatic optimize compression is activated for the table: TRUE/FALSE. Only valid for column store tables. |
| COMPRESSED_EXTKEY | VARCHAR(5) | Displays whether or not the table uses a compressed external key: TRUE/ FALSE. Only valid for column store tables. |
| HAS_TEXT_FIELDS | VARCHAR(5) | Displays whether or not the table has at least one column of type TEXT: TRUE/ FALSE. Only valid for column store tables. |
| USES_QUEUE_TABLE | VARCHAR(5) | Displays whether or not the table uses a queue table: TRUE/FALSE. Only valid for column store tables. |
| IS_PRELOAD | VARCHAR(5) | Displays whether or not the table uses preloading: TRUE/FALSE. Only valid for column store tables. Preload information can be NULL for row store, virtual columns, or tables on extended storage. |
| IS_PARTIAL_PRELOAD | VARCHAR(5) | Displays whether or not the table uses partial preloading: TRUE/FALSE. Only valid for column store tables. Preload information can be NULL for row store, virtual columns, or tables on extended storage |
| UNLOAD_PRIORITY | TINYINT | Displays the unload priority of the table: 0 - 9 means not unloadable, 1 means latest unload, and 9 means earliest un load. |
| HAS_SCHEMA_FLEXIBILITY | VARCHAR(5) | Displays whether or not the table has schema flexibility: TRUE/FALSE. Only valid for column store tables. |
| IS_REPLICA | VARCHAR(5) | Displays whether or not the table is a replica: TRUE/FALSE. |
| HAS_STRUCTURED_PRIVILEGE_CHECK | VARCHAR(5) | Displays whether or not the table is registered for a structured privilege check: TRUE/FALSE. |
| IS_SERIES_TABLE | VARCHAR(5) | Displays whether or not the table is a series table: TRUE/FALSE. |
| ROW_ORDER_TYPE | VARCHAR(8) | Displays the row order type: NULL/BY VALUE. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the table. |
| TEMPORAL_TYPE | VARCHAR(8) | Displays the type of temporal table:<br>• TEMPORAL - a table with system versioning enabled. Tables of this type have a corresponding entry in the TEMPORAL_TABLES system table.<br>• HISTORY - the history table associated with a system-versioned table.<br>• NULL - all other types of tables. |
| HAS_MASKED_COLUMNS | VARCHAR(5) | Displays whether or not the table has a mask definition for at least one column: TRUE/FALSE. |
| MASK_MODE | NVARCHAR(12) | Displays the mask mode to be applied if the table has masked columns: DE FAULT or SESSION USER; otherwise NULL. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays the userspecified persistent memory preference: TRUE (persistent memory is ON)/FALSE (persistent memory OFF). If the user has not speci fied a persistent memory preference, or if the preference is set to the default, then the value is NULL. |
| HAS_RECORD_COMMIT_TIMESTAMP | VARCHAR(5) | Displays whether the table is tracking commit timestamps: TRUE/FALSE. |
| IS_REPLICATION_LOG_ENABLED | VARCHAR(5) | Displays whether the table's replication log is collected. Values are TRUE/ FALSE. |
| NUMA_NODE_INDEXES | VARCHAR (1024) | Displays a comma-separated list of userspecified logical NUMA node indexes for the table. For each column en try in this view there are preferences (if set); otherwise, the value is NULL.<br>The elements of the list are either individual nodes indexes or ranges of index nodes, or a mixture of both. For example, the value `0, 1 TO 3, 6` indicates node indexes 0, 1, 2, 3, and 6. |
| IS_MOVABLE | VARCHAR(5) | Displays whether the table can be moved to another location: TRUE/ FALSE. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for the table partition: TABLE, PAGE (when the partition uses paged attributes), COLUMN, or DEFAULT. |

## Related Information

TABLE_COLUMNS System View [→](TABLE_COLUMNS-System-View.md) TABLE_COLUMNS_ODBC System View [→](TABLE_COLUMNS_ODBC-System-View.md) TABLE_GROUPS System View [→](TABLE_GROUPS-System-View.md) TABLE_PARTITIONS System View [→](TABLE_PARTITIONS-System-View.md) TABLE_PLACEMENT System View [→](TABLE_PLACEMENT-System-View.md) TABLE_REPLICAS System View [→](TABLE_REPLICAS-System-View.md) TEMPORAL_TABLES System View [→](TEMPORAL_TABLES-System-View.md)

M_TABLES System View [→](../6.02-Monitoring-Views/M_TABLES-System-View.md) M_TABLE_LOCATIONS System View [→](../6.02-Monitoring-Views/M_TABLE_LOCATIONS-System-View.md) M_TABLE_LOCKS System View [→](../6.02-Monitoring-Views/M_TABLE_LOCKS-System-View.md) M_TABLE_SNAPSHOTS System View [→](../6.02-Monitoring-Views/M_TABLE_SNAPSHOTS-System-View.md) M_TABLE_STATISTICS System View [→](../6.02-Monitoring-Views/M_TABLE_STATISTICS-System-View.md) M_TABLE_STATISTICS_RESET System View [→](../6.02-Monitoring-Views/M_TABLE_STATISTICS_RESET-System-View.md) M_TABLE_VIRTUAL_FILES System View [→](../6.02-Monitoring-Views/M_TABLE_VIRTUAL_FILES-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md) RENAME TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-TABLE-Statement-Data-Definition.md) TRUNCATE TABLE Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/TRUNCATE-TABLE-Statement-Data-Manipulation.md) DROP TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TABLE-Statement-Data-Definition.md)
