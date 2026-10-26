# 6.1.66 EFFECTIVE_STRUCTURED_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1477–1479

Displays the structured privileges applied to an object.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROOT_SCHEMA_NAME | NVARCHAR(256) | Displays the root schema name. |
| ROOT_OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| USER_ID | BIGINT | Displays the user ID. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OBJECT_OID | BIGINT | Displays the object ID. |
| EFFECTIVE_FILTER | NCLOB | Displays the filter condition applied from all structured privileges. |
| STRUCTURED_PRIVILEGE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of a structured privilege created for an object. |
| STRUCTURED_PRIVILEGE_NAME | NVARCHAR(256) | Displays the name of a structured privilege created for an object. |
| STRUCTURED_PRIVILEGE_ID | BIGINT | Displays the ID of the structured privilege. |
| STRUCTURED_PRIVILEGE_FILTER | NCLOB | Displays the filter condition provided by the structured privilege. |
| STRUCTURED_PRIVILEGE_DEFAULT_SCHEMA_NAME | NVARCHAR(256) | Displays the default schema name of the structured privilege. This schema name is used for unqualified tables and views in a complex filter. |
| STRUCTURED_PRIVILEGE_STATUS | NVARCHAR(64) | Displays the status of a particular structured privilege: APPLIED, NOT GRANTED, NO MATCHING ATTRIBUTE, or NO FILTER VALUES FOUND. |

## Additional Information

This view requires an equal predicate on ROOT_SCHEMA_NAME, ROOT_OBJECT_NAME, and USER_NAME.

## Related Information

STRUCTURED_PRIVILEGES System View [→](STRUCTURED_PRIVILEGES-System-View.md) CREATE STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) ALTER STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) DROP STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md) EFFECTIVE_APPLICATION_PRIVILEGES System View [→](EFFECTIVE_APPLICATION_PRIVILEGES-System-View.md) EFFECTIVE_PRIVILEGES System View [→](EFFECTIVE_PRIVILEGES-System-View.md) EFFECTIVE_PRIVILEGE_GRANTEES System View [→](EFFECTIVE_PRIVILEGE_GRANTEES-System-View.md) OBJECT_PRIVILEGES System View [→](OBJECT_PRIVILEGES-System-View.md)
