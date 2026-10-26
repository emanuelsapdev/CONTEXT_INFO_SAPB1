# 6.1.166 TABLE_PLACEMENT_LOCATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1595–1596

Provides table placement location information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| LOCATION_NAME | VARCHAR(256) | Displays the location name. |
| INCLUDE | VARCHAR(256) | Displays the list of volume IDs or synonyms which are added to the respective location name. |
| EXCLUDE | VARCHAR(256) | Displays the list of volume IDs or synonyms which are removed from the respective location name. |

## Related Information

ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md) TABLES System View [→](TABLES-System-View.md) TABLE_PLACEMENT System View [→](TABLE_PLACEMENT-System-View.md) M_TABLE_PLACEMENT_LOCATIONS System View [→](../6.02-Monitoring-Views/M_TABLE_PLACEMENT_LOCATIONS-System-View.md) M_TABLE_LOCATIONS System View [→](../6.02-Monitoring-Views/M_TABLE_LOCATIONS-System-View.md) TABLE_PLACEMENT_LOCATIONS System View [→](TABLE_PLACEMENT_LOCATIONS-System-View.md)
