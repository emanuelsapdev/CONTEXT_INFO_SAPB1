# 6.2.91 M_EFFECTIVE_PASSWORD_POLICY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1767–1768

Provides information about password policy parameters for database users.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user that this password policy is valid for. |
| PROPERTY | VARCHAR(128) | Displays the password policy parameter. |
| VALUE | VARCHAR(128) | Displays the value of the password policy parameter. |

## Additional Information

This view requires an equal predicate on USER_NAME.

## Related Information

M_PASSWORD_POLICY System View [→](M_PASSWORD_POLICY-System-View.md) CREATE USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USERGROUP-Statement-Access-Control.md) ALTER USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USERGROUP-Statement-Access-Control.md) GENERATE_PASSWORD Function (Security) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/GENERATE_PASSWORD-Function-Security.md) CREATE USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USER-Statement-Access-Control.md) ALTER USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USER-Statement-Access-Control.md) DROP USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-USER-Statement-Access-Control.md)
