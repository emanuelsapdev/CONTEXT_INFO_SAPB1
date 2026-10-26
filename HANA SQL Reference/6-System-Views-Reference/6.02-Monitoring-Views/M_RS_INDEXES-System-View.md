# 6.2.240 M_RS_INDEXES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1968–1970

Provides the statistics for B-tree and CPB-tree indexes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| INDEX_NAME | NVARCHAR(256) | Displays the index name. |
| KEY_TYPE | VARCHAR(128) | Displays the key type (data or composite). |
| INDEX_STATUS | VARCHAR(16) | Displays the index status: VALID, INVA LID, or UNUSABLE. |
| TREE_HEIGHT | BIGINT | Displays the B-tree level. |
| LEAF_NODE_COUNT | BIGINT | Displays the number of leaf nodes. |
| NONLEAF_NODE_COUNT | BIGINT | Displays the number of intermediate nodes. |
| NODE_SIZE | BIGINT | Displays the node size in bytes. |
| FANOUT | DOUBLE | Displays the index fan-out. |
| BULKLOAD_FACTOR | DOUBLE | Displays the fill factor for creating or re covering indexes. |
| INDEX_SIZE | BIGINT | Displays the memory index size (number of nodes \* node size) in bytes. |
| ENTRY_COUNT | BIGINT | Displays the number of indexed records. |
| FIXED_LEAF_NODE_COUNT | BIGINT | Displays the number of fixed leaf nodes. FIXED means that the key lengths of all entries in the node have the same value. |
| FIXED_NONLEAF_NODE_COUNT | BIGINT | Displays the number of fixed non-leaf nodes. |
| AVG_LEAF_OFFSET_SIZE | DOUBLE | Displays the average offset size of leaf nodes. |
| AVG_NONLEAF_OFFSET_SIZE | DOUBLE | Displays the average offset size of non-leaf nodes. |
| AVG_LEAF_POINTER_SIZE | DOUBLE | Displays the average pointer size of leaf nodes. |
| AVG_NONLEAF_POINTER_SIZE | DOUBLE | Displays the average pointer size of non-leaf nodes. |
| LEAF_PARTIAL_KEY_SIZE | BIGINT | Displays the partial key length of the leaf node. |
| NONLEAF_PARTIAL_KEY_SIZE | BIGINT | Displays the partial key length of the non-leaf node. |
| INDEX_UTILIZATION | DOUBLE | Displays the index utilization (num_en tries / max_entries). |
| IS_UNIQUE | VARCHAR(5) | Displays the whether the index is unique: TRUE or FALSE. |
| SEARCH_COUNT | BIGINT | Displays the number of search operations. |
| INSERT_COUNT | BIGINT | Deprecated. |
| REMOVE_COUNT | BIGINT | Deprecated. |
| FULL_KEY_REFERENCE_COUNT | BIGINT | Deprecated. |
| DISTINCT_KEY_COUNT | BIGINT | Displays the number of distinct keys. |
| KEY_COUNT | BIGINT | Displays the number of keys. |
| ELIMINATED_DUPLICATE_LEAF_NODE_COUNT | BIGINT | Displays the number of leaf nodes whose duplicate keys are eliminated. |
| UNUSED_LEAF_SLOTS_PER_NODE | DOUBLE | Displays the number of unused slots per leaf node. |
