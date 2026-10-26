# 6.2.307 M_TABLE_LOCKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2078

Shows table locks.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| LOCK_OWNER_TRANSACTION_ID | INTEGER | Displays the transaction object ID owning the lock. |
| LOCK_OWNER_UPDATE_TRANSACTION_ID | BIGINT | Displays the write transaction ID owning the lock. |
| ACQUIRED_TIME | TIMESTAMP | Displays the lock acquisition time. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| LOCK_MODE | VARCHAR(32) | Displays the lock mode: EXCLUSIVE/ INTENTIONAL EXCLUSIVE. |

## Related Information

LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md) M_READWRITELOCKS System View [→](M_READWRITELOCKS-System-View.md)
