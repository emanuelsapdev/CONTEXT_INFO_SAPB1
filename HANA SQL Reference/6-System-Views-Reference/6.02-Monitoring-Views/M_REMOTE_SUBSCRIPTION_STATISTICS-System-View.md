# 6.2.231 M_REMOTE_SUBSCRIPTION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1959–1960

Provides remote subscription statistic information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| RECEIVED_MESSAGE_COUNT | BIGINT | Displays the received message count. |
| RECEIVED_MESSAGE_SIZE | BIGINT | Displays the received message size in bytes. |
| APPLIED_MESSAGE_COUNT | BIGINT | Displays the received message count. |
| APPLIED_MESSAGE_SIZE | BIGINT | Displays the applied message size in bytes. |
| REJECTED_MESSAGE_COUNT | BIGINT | Displays the rejected message count. |
| LAST_MESSAGE_RECEIVED | TIMESTAMP | Displays the last received message. |
| LAST_MESSAGE_APPLIED | TIMESTAMP | Displays the last applied message. |
| RECEIVER_LATENCY | BIGINT | Displays the receiver latency. |
| APPLIER_LATENCY | BIGINT | Displays the applier latency. |
