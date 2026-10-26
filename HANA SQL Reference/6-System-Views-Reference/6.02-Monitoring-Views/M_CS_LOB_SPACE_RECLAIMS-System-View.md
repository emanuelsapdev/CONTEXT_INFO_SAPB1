# 6.2.61 M_CS_LOB_SPACE_RECLAIMS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1721–1722

Provides information regarding executed LOB garbage collection runs.

## Structure

| **Column name** | **Data type** | **Unit** | **Description** |
| --- | --- | --- | --- |
| HOST | VARCHAR(64) |   | Displays the name of the host. |
| PORT | INTEGER |   | Displays the internal port. |
| VOLUME_ID | INTEGER |   | Displays the persistence volume ID. |
| COLLECTION_SCOPE | VARCHAR(8) |   | Displays the scope of the garbage collection run on either VOLUME, TABLES, or TABLE. |
| SCHEMA_NAME | NVARCHAR(256) |   | Displays the schema name of the scanned table if the scope is TABLE. |
| TABLE_NAME | NVARCHAR(256) |   | Displays the name of the scanned table if the scope is TABLE. |
| START_TIME | TIMESTAMP |   | Displays the start TIME STAMP of the garbage collection run. |
| END_TIME | TIMESTAMP |   | Displays the end TIMESTAMP of the garbage collection run. |
| SCANNED_COLUMNS_COUNT | BIGINT | Counter | Displays the number of over all scanned columns. |
| REMOVED_FILE_LOBS_COUNT | BIGINT | Counter | Displays the number of re moved file LOBs. |
| REMOVED_PACKED_LOBS_COUNT | BIGINT | Counter | Displays the number of re moved packed LOBs. |
| ERROR_CODE | INTEGER |   | Displays the first error code if the execution fails. More details are available in the ERROR_MESSAGE field. |
| ERROR_MESSAGE | NVARCHAR(2000) |   | Displays the detailed error message. |

## Related Information

ALTER SYSTEM RECLAIM LOB SPACE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-LOB-SPACE-Statement-System-Management.md) M_GARBAGE_COLLECTION_STATISTICS System View [→](M_GARBAGE_COLLECTION_STATISTICS-System-View.md)
