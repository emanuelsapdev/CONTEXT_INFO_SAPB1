# 6.1.101 LDAP_USERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1519

Shows information about the users using LDAP authorization.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user. |
| DN | NVARCHAR(1024) | Displays the distinguished name of the user in the LDAP server. |
| LAST_AUTHORIZATION_REFRESH_TIME | TIMESTAMP | Displays the time of the last successful LDAP authorization refresh. |

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LDAP-PROVIDER-Statement-Access-Control.md) ALTER LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md) DROP LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDER_URLS System View [→](LDAP_PROVIDER_URLS-System-View.md) LDAP_PROVIDERS System View [→](LDAP_PROVIDERS-System-View.md)
