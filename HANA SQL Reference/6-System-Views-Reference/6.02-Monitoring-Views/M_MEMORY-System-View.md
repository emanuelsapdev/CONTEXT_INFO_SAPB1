# 6.2.172 M_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1890–1891

Deprecated. For servicespecific information related to memory, use the M_SERVICE_MEMORY System View topic and for hostspecific information related to memory, use the M_HOST_RESOURCE_UTILIZATION System View topic.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| NAME | VARCHAR(256) | Displays the type of memory. |
| VALUE | BIGINT | Displays the size of the memory in bytes. |

## Related Information

M_SERVICE_MEMORY System View [→](M_SERVICE_MEMORY-System-View.md) M_HOST_RESOURCE_UTILIZATION System View [→](M_HOST_RESOURCE_UTILIZATION-System-View.md)
