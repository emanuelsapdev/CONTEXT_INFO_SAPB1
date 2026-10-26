# 6.2.241 M_RS_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1970

Provides RS memory statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| CATEGORY | VARCHAR(128) | Displays the module name. |
| ALLOCATED_SIZE | BIGINT | Displays the allocated memory size of the module in bytes. |
| USED_SIZE | BIGINT | Displays the used memory size of the module in bytes. |
| FREE_SIZE | BIGINT | Displays the free memory size of the module in bytes |
