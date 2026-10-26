# 6.1.81 GRANTED_ROLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1502–1503

Provides information about roles granted to users or other roles.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the grantee. |
| GRANTEE | NVARCHAR(256) | Displays the user or role the role is granted to. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the role granted. |
| ROLE_NAME | NVARCHAR(256) | Displays the name of the granted role. |
| GRANTOR | NVARCHAR(256) | Displays the user who granted the role. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the role was granted wotj WITH ADMIN OPTION: TRUE/ FALSE. |
| IS_GRANTED_BY_LDAP | VARCHAR(5) | Displays whether the role is granted by LDAP: TRUE/FALSE. |

## Related Information

GRANT Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md) CREATE ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-ROLE-Statement-Access-Control.md) ALTER ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-ROLE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-ROLE-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md) ROLES System View [→](ROLES-System-View.md) EFFECTIVE_ROLE_GRANTEES System View [→](EFFECTIVE_ROLE_GRANTEES-System-View.md) EFFECTIVE_ROLES System View [→](EFFECTIVE_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](GRANTED_PRIVILEGES-System-View.md)
