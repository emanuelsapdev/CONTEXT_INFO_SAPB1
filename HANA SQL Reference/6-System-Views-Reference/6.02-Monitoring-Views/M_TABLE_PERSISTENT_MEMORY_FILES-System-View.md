# 6.2.313 M_TABLE_PERSISTENT_MEMORY_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2087–2088

Displays the persistent memory file information for all of the tables in the database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| COLUMN_FRAGMENT_TYPE | VARCHAR(16) | Displays the column fragment type: PAGED MAIN, SINGLE MAIN, or DELTA. |
| COLUMN_FRAGMENT_VERSION | INTEGER | Displays the column fragment version. |
| FILE_BLOCK_ID | INTEGER | Displays the persistent memory block identifier inside the column fragment version. |
| FILE_NAME | VARCHAR(256) | Displays the persistent memory block file name. |
| FILE_STATUS | VARCHAR(8) | Displays the persistent memory file status: ACTIVE/INACTIVE. |

## Related Information

ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) EXPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/EXPORT-Statement-Data-Import-Export.md) Non-heterogeneous Alter Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/4.10.01.20.01-Non-heterogeneous-Alter-Partition-Clauses.md) Non-heterogeneous Create Partition Clauses [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.01-Non-heterogeneous-Create-Partition-Clauses.md) UNLOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNLOAD-Statement-Data-Manipulation.md) CREATE TABLE Statement (Multistore Table) [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/CREATE-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md) IMPORT Statement (Data Import Export) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/IMPORT-Statement-Data-Import-Export.md)
