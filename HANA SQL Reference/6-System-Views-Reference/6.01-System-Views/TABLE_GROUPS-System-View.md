# 6.1.163 TABLE_GROUPS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1591

Provides an overview of table group relationships.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| GROUP_TYPE | NVARCHAR(256) | Displays the group type. |
| SUBTYPE | NVARCHAR(256) | Displays the subtype. |
| GROUP_NAME | NVARCHAR(256) | Displays the group name. |
| IS_GROUP_LEAD | VARCHAR(5) | Determines the leading table within a group. |

## Related Information

[TABLES System View](TABLES-System-View.md)
