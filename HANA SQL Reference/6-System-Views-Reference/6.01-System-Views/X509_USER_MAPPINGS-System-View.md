# 6.1.197 X509_USER_MAPPINGS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1632–1633

Shows the X.509 certificates that are known for each user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| SUBJECT_NAME | NVARCHAR(512) | Displays the subject of the X.509 certificate of the user. |
| ISSUER_NAME | NVARCHAR(512) | Displays the issuer of the X.509 certificate of the user. |
| X509_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the X.509 provider. If the user is mapped without a provider, this column is NULL. |

## Related Information

CERTIFICATES System View [→](CERTIFICATES-System-View.md) SAML_PROVIDERS System View [→](SAML_PROVIDERS-System-View.md) PSE_CERTIFICATES System View [→](PSE_CERTIFICATES-System-View.md)

CREATE SAML PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SAML-PROVIDER-Statement-Access-Control.md) CREATE X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-X509-PROVIDER-Access-Control.md) ALTER X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-X509-PROVIDER-Access-Control.md) DROP X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-X509-PROVIDER-Access-Control.md) X509_PROVIDERS System View [→](X509_PROVIDERS-System-View.md) X509_PROVIDER_RULES System View [→](X509_PROVIDER_RULES-System-View.md)
