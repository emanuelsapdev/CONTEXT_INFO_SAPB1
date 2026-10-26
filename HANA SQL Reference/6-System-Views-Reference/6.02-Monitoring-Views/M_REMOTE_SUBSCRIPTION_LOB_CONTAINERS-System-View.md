# 6.2.229 M_REMOTE_SUBSCRIPTION_LOB_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1958

Lists all lob container IDs for each remote subscription transaction.

| **Column** | **Data type** | **Purpose** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the container ID of this virtual file. |
| TRANSACTION_ID | VARCHAR(256) | Displays the remote source transaction ID of the lob. |
| LOB_CONTAINER_ID | BIGINT | Displays the container ID of the lob virtual file. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
