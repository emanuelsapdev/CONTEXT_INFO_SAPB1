# 6.1.64 EFFECTIVE_ROLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1475–1476

Provides the roles of the current user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user for whom effective roles are shown. |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the grantee. |
| GRANTEE | NVARCHAR(256) | Displays the user or role that has the role. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| GRANTOR | NVARCHAR(256) | Displays the user who granted the role. |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the role granted. |
| ROLE_NAME | NVARCHAR(256) | Displays the role granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the role was granted with WITH ADMIN OPTION: TRUE/ FALSE. |

## Additional Information

This view requires an equal predicate on USER_NAME.

## Related Information

EFFECTIVE_ROLE_GRANTEES System View [→](EFFECTIVE_ROLE_GRANTEES-System-View.md) ROLES System View [→](ROLES-System-View.md) CREATE ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-ROLE-Statement-Access-Control.md) ALTER ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-ROLE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-ROLE-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md) GRANTED_ROLES System View [→](GRANTED_ROLES-System-View.md)
