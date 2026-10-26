# 6.2.223 M_REMOTE_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1951–1952

Displays detailed information about executed remote queries. This information includes the query status and the number of fetched rows.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction ID. |
| STATEMENT_ID | VARCHAR(20) | Displays the statement ID. |
| REMOTE_CONNECTION_ID | BIGINT | Displays the ID of the remote connection. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| START_TIME | TIMESTAMP | Displays the statement start time. |
| END_TIME | TIMESTAMP | Displays the statement end time. |
| FETCHED_RECORD_COUNT | BIGINT | Displays the number of fetched records. |
| FETCHED_SIZE | BIGINT | Displays the byte size of fetched records. |
| REMOTE_STATEMENT_STATUS | VARCHAR(16) | Displays the statement status: EXE CUTING/CLOSED. |
| REMOTE_STATEMENT_STRING | NCLOB | Displays the statement string. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REMOTE_STATEMENT_DETAILS | NCLOB | Displays the statement details. |
