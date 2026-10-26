# 6.1.196 X509_PROVIDER_RULES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1631–1632

Lists all of the matching rules for X.509 providers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| X509_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the X.509 provider. |
| POSITION | TINYINT | Displays the order of the rule. |
| MATCHING_RULE | NVARCHAR(512) | Displays the matching rule for the subject distinguished name. |

## Related Information

CREATE X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-X509-PROVIDER-Access-Control.md) ALTER X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-X509-PROVIDER-Access-Control.md) DROP X509 PROVIDER (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-X509-PROVIDER-Access-Control.md) X509_PROVIDERS System View [→](X509_PROVIDERS-System-View.md) X509_USER_MAPPINGS System View [→](X509_USER_MAPPINGS-System-View.md)
