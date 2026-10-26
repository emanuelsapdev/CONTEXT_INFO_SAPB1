# 6.2.107 M_ES_TRANSACTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1786–1788

Provides extended storage transaction information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TRANSACTION_ID | BIGINT | Displays the transaction ID. |
| CONNECTION_ID | BIGINT | Displays the connection ID. |
| INTERNAL_CONNECTION_ID | BIGINT | Displays the 10-digit connection ID included as a part of all messages in the `esserver.trc` file. |
| APPLICATION_NAME | VARCHAR(255) | Displays the name of the application. |
| USER_ID | VARCHAR(255) | Displays the user ID for the connection. |
| COMMIT_ID | BIGINT | Displays the ID assigned by the transaction manager when the transaction commits. For active transactions, the commit ID is 0. |
| VERSION_ID | BIGINT | Displays the version ID. A value of 0 indicates that the transaction has no version and that the ID has not been as signed. |
| TRANSACTION_STATE | VARCHAR(16) | Displays the state of the transaction: NONE, ACTIVE, ROLLING_BACK, ROLLED_BACK, COMMITTING, COMMIT TED, or APPLIED. |
| MAIN_TABLE_USED_SIZE | BIGINT | Displays the amount of ES_USER space created by the transaction in megabytes. |
| MAIN_TABLE_FREED_SIZE | BIGINT | Displays the amount of ES_USER space dropped by the transaction in megabytes. |
| TEMP_TABLE_USED_SIZE | BIGINT | Displays the amount of ES_TEMP space created by the transaction in megabytes. |
| TEMP_TABLE_FREED_SIZE | BIGINT | Displays the amount of ES_TEMP space dropped by the transaction in megabytes. |
| TEMP_WORKSPACE_SIZE | BIGINT | For ACTIVE transactions, displays a snapshot of the work space in use at this instant by this transaction, such as sorts, hashes, and temporary bitmaps in megabytes. This number changes de pending on the usage as memory is allocated and freed. When the transaction is no longer active, this column is 0. |
| TRANSACTION_CREATE_TIME | TIMESTAMP | Displays the time that the transaction began. |
| CURSOR_COUNT | INTEGER | Displays the number of open dynamic tiering cursors that reference the trans action control block. If the transaction is ACTIVE, it displays the number of open cursors created within the trans action. If the transaction is COMMIT TED, it displays the number of hold cursors that reference a database version owned by the transaction. |
| INTERNAL_SAVEPOINT_COUNT | INTEGER | Displays the number of savepoint structures that exist within the transaction control block. |
| INTERNAL_SAVEPOINT_NUMBER | INTEGER | Displays the active savepoint number of the transaction. |
| GLOBAL_TRANSACTION_ID | BIGINT | Displays the global transaction ID associated with the transaction. If there is no transaction, then this value is 0. |
| VERSIONING_TYPE | VARCHAR(32) | Displays the snapshot versioning trans action type, either table-level (default), or row-level. Row-level snapshot versioning (DELTA) applies only to DELTA-enabled tables. Once a transaction is started, this value cannot change. |
| IS_BLOCKED | VARCHAR(5) | Indicates whether or not connection blocking is enabled: TRUE/FALSE. If TRUE, the transaction blocks and waits for a conflicting lock to release before it attempts to retry the lock request. |
| BLOCKING_TIME_OUT | INTEGER | Displays the time, in milliseconds, that a transaction waits for a locking conflict to clear. A value of 0 (default) indicates that the transaction waits indefinitely. |

## Related Information

M_ES_TRANSACTIONS System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.11-M_ES_TRANSACTIONS-System-View-Dynamic-Tiering.md) M_TRANSACTIONS System View [→](M_TRANSACTIONS-System-View.md) M_BLOCKED_TRANSACTIONS System View [→](M_BLOCKED_TRANSACTIONS-System-View.md) TRANSACTION_HISTORY System View [→](../6.01-System-Views/TRANSACTION_HISTORY-System-View.md) SET TRANSACTION Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-TRANSACTION-Statement-Transaction-Management.md)
