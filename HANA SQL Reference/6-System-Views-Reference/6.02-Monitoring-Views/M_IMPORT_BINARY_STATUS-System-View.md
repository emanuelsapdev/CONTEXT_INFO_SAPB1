# 6.2.131 M_IMPORT_BINARY_STATUS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1824–1825

Provides import status information for the current session.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID to distinguish data of each import session (-1 for Python). |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the table or view being imported. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table or view being imported. |
| INDEX_TYPE | VARCHAR(16) | Displays the index type: UNKNOWN, PHYSICAL, OLAP, JOIN, HIERARCHY, or CALCULATION. |
| STATUS | VARCHAR(16) | Displays the import status: QUEUED, WORKING, SKIPPED, DONE, or FAILED. |
| ERROR | VARCHAR(512) | Displays empty if the import was successful and displays error text other wise. |

## Related Information

Binary Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.01-Binary-Data-Types.md) IMPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/IMPORT-Statement-Data-Import-Export.md) IMPORT FROM Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/IMPORT-FROM-Statement-Data-Import-Export.md)
