# 6.1.91 JWT_PROVIDERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1510

Lists all of the JWT providers configured in the SAP HANA database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| JWT_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the JWT provider. |
| ISSUER_NAME | NVARCHAR(512) | Displays the name in the iss claim of the JWT tokens provided by this provider. |
| EXTERNAL_IDENTITY_CLAIM | NVARCHAR(256) | Displays the claim provided in the JWT tokens to use when mapping the SAP HANA user to an external user name. |
| IS_CASE_SENSITIVE | VARCHAR(5) | Displays whether the user mapping is checked case sensitive: TRUE/FALSE. |

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-JWT-PROVIDER-Statement-Access-Control.md) DROP JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-JWT-PROVIDER-Statement-Access-Control.md) ALTER JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-JWT-PROVIDER-Statement-Access-Control.md) JWT_USER_MAPPINGS System View [→](JWT_USER_MAPPINGS-System-View.md)
