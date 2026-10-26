# 6.2.310 M_TABLE_PERSISTENCE_LOCATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2082–2084

Provides information about column store tables and their physical data locations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that the table schema is currently in being modified. |
| IS_HISTORY | VARCHAR(5) | Displays whether the history is part of a table: TRUE/FALSE. |
| PERSISTENCE_HOST | VARCHAR(64) | Displays the host where table data is located. |
| PERSISTENCE_PORT | INTEGER | Displays the port where table data is located. |

## Additional Information

This view shows information on which node contains the persistence parts of a table. This includes the assigned node as visible from the M_TABLE_LOCATIONS view, but also includes other nodes that still contain some persistence of the table. This could occur if a table is moved and not yet merged. In this case the old node still contains some persistence content for the table beside the currently assigned node.

## Related Information

M_TABLE_LOCATIONS System View [→](M_TABLE_LOCATIONS-System-View.md) M_TABLE_PERSISTENCE_LOCATION_STATISTICS System View [→](M_TABLE_PERSISTENCE_LOCATION_STATISTICS-System-View.md)
