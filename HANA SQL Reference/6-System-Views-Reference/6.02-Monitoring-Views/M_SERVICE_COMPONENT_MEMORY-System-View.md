# 6.2.253 M_SERVICE_COMPONENT_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1988

Provides servicespecific memory usage by logical component.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host where the service is running. |
| PORT | INTEGER | Displays the port where the service is running. |
| COMPONENT | VARCHAR(64) | Displays the logical component for which memory usage is reported. |
| USED_MEMORY_SIZE | BIGINT | Displays the amount of memory, in bytes, being used for the logical component. |
