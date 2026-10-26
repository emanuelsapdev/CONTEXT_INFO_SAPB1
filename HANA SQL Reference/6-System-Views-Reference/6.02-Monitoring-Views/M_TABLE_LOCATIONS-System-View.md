# 6.2.306 M_TABLE_LOCATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2076–2078

Provides information about tables and their logical location. Physical locations are shown in M_TABLE_PERSISTENCE_LOCATIONS.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host where table data is located. This value is empty for views. |
| PORT | INTEGER | Displays the port where the table data is located. This value is 0 for views. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| LOCATION | VARCHAR(75) | Displays the host and port where the table data is located. |

## Related Information

ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) M_TABLE_PERSISTENCE_LOCATIONS System View [→](M_TABLE_PERSISTENCE_LOCATIONS-System-View.md) TABLE_PLACEMENT System View [→](../6.01-System-Views/TABLE_PLACEMENT-System-View.md) M_TABLE_PLACEMENT_LOCATIONS System View [→](M_TABLE_PLACEMENT_LOCATIONS-System-View.md) M_TABLE_LOCATIONS System View [→](M_TABLE_LOCATIONS-System-View.md) TABLE_PLACEMENT_LOCATIONS System View [→](../6.01-System-Views/TABLE_PLACEMENT_LOCATIONS-System-View.md)
