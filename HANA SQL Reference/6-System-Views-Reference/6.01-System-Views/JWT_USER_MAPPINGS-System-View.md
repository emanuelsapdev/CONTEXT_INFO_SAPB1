# 6.1.92 JWT_USER_MAPPINGS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1510–1511

Lists all of the user-JWT mappings configured in the SAP HANA database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the SAP HANA user name. |
| JWT_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the JWT provider. |
| EXTERNAL_IDENTITY | NVARCHAR(256) | Displays the name of the user known to the JWT provider. |

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-JWT-PROVIDER-Statement-Access-Control.md) DROP JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-JWT-PROVIDER-Statement-Access-Control.md) ALTER JWT PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-JWT-PROVIDER-Statement-Access-Control.md) JWT_PROVIDERS System View [→](JWT_PROVIDERS-System-View.md)
