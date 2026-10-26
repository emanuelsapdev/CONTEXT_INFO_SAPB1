# 6.2.21 M_BLOCKED_TRANSACTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1662–1664

Provides a transaction list waiting for locks.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| BLOCKED_TRANSACTION_ID | INTEGER | Displays the transaction object ID of the transaction waiting for a lock. |
| BLOCKED_UPDATE_TRANSACTION_ID | BIGINT | Displays the write transaction ID of the write transaction waiting for the lock. |
| BLOCKED_CONNECTION_ID | INTEGER | Displays the connection ID associated with the blocked write transaction. |
| LOCK_OWNER_TRANSACTION_ID | INTEGER | Displays the transaction object ID of the transaction holding the lock. |
| LOCK_OWNER_UPDATE_TRANSACTION_ID | BIGINT | Displays the write transaction ID of the write transaction holding the lock. |
| LOCK_OWNER_CONNECTION_ID | INTEGER | Displays the connection ID associated with the write transaction holding the lock. |
| BLOCKED_TIME | TIMESTAMP | Displays the blocked timestamp. |
| WAITING_RECORD_ID | VARCHAR(256) | Displays the ID of the record on which the lock is currently placed. |
| WAITING_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema on which the lock is currently placed. |
| WAITING_TABLE_NAME | NVARCHAR(256) | Deprecated: use WAITING_OBJECT_NAME instead. |
| WAITING_OBJECT_NAME | NVARCHAR(256) | Displays the name of the object on which the lock is currently placed. |
| WAITING_OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| LOCK_TYPE | VARCHAR(32) | Displays the lock type: RECORD, TA BLE, or METADATA. The active lock and the requested lock always have the same lock type. This value applies to the lock, not the request. |
| LOCK_MODE | VARCHAR(32) | Displays the lock mode: SHARED, EX CLUSIVE, or INTENTIONAL EXCLU SIVE. LOCK_MODE applies to the active lock. |

## Related Information

M_TRANSACTIONS System View [→](M_TRANSACTIONS-System-View.md) TRANSACTION_HISTORY System View [→](../6.01-System-Views/TRANSACTION_HISTORY-System-View.md) SET TRANSACTION AUTOCOMMIT DDL Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-TRANSACTION-AUTOCOMMIT-DDL-Statement-Transaction.md)
