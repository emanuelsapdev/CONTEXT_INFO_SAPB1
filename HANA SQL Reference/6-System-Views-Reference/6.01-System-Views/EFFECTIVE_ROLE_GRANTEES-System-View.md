# 6.1.65 EFFECTIVE_ROLE_GRANTEES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1476–1477

Provides information regarding the users and roles that the role is granted to.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the role for whom effective grantees are shown. |
| ROLE_NAME | NVARCHAR(256) | Displays the name of the role for whom effective grantees are shown. |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of grantee that has the role. |
| GRANTEE | NVARCHAR(256) | Displays the user or role that has the role. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| GRANTOR | NVARCHAR(256) | Displays the user that granted the role. |
| GRANTED_ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of granted role. |
| GRANTED_ROLE_NAME | NVARCHAR(256) | Displays the role granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the role was granted with WITH ADMIN OPTION: TRUE/ FALSE. |

## Related Information

EFFECTIVE_ROLES System View [→](EFFECTIVE_ROLES-System-View.md) GRANTED_ROLES System View [→](GRANTED_ROLES-System-View.md) ROLES System View [→](ROLES-System-View.md) CREATE ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-ROLE-Statement-Access-Control.md) ALTER ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-ROLE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-ROLE-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md)
