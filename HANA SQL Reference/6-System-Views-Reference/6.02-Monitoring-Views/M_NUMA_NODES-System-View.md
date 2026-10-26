# 6.2.189 M_NUMA_NODES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1913–1914

Provides resource availability information on each NUMA node in the hardware topology, including inter-node distances and neighbor information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| NUMA_NODE_ID | INTEGER | Displays the physical NUMA node ID as shown by the operating system. |
| NUMA_NODE_INDEX | INTEGER | Displays the logical NUMA node index. Indexes are in the range of 0 to MAX_NUMA_NODE_COUNT. |
| ACTIVE_LOGICAL_CORE_COUNT | INTEGER | Displays the total active logical core count in the NUMA node. |
| LOGICAL_CORE_IDS | VARCHAR(1024) | Displays the range-separated list of logical core IDs in the NUMA node, for example, (0-3,10-13). |
| MEMORY_SIZE | BIGINT | Displays the total memory size, in bytes, present in the NUMA node. |
| NUMA_NODE_DISTANCES | VARCHAR(1024) | Displays the distances from this node to all other nodes. Indexes in this list are NUMA_NODE_INDEX and the number of entries are as many as MAX_NUMA_NODE_COUNT. |
| NEIGHBOUR_NUMA_NODE_IDS | VARCHAR(512) | Displays the physical NUMA node ID of the neighboring nodes. |

## Related Information

M_NUMA_RESOURCES System View [→](M_NUMA_RESOURCES-System-View.md) IMPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/IMPORT-Statement-Data-Import-Export.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md)
