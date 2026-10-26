# 6.2.220 M_REMOTE_SOURCE_LATENCY_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1949–1950

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| LATENCY_TICKET_NAME | NVARCHAR(32) | Displays the latency ticket name. |
| START_TIME | TIMESTAMP | Displays the start time. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| COMPONENT | NVARCHAR(32) | Displays the component. |
| SUB_COMPONENT | NVARCHAR(32) | Displays the subcomponent. |
| STATISTIC_NAME | NVARCHAR(128) | Displays the statistic name. |
| STATISTIC_VALUE | NVARCHAR(64) | Displays the statistic value. |
