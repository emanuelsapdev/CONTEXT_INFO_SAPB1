# 6.2.109 M_EXECUTED_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1790–1792

Provides all statement executions that belong to a specified category.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction object ID. |
| UPDATE_TRANSACTION_ID | BIGINT | Displays the write transaction ID. This number is ever increasing. |
| STATEMENT_ID | VARCHAR(20) | Displays the statement ID. |
| STATEMENT_HASH | VARCHAR(32) | Displays the unique identifier for an SQL string. |
| DB_USER | NVARCHAR(256) | Displays the user name. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema in whose context the statement is executed. |
| APP_USER | NVARCHAR(256) | Displays the application user name. |
| CLIENT_IP | VARCHAR(45) | Displays the IP address of the client machine. |
| CLIENT_PID | BIGINT | Displays the client process ID. |
| START_TIME | TIMESTAMP | Displays the statement start time. |
| DURATION_MICROSEC | BIGINT | Displays the statement duration in microseconds. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the name of the related object. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| ERROR_CODE | INTEGER | Displays the error code. |
| ERROR_TEXT | NVARCHAR(5000) | Displays the error message. |
| PASSPORT_ROOT_CONTEXT_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the source of the request. |
| PASSPORT_TRANSACTION_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the business transaction. |
| PASSPORT_CONNECTION_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the connection. |
| PASSPORT_CONNECTION_COUNTER | BIGINT | Displays the SAP EPP Passport connection counter. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application that defines from which source file SAP HANA is called. The usage is up to the application. This value is also displayed in M_PREPARED_STATEMENTS.APPLICATION_SOURCE. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |

## Additional Information

This view allows you to collect all of the executed statements from whichever category you want to collect from. Only the DDL category is supported. The historization of DDL statement executions investigates the root cause more easily when your SAP HANA instance falls into the invalid metadata status. The collection functionality is turned off by setting the enable_ddl parameter to OFF in the [executed_statements] section of `global.ini`.

The collected history persists by generating the dedicated trace files (for example, `indexserver_selqnta3.32503.executed_statements.000.trc`). You can adjust the consumed disk size for persisted trace files by configuring the maxfiles and maxfilesize parameter, which represents the maximum number of files to be generated (the default is 10) and represents the size limit of each trace file in bytes (the default is 10MB) respectively, in the [executed_statements] section of `global.ini`.

If the history for an executed statement is immediately persisted to the file whenever it is collected, then it may degrade the performance, as the disk input/output is usually more expensive (that is, it takes more times to flush) than memory input/output. Therefore, each statistic is stored at the in-memory buffer instead of instant disk input/output, and the buffer is flushed whenever N records are accumulated in the buffer. Adjust the degree of the flush interval with the trace_flush_interval parameter (the default is 10 records) in the [executed_statements] section of `global.ini` and turn OFF this feature by setting use_in_memory_tracing to OFF in the same section.

The following SQL statements are collected as DDL (Data Definition Language):

- All SQL statements starting with CREATE, DROP, ALTER, and RENAME. For example, CREATE TABLE, CREATE USER and ALTER TABLE.
- All SQL statements starting with TRUNCATE, GRANT, REVOKE, LOAD, EXPORT, IMPORT, and COMMENT.
- The SET SYSTEM LICENSE `<license_key>` and UNSET SYSTEM LICENSE ALL statements.

## Additional Information

Setting the value of the APPLICATION_SOURCE is only available via internal APIs of the SAP HANA database client interfaces (for more information see SAP Note 2873396).

## Related Information

[SAP Note 2873396 SQL Statements](../../4-SQL-Reference/4.10-SQL-Statements/README.md)
