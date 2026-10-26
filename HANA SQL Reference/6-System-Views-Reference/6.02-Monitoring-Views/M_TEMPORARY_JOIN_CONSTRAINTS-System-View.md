# 6.2.324 M_TEMPORARY_JOIN_CONSTRAINTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2099–2100

Provides information about temporary join constraints.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the view name. |
| JOIN_CONSTRAINT_NAME | NVARCHAR(256) | Displays the join constraint name. |
| CONSTRAINT_TYPE | VARCHAR(32) | Displays the operator. |
| LOCATION | NVARCHAR(256) | Displays the name of the constraint owner. |
| TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the column. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| OPERATOR | NVARCHAR(256) | Displays the operator. |
| VALUE | NVARCHAR(5000) | Displays the value. |
