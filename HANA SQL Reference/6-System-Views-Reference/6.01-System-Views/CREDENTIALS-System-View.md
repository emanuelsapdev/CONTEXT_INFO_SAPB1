# 6.1.42 CREDENTIALS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1445–1446

Provides information about credentials for users and components.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user the credential belongs to. |
| COMPONENT | NVARCHAR(256) | Displays the name of the component the credential is valid for. |
| PURPOSE | NVARCHAR(256) | Displays the purpose, for example remote machine, that the credential is valid for. |
| CREDENTIAL_TYPE | NVARCHAR(64) | Displays the type of the credential, for example, password or X509. |

## Related Information

CREATE CREDENTIAL Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CREDENTIAL-Statement-Access-Control.md) ALTER CREDENTIAL Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-CREDENTIAL-Statement-Access-Control.md) DROP CREDENTIAL Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CREDENTIAL-Statement-Access-Control.md)
