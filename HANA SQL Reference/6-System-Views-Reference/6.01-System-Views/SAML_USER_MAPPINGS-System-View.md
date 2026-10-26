# 6.1.144 SAML_USER_MAPPINGS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1563–1564

Shows the SAML providers known for each user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| SAML_PROVIDER_NAME | NVARCHAR(256) | Displays the provider name. |
| EXTERNAL_IDENTITY | NVARCHAR(256) | Displays the name of the user known to the provider. |

## Related Information

SAML_PROVIDERS System View [→](SAML_PROVIDERS-System-View.md) CREATE SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SAML-PROVIDER-Statement-Access-Control.md) ALTER SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-SAML-PROVIDER-Statement-Access-Control.md) DROP SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SAML-PROVIDER-Statement-Access-Control.md)
