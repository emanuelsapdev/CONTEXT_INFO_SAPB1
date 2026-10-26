# 6.2.232 M_REMOTE_SUBSCRIPTION_TRANSACTION_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1960–1962

Lists all real time data rowsets in the remote subscription transaction container.

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID. |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the container ID of the virtual file. |
| TRANSACTION_ID | VARCHAR(256) | Displays the the remote source trans action ID of the row. |
| SEQUENCE_ID | VARCHAR(256) | Displays the the sequence ID of the row. |
| ROW_TYPE | VARCHAR(32) | Displays the internal CDC row type. Values are:<br>1 – BEGIN TRANSACTION<br>2 – COMMIT<br>3 – ROLLBACK<br>4 – INSERT<br>5 – DELETE<br>6 – BEFORE-IMAGE<br>7 – AFTER-IMAGE<br>8 – BEGIN-MARKER<br>9 – END-MARKER<br>10 – ROLLBACK-TO-SAVEPOINT<br>11 – REPLACE<br>12 – SCHEMA-CHANGE<br>13 – TRUNCATE-TABLE<br>14 – UPSERT<br>15 – TRUNCATE-REPLACE-TARGET<br>16 – BEGIN-REPLACE-SET<br>17 – END-REPLACE-SET<br>18 – EXTERMINATE-ROW<br>19 – LATENCY-STATISTICS |
| DIGEST | VARCHAR(1000) | Displays the digest of the row content. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
