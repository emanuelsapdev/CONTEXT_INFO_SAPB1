# 6.2.160 M_LOAD_HISTORY_HOST System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1872–1873

Host specific load history KPIs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| TIME | TIMESTAMP | Displays the KPI collection timestamp. |
| CPU | BIGINT | Displays the percent of CPU used by all processes. |
| MEMORY_RESIDENT | BIGINT | Displays the physical memory used for all SAP HANA processes in bytes. |
| MEMORY_TOTAL_RESIDENT | BIGINT | Displays the physical memory used for all processes in bytes. |
| MEMORY_USED | BIGINT | Displays the memory used for all SAP HANA processes in bytes. |
| MEMORY_ALLOCATION_LIMIT | BIGINT | Displays the memory allocation limit for all processes of an SAP HANA instance in bytes. |
| MEMORY_SIZE | BIGINT | Displays the physical memory size in bytes. |
| DISK_USED | BIGINT | Displays the amount of disk used in bytes. |
| DISK_SIZE | BIGINT | Displays the disk size in bytes. |
| NETWORK_IN | BIGINT | Displays the bytes read from network by all processes in bytes per sample. |
| NETWORK_OUT | BIGINT | Displays the bytes written to network by all processes in bytes per sample. |
| SWAP_IN | BIGINT | Displays the bytes read from swap by all processes in bytes per sample. |
| SWAP_OUT | BIGINT | Displays the bytes written to swap by all processes in bytes per sample. |

## Related Information

M_LOAD_HISTORY_INFO System View [→](M_LOAD_HISTORY_INFO-System-View.md) M_LOAD_HISTORY_SERVICE System View [→](M_LOAD_HISTORY_SERVICE-System-View.md) LOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOAD-Statement-Data-Manipulation.md) PERSISTENCE_HISTORY System View [→](../6.01-System-Views/PERSISTENCE_HISTORY-System-View.md)
