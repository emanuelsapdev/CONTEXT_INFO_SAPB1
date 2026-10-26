# 6.2.96 M_ES_CONNECTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1771–1773

Provides extended storage connection information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CONNECTION_ID | BIGINT | Displays the connection ID. |
| INTERNAL_CONNECTION_ID | BIGINT | Displays the internal connection ID. |
| USER_ID | VARCHAR(255) | Displays the user ID for the connection. |
| REQUEST_TYPE | VARCHAR(255) | Displays the last request type. |
| COMMAND_TYPE | VARCHAR(32) | Displays the type of command being executed. |
| LOCK_OWNER_CONNECTION_ID | BIGINT | Displays the connection on which this connection is blocked. This value is 0 if the connection is not blocked. |
| LOCK_OWNER_USER_ID | VARCHAR(255) | Displays the owner of the blocking connection. This value is NULL if there is no blocking connection. |
| CURSOR_COUNT | INTEGER | Displays the number of active cursors in the connection. This value is 0 if there are no cursors. |
| THREAD_COUNT | INTEGER | Displays the number of threads in the connection. The minimum value is 1. |
| IDLE_DURATION | INTEGER | Displays the time, in seconds, since the last SA request was issued through the connection. If there is no command, then the time since 01-01-2000 is displayed. |
| INTERNAL_IDLE_DURATION | INTEGER | Displays the time, in seconds, since the last command was issued through the connection. If there is no command, then the time since 01-01-2000 is displayed. |
| TEMP_TABLE_SIZE | BIGINT | Displays the size of the temporary table space in megabytes. This value is 0 if there is no temporary table. |
| TEMP_WORKSPACE_SIZE | BIGINT | Displays the size of the temporary workspace in megabytes. This value is 0 if there is no temporary workspace. |
| LAST_REQUEST_TIME | TIMESTAMP | Displays the start time of the last request for the connection. |
| START_TIME | TIMESTAMP | Displays the creation time of the connection. |
| TRANSACTION_ID | BIGINT | Displays the transaction ID of the current transaction on the connection. |

## Related Information

[M_CONNECTIONS System View](M_CONNECTIONS-System-View.md)

[CONNECT Statement (Session Management)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md)
