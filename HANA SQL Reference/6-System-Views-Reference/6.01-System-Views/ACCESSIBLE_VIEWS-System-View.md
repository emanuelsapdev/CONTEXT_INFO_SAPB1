# 6.1.2 ACCESSIBLE_VIEWS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1403

Provides information about accessible views for a given user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user who is authorized to access the view. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the view. |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the view. |
| ANALYTICAL_PRIVILEGE_NEEDED | VARCHAR(5) | Displays whether this view is secured by means of analytical privileges. |

## Additional Information

This view requires an equal predicate on USER_NAME.
