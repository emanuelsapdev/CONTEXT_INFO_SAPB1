# 6.1.173 TRANSACTION_HISTORY System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1603–1604

Provides information about committed transactions and their users.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COMMIT_TIME | TIMESTAMP | Displays the timestamp. |
| COMMIT_ID | BIGINT | Displays the ID of the committed trans action. |
| APP_USER | NVARCHAR(256) | Displays the user that used the transaction. |

## Related Information

M_TRANSACTIONS System View [→](../6.02-Monitoring-Views/M_TRANSACTIONS-System-View.md) M_BLOCKED_TRANSACTIONS System View [→](../6.02-Monitoring-Views/M_BLOCKED_TRANSACTIONS-System-View.md) M_TRANS_TOKENS System View [→](../6.02-Monitoring-Views/M_TRANS_TOKENS-System-View.md) M_ES_TRANSACTIONS System View [→](../6.02-Monitoring-Views/M_ES_TRANSACTIONS-System-View.md) CURRENT_UPDATE_TRANSACTION Function (Miscellaneous) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UPDATE_TRANSACTION-Function-Miscellaneous.md) Transaction Management Statements [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.13-Transaction-Management-Statements.md) SET TRANSACTION Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-TRANSACTION-Statement-Transaction-Management.md) SET TRANSACTION AUTOCOMMIT DDL Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-TRANSACTION-AUTOCOMMIT-DDL-Statement-Transaction.md)
