# 6.2.228 M_REMOTE_SUBSCRIPTION_DISTRIBUTOR_QUEUE_DATA_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1957–1958

Lists all real time data elements between begin-marker and end-marker for the remote subscription.

| **Column** | **Data type** | **Purpose** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the container ID of this virtual file. |
| ELEMENT_TYPE | VARCHAR(32) | Displays the element type. Values are:<br>1 - BEGIN MARKER<br>2 - END MARKER<br>3 - COMMITTED TRANSACTION |
| MARKER | VARCHAR(64) | Displays the marker string. |
| SEQUENCE_ID | VARCHAR(256) | Displays the The sequence ID of the row. |
| ROW_TYPE | VARCHAR(32) | Displays the internal CDC row type. Values are:<br>2 – COMMIT<br>3 – ROLLBACK<br>8 – BEGIN MARKER<br>9 – END MARKER |
| TRANSACTION_ID | VARCHAR(256) | Displays the remote source transaction ID of the row. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
