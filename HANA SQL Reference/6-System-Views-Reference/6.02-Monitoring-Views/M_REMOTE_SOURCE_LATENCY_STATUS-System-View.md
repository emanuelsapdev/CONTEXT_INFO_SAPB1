# 6.2.221 M_REMOTE_SOURCE_LATENCY_STATUS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1950

Provides remote source latency status information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| LATENCY_TICKET_NAME | NVARCHAR(32) | Displays the latency ticket name. |
| INTERVAL | INTEGER | Displays the latency interval. |
| STATUS | VARCHAR(8) | Displays the latency ticket status. |
