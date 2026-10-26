# 6.2.225 M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1954–1955

Lists all real time data elements such as markers and commit / rollback rows in the remote subscription commit sequence container.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the container ID of the virtual file. |
| ELEMENT_TYPE | VARCHAR(32) | Displays the element type. Values are:<br>1 - BEGIN MARKER<br>2 - END MARKER<br>3 - COMMITTED TRANSACTION |
| MARKER | VARCHAR(64) | Displays the marker string. |
| SEQUENCE_ID | VARCHAR(256) | Displays the sequence ID of the row. |
| ROW_TYPE | VARCHAR(32) | Displays the internal CDC row type. Values are:<br>2 – commit<br>3 – rollback<br>8 – begin-marker<br>9 – end-marker |
| TRANSACTION_ID | VARCHAR(256) | Displays the remote source transaction ID of the row. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
