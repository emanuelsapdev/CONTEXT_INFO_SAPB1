# 6.2.227 M_REMOTE_SUBSCRIPTION_COMPONENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1956–1957

Provides remote subscription component information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| COMPONENT | VARCHAR(10) | Displays the component: DPSERVER, ADAPTER, RECEIVER, or APPLIER. |
| STATUS | VARCHAR(10) | Displays the component status. |
| MESSAGE | NVARCHAR(2000) | Displays an error or warning message. |
