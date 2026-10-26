# 6.1.145 SCHEMAS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1564–1565

Shows available schemas.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SCHEMA_OWNER | NVARCHAR(256) | Displays the schema owner. |
| HAS_PRIVILEGES | VARCHAR(5) | Shows if the user is the schema owner or has any privileges for the schema or any object within the schema: TRUE/ FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the schema. |

## Related Information

CREATE SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SCHEMA-Statement-Data-Definition.md) SET SCHEMA Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SCHEMA-Statement-Session-Management.md) RENAME SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-SCHEMA-Statement-Data-Definition.md) DROP SCHEMA Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SCHEMA-Statement-Data-Definition.md) CREATE SCHEMA SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SCHEMA-SYNONYM-Statement-Data-Definition.md) DROP SCHEMA SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SCHEMA-SYNONYM-Statement-Data-Definition.md) CURRENT_OBJECT_SCHEMA Function (Miscellaneous) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_OBJECT_SCHEMA-Function-Miscellaneous.md)
