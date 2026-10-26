# 6.1.61 EFFECTIVE_MASK_EXPRESSIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1471–1472

Provides information as to how data is exposed to certain users in terms of data masking.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROOT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. An equal predicate is required. |
| ROOT_OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. An equal predicate is required. |
| ROOT_COLUMN_NAME | NVARCHAR(256) | Displays the column name. An equal predicate is required. |
| USER_NAME | NVARCHAR(256) | Displays the user name. An equal predicate is required. |
| EFFECTIVE_USER_NAME | NVARCHAR(256) | Displays the name of the effective user whom the mask expression enforced on the underlying object it applies to. |
| DEPENDENT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the dependent object. |
| DEPENDENT_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the dependent object. |
| DEPENDENT_OBJECT_TYPE | VARCHAR(32) | Displays the type name of the dependent object. |
| DEPENDENT_COLUMN_NAME | NVARCHAR(256) | Displays the name of the dependent column. |
| UNDERLYING_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the object at its current level. |
| UNDERLYING_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the object at its current level. |
| UNDERLYING_OBJECT_TYPE | VARCHAR(32) | Displays the type name of the object at its current level. |
| UNDERLYING_COLUMN_NAME | NVARCHAR(256) | Displays the name of the column at its current level. |
| MASK_EXPRESSION | NVARCHAR(5000) | Displays the mask expression string. |
| MASK_EXPRESSION_STATUS | VARCHAR(32) | Displays the status of the applied masking: NULL, APPLIED, NOT APPLIED, SESSION USER APPLIED, or SESSION USER NOT APPLIED. The status is NOT APPLIED if the effective user has an UNMASKED privilege. The status is NULL if the specified column does not have a mask definition. |

## Additional Information

This view requires an equal predicate on ROOT_SCHEMA_NAME, ROOT_OBJECT_NAME, ROOT_COLUMN_NAME, and USER_NAME.

## Related Information

CREATE VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIEW-Statement-Data-Definition.md) ALTER VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIEW-Statement-Data-Definition.md)
