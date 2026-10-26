# 6.2.3 M_ACTIVE_PROCEDURES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1639–1641

Provides statistics of procedure execution.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PROCEDURE_HOST | VARCHAR(64) | Displays the procedure host. |
| PROCEDURE_PORT | INTEGER | Displays the procedure internal port. |
| PROCEDURE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the name of the stored procedure. |
| PROCEDURE_CONNECTION_ID | INTEGER | Displays the procedure connection ID. |
| PROCEDURE_TRANSACTION_ID | INTEGER | Displays the procedure transaction ID. |
| STATEMENT_ID | VARCHAR(20) | Displays the ID of the statement. |
| STATEMENT_STRING | NCLOB | Displays the SQL statement string. |
| STATEMENT_PARAMETERS | NCLOB | Displays the statement parameters. |
| STATEMENT_STATUS | VARCHAR(16) | Displays the status of the statement:<br>• EXECUTING: the statement is still running<br>• COMPLETED: the statement is completed<br>• COMPILING: the statement is compiling<br>• ABORTED: the statement was aborted |
| STATEMENT_EXECUTION_COUNT | INTEGER | Displays the count of statement execution. |
| STATEMENT_DEPTH | INTEGER | Displays the statement depth. |
| STATEMENT_COMPILE_TIME | BIGINT | Displays the elapsed time spent compiling the statement. |
| STATEMENT_EXECUTION_TIME | BIGINT | Displays the elapsed time spent executing the statement. |
| STATEMENT_START_TIME | TIMESTAMP | Displays the statement start time. |
| STATEMENT_END_TIME | TIMESTAMP | Displays the statement end time. |
| STATEMENT_CONNECTION_ID | INTEGER | Displays the connection ID of the statement. |
| STATEMENT_TRANSACTION_ID | INTEGER | Displays the transaction ID of the statement. |
| STATEMENT_MATERIALIZATION_TIME | BIGINT | Displays the internal table materialization time. |
| STATEMENT_MATERIALIZATION_MEMORY_SIZE | BIGINT | Displays the memory size, in bytes, of the internal table materialization. |
| STATEMENT_EXECUTION_MEMORY_SIZE | BIGINT | Displays the peak amount of memory, in bytes, used for executing each statement inside a procedure. If you are using a distributed execution, shows the sum of local peak memory for multiple servers. |

## Related Information

ALTER PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-PROCEDURE-Statement-Procedural.md) CREATE PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PROCEDURE-Statement-Procedural.md) CREATE VIRTUAL PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-PROCEDURE-Statement-Procedural.md) DROP PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-PROCEDURE-Statement-Procedural.md) M_ACTIVE_STATEMENTS System View [→](M_ACTIVE_STATEMENTS-System-View.md) Procedural Statements [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.09-Procedural-Statements.md) PROCEDURES System View [→](../6.01-System-Views/PROCEDURES-System-View.md)
