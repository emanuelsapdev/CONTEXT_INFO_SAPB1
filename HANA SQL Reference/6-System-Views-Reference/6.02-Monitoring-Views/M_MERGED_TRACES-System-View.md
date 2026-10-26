# 6.2.179 M_MERGED_TRACES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1900–1902

Contains the merged content of the server trace files for all of the SAP HANA services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| USER_NAME | NVARCHAR(256) | Displays the database user. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction ID. |
| UPDATE_TRANSACTION_ID | BIGINT | Displays the update transaction ID. |
| STATEMENT_ID | BIGINT | Displays the statement ID. |
| THREAD_ID | BIGINT | Displays the ID of thread that wrote trace entry. |
| TIMESTAMP | TIMESTAMP | Displays the time when trace entry was written. |
| TRACE_LEVEL | VARCHAR(16) | Displays the trace level. |
| COMPONENT | VARCHAR(16) | Displays the trace component. |
| SOURCE_FILE_NAME | VARCHAR(512) | Displays the source file which contains the trace. |
| SOURCE_FILE_LINE | BIGINT | Displays the source file line. |
| TRACE_TEXT | NCLOB | Displays the traced text. |
| TRACE_FILE_NAME | VARCHAR(256) | Displays the name of the trace file containing the trace entry. |
| TRACE_FILE_LINE | INTEGER | Displays the trace file line. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the application name. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application source. |
| PASSPORT_ROOT_CONTEXT_ID | VARCHAR(32) | Displays the SAP EPP passport GUID identifying the source of request. |
| PASSPORT_TRANSACTION_ID | VARCHAR(32) | Displays the SAP EPP passport GUID identifying the business transaction. |
| PASSPORT_CONNECTION_ID | VARCHAR(32) | Displays the SAP EPP passport GUID identifying the connection. |
| PASSPORT_CONNECTION_COUNTER | BIGINT | Displays the SAP EPP passport connection counter. |
| PASSPORT_COMPONENT_NAME | NVARCHAR(32) | Displays the SAP EPP passport component name of the initial/root context. |
| PASSPORT_ACTION | NVARCHAR(40) | Displays the SAP EPP passport action. |

## Related Information

[MERGE INTO Statement (Data Manipulation)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/MERGE-INTO-Statement-Data-Manipulation.md)
