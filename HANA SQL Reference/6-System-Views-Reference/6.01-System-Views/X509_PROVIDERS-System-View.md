# 6.1.195 X509_PROVIDERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1631

Lists all of the X.509 providers configured in the SAP HANA database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| X509_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the X.509 provider. |
| ISSUER_NAME | NVARCHAR(512) | Displays the issuer distinguished name. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the provider's owner. |

## Related Information

CREATE X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-X509-PROVIDER-Access-Control.md) ALTER X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-X509-PROVIDER-Access-Control.md) DROP X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-X509-PROVIDER-Access-Control.md) X509_PROVIDER_RULES System View [→](X509_PROVIDER_RULES-System-View.md) X509_USER_MAPPINGS System View [→](X509_USER_MAPPINGS-System-View.md)
