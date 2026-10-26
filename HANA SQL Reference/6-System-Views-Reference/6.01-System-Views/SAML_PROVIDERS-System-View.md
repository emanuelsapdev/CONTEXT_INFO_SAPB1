# 6.1.143 SAML_PROVIDERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1562–1563

Shows available SAML providers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SAML_PROVIDER_NAME | NVARCHAR(256) | Displays the provider name. |
| SUBJECT_NAME | NVARCHAR(512) | Displays the subject of the X.509 certificate of the SAML provider. |
| ISSUER_NAME | NVARCHAR(512) | Displays the issuer of the X.509 certificate of the SAML provider. |
| ENTITY_ID | NVARCHAR(1024) | Displays the entity name of the SAML provider (optional). |
| IS_USER_CREATION_ENABLED | VARCHAR(5) | Displays whether the SAML provider is allowed to create a user implicitly: TRUE/FALSE. |
| IS_CASE_SENSITIVE | VARCHAR(5) | Displays whether the user mapping is checked case sensitive: TRUE/FALSE. |

## Related Information

CREATE SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SAML-PROVIDER-Statement-Access-Control.md) ALTER SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-SAML-PROVIDER-Statement-Access-Control.md) DROP SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SAML-PROVIDER-Statement-Access-Control.md)
