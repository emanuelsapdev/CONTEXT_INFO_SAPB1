# 6.1.99 LDAP_PROVIDERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1517–1518

Lists all LDAP providers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| LDAP_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the LDAP provider. |
| LDAP_PROVIDER_ID | BIGINT | Displays the ID of the LDAP provider. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| IS_DEFAULT | VARCHAR(5) | Displays whether the the LDAP provider is the default provider: TRUE/FALSE. |
| IS_SSL_USED | VARCHAR(5) | Displays whether the connection to the configured LDAP Server uses SSL: TRUE/FALSE. If SSL ON is specified for the provider, or if USER LOOKUP URL or NESTED GROUP LOOKUP URL use 'ldaps://', the value is TRUE. Otherwise, the value is FALSE. |
| IS_PROVIDER_ENABLED | VARCHAR(5) | Displays whether the LDAP provider is enabled for use: TRUE/FALSE. |
| ATTRIBUTE_DN | VARCHAR(256) | Displays the LDAP attribute to provide the LDAP distinguished name of a user. |
| ATTRIBUTE_MEMBER_OF | NVARCHAR(256) | Displays the LDAP attribute that provides the list of LDAP groups that the user is a member of. |
| USER_TYPE_FOR_LDAP_USER_CREATION | VARCHAR(10) | Displays the type of user to create when LDAP user creation is enabled. NULL if LDAP user creation is not enabled: STANDARD, RESTRICTED, NULL |

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LDAP-PROVIDER-Statement-Access-Control.md) ALTER LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md)

DROP LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDER_URLS System View [→](LDAP_PROVIDER_URLS-System-View.md) LDAP_USERS System View [→](LDAP_USERS-System-View.md) LDAP_PROVIDER_URLS System View [→](LDAP_PROVIDER_URLS-System-View.md) LDAP_USERS System View [→](LDAP_USERS-System-View.md)
