# 6.2.230 M_REMOTE_SUBSCRIPTION_ROLLBACK_SAVEPOINT_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1958–1959

Lists all rollback save points for each remote subscription transaction.

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the container ID of this virtual file. |
| TRANSACTION_ID | VARCHAR(256) | Displays the remote source transaction id of the row. |
| FROM_SEQUENCE_ID | VARCHAR(256) | Displays the sequence ID of the row to roll back from. |
| TO_SEQUENCE_ID | VARCHAR(256) | Displays the sequence ID of the row to roll back to. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
