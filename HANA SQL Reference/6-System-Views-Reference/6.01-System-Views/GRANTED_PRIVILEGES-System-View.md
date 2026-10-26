# 6.1.80 GRANTED_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1500–1502

Provides information about privileges and roles granted to users.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the grantee. |
| GRANTEE | NVARCHAR(256) | Displays the user or role the privilege is granted to. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| GRANTOR | NVARCHAR(256) | Displays the user who granted the privilege. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of the granted object like: TABLE, SCHEMA, and so on. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the object belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name of granted object. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PRIVILEGE | NVARCHAR(256) | Displays the privilege granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the privilege was granted with WITH GRANT OPTION or WITH ADMIN OPTION: TRUE/FALSE. |
| IS_VALID | VARCHAR(5) | Displays whether the privilege is valid or has become invalid because of implicit revoking: TRUE/FALSE. |

## Related Information

GRANT Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md) CREATE STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) ALTER STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md) EFFECTIVE_PRIVILEGES System View [→](EFFECTIVE_PRIVILEGES-System-View.md) EFFECTIVE_PRIVILEGE_GRANTEES System View [→](EFFECTIVE_PRIVILEGE_GRANTEES-System-View.md)
