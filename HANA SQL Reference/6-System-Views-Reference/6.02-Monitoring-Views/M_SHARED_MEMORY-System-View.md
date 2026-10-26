# 6.2.267 M_SHARED_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2008–2009

Provides shared memory usage information for the SAP HANA indexserver.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CATEGORY | VARCHAR(128) | Displays the module name. |
| ALLOCATED_SIZE | BIGINT | Displays the allocated shared memory size on the module in bytes. |
| USED_SIZE | BIGINT | Displays the used shared memory size on the module in bytes. |
| FREE_SIZE | BIGINT | Displays the free shared memory size on the module in bytes. |
