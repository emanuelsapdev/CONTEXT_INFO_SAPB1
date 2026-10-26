# 6.1.141 ROLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1561–1562

Shows available roles.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the role granted. |
| ROLE_NAME | NVARCHAR(256) | Displays the role name. |
| ROLE_ID | BIGINT | Displays the role ID. |
| ROLE_MODE | VARCHAR(5) | Displays the local mode of the role. |
| GLOBAL_IDENTITY | NVARCHAR(256) | Displays the identity specified for the role with ROLE_MODE GLOBAL. |
| CREATOR | NVARCHAR(256) | Displays the name of the user who created the role. |
| CREATE_TIME | TIMESTAMP | Displays the time that the role was created. |
| COMMENTS | NVARCHAR(5000) | Displays the description for the speci fied role. |
| CONTEXT | NVARCHAR(2048) | Displays the context that the role is valid for. |

## Related Information

CREATE ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-ROLE-Statement-Access-Control.md) ALTER ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-ROLE-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-ROLE-Statement-Access-Control.md) ROLE_LDAP_GROUPS System View [→](ROLE_LDAP_GROUPS-System-View.md) GRANTED_ROLES System View [→](GRANTED_ROLES-System-View.md) EFFECTIVE_ROLES System View [→](EFFECTIVE_ROLES-System-View.md) EFFECTIVE_ROLE_GRANTEES System View [→](EFFECTIVE_ROLE_GRANTEES-System-View.md)
