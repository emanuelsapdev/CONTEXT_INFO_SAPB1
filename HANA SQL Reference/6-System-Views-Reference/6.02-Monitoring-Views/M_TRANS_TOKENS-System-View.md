# 6.2.340 M_TRANS_TOKENS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2119–2120

Provides information about all active transaction tokens.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| TRANS_TOKEN_ID | BIGINT | Displays the transaction token ID. |
| PRIMARY_TRANS_TOKEN_ID | BIGINT | Displays the primary transaction token ID for the shipped transaction token. If the transaction token is local-only, then this has the same value as TRANS_TOKEN_ID. |
| TRANSACTION_ID | INTEGER | Displays the associated transaction object ID. |
| LOGICAL_CONNECTION_ID | INTEGER | Displays the associated logical connection ID. |
| STATEMENT_ID | BIGINT | Displays the associated logical statement ID. |
| MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the MVCC timestamp that is held by the transaction token. |
| MVCC_SNAPSHOT_SCOPE | VARCHAR(8) | Displays the MVCC snapshot scope: TA BLE/GLOBAL. |
| ES_SNAPSHOT_COUNT | BIGINT | Displays the number of extended storage snapshots. |
| ES_SNAPSHOTS | VARCHAR(1024) | Displays a list of volume and snapshot IDs for all extended storage snapshots. |

## Related Information

M_TRANSACTIONS System View [→](M_TRANSACTIONS-System-View.md) IS_SQL_INJECTION_SAFE Function (Security) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/IS_SQL_INJECTION_SAFE-Function-Security.md)
