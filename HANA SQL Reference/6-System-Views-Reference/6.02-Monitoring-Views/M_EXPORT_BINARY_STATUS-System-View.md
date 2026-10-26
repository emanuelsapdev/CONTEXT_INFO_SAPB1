# 6.2.112 M_EXPORT_BINARY_STATUS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1797–1798

Provides export status information for the current session.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID to distinguish the data of each export session (-1 for Python). |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the table or view being exported. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table or view being exported. |
| INDEX_TYPE | VARCHAR(16) | Displays the index type: UNKNOWN, PHYSICAL, OLAP, JOIN, HIERARCHY, or CALCULATION. |
| STATUS | VARCHAR(16) | Displays the export status: QUEUED, WORKING, SKIPPED, DONE, or FAILED. |
| ERROR | VARCHAR(512) | Displays empty if the export is successful. If the export was unsuccessful, then this row displays error text. |

## Related Information

EXPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/EXPORT-Statement-Data-Import-Export.md) IMPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/IMPORT-Statement-Data-Import-Export.md) Binary Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.01-Binary-Data-Types.md)
