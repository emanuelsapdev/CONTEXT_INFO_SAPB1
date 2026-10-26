# 6.2.318 M_TABLE_SNAPSHOTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2092–2093

Provides snapshot information for tables that are blocked by table-wise GC.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the table object ID. |
| TABLE_TYPE | VARCHAR(16) | Displays the table type: ROW/COLUMN. |
| MIN_MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the minimum MVCC time stamp which is held by the table-wise GC blocker transaction or cursor. |
| VERSION_COUNT | BIGINT | Displays the number of versions (for a column table, this value is the number of unconsolidated udivlists). |

## Related Information

M_SNAPSHOTS System View [→](M_SNAPSHOTS-System-View.md) M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md)
