# 6.2.192 M_OBJECT_LOCK_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1916–1918

Provides lock contention statistics, including lock wait count, wait time, and failed count, for each object.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type: RECORD, TA BLE, VIEW, SYNONYM, or SEQUENCE. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the object belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| OBJECT_ID | BIGINT | Displays the object ID. |
| LOCK_TYPE | VARCHAR(32) | Displays the lock type: OBJECT/ RECORD. |
| LOCK_WAIT_COUNT | BIGINT | Displays the lock wait count. |
| LOCK_WAIT_TIME | BIGINT | Displays the lock wait time in microseconds. |
| LOCK_FAILED_COUNT | BIGINT | Displays the RECORD type lock failed count. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_OBJECT_LOCK_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_OBJECT_LOCK_STATISTICS_RESET;`.

## Related Information

M_OBJECT_LOCK_STATISTICS_RESET System View [→](M_OBJECT_LOCK_STATISTICS_RESET-System-View.md) M_OBJECT_LOCKS System View [→](M_OBJECT_LOCKS-System-View.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md)
