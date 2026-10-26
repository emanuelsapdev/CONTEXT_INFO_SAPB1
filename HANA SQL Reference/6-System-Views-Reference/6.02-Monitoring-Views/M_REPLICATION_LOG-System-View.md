# 6.2.235 M_REPLICATION_LOG System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1964–1965

Provides replication log monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| IS_ENABLED | VARCHAR(5) | Displays TRUE when the replication logs are being collected and FALSE when collecting replication logs is disabled. |
| LAST_DISABLE_REASON | VARCHAR(32) | Displays the latest disable reason: REPLICATION_LOG_SPACE FULL/ USER_COMMAND. |
| USED_REPLICATION_LOG_SIZE | BIGINT | Displays the used replication log size in the volume in bytes. |
| MAX_REPLICATION_LOG_SIZE | BIGINT | Displays the limitation of the replication log size in the volume in bytes. |
