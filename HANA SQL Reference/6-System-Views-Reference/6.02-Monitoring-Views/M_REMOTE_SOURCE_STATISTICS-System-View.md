# 6.2.222 M_REMOTE_SOURCE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1950–1951

Returns the remote source operational statistics for monitoring data provisioning components.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| COLLECT_TIME | TIMESTAMP | Displays the collection time. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| COMPONENT | NVARCHAR(32) | Displays the component. |
| SUB_COMPONENT | NVARCHAR(32) | Displays the subcomponent. |
| STATISTIC_NAME | NVARCHAR(128) | Displays the name of the statistic. |
| STATISTICS_VALUE | NVARCHAR(512) | Displays the statistic value. |
