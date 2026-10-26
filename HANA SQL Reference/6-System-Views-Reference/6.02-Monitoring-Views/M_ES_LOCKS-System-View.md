# 6.2.102 M_ES_LOCKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1778–1780

Provides extended storage lock information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CONNECTION_ID | BIGINT | Displays the connection ID that has the lock. |
| USER_ID | VARCHAR(255) | Displays the ID of the user who has the lock. |
| TABLE_TYPE | VARCHAR(32) | Displays the type of table: BASE TABLE, GLOBAL TEMPORARY TABLE, or MA TERIALIZED VIEW. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table on which the lock is held. |
| INDEX_ID | BIGINT | Displays the index ID or NULL if there is no index ID. |
| LOCK_CLASS | VARCHAR(8) | Displays the lock class: SCHEMA, ROW, TABLE, or POSITION. |
| LOCK_DURATION_TYPE | VARCHAR(16) | Displays the type of lock duration: TRANSACTION, POSITION, or CON NECTION. |
| LOCK_TYPE | VARCHAR(10) | Displays the lock type:<br>• For SCHEMA, it could be SHARED or EXCLUSIVE<br>• For ROW, it could be: INTENT, READPK, WRITE, WRITTENOPK, or SURROGATE<br>• For TABLE, it could be: SHARED, INTENT, or EXCLUSIVE<br>• For POSITION, it could be PHAN TOM or INSERT |
| ROW_INDENTIFIER | BIGINT | Displays the identifier for the row that the lock starts on. This value is NULL if there is no lock. |
| ROW_RANGE | BIGINT | Displays the number of contiguous rows that are locked. Row locks in the DELTA store can either be a single row or a range of rows. |

## Related Information

LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md) M_ES_LOCKS System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.07-M_ES_LOCKS-System-View-Dynamic-Tiering.md)
