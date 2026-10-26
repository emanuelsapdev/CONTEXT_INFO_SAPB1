# 6.2.190 M_NUMA_RESOURCES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1914–1915

Provides information on overall resource availability for the system.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| MAX_NUMA_NODE_COUNT | INTEGER | Displays the maximum number of NUMA nodes. |
| MAX_LOGICAL_CORE_COUNT | INTEGER | Displays the maximum number of logical cores. |

## Related Information

[M_NUMA_NODES System View](M_NUMA_NODES-System-View.md)
