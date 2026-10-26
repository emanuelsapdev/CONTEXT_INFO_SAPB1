# 6.2.314 M_TABLE_PLACEMENT_LOCATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2088–2089

Provides table placement location monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| LOCATION_NAME | NVARCHAR(256) | Displays the name of the location. |
| SYSTEM_DEFINED_VOLUME_IDS | NVARCHAR(256) | Displays the volume IDs, which are received from the topology. |
| INCLUDE | NVARCHAR(256) | Displays the list of volume IDs or synonyms which are added to the location name. |
| EXCLUDE | NVARCHAR(256) | Displays the list of volume IDs or synonyms which are removed from the location name. |
| EFFECTIVE_VOLUME_IDS | NVARCHAR(256) | Displays the calculated volume IDs for the location name. |

## Related Information

ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) TABLE_PLACEMENT System View [→](../6.01-System-Views/TABLE_PLACEMENT-System-View.md)

M_TABLE_LOCATIONS System View [→](M_TABLE_LOCATIONS-System-View.md) M_TABLE_PLACEMENT_LOCATIONS System View [→](M_TABLE_PLACEMENT_LOCATIONS-System-View.md)
