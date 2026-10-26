# 6.1.178 USERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1608–1611

Lists all users.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user. |
| USER_ID | BIGINT | Displays the ID of the user. |
| USERGROUP_NAME | NVARCHAR(256) | Displays the name of the user group that the user belongs to; otherwise, NULL. |
| USER_MODE | VARCHAR(8) | Displays the mode of the user: LOCAL/ EXTERNAL. |
| EXTERNAL_IDENTITY | NVARCHAR(256) | Displays the external identity of the user. |
| CREATOR | NVARCHAR(256) | Displays the creator of the user, SYS TEM, or the ID of a user with USER AD MIN privilege. If the user was created by an LDAP provider, the value is SYS. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| VALID_FROM | TIMESTAMP | Displays the start time of the user's validity. |
| VALID_UNTIL | TIMESTAMP | Displays the end time of the user's validity. |
| LAST_SUCCESSFUL_CONNECT | TIMESTAMP | Displays the time of the last successful connection of the user. |
| LAST_INVALID_CONNECT_ATTEMPT | TIMESTAMP | Displays the time of the last invalid connection attempt. |
| INVALID_CONNECT_ATTEMPTS | INTEGER | Displays the number of invalid connection attempts since the last successful connection. |
| ADMIN_GIVEN_PASSWORD | VARCHAR(5) | Displays whether the password was provided by the administrator or by the user: TRUE/FALSE. |
| LAST_PASSWORD_CHANGE_TIME | TIMESTAMP | Displays the time of the last password change. |
| PASSWORD_CHANGE_NEEDED | VARCHAR(5) | Displays whether the user is forced to change their own password: TRUE/ FALSE. |
| IS_PASSWORD_LIFETIME_CHECK_ENABLED | VARCHAR(5) | Displays whether the password-lifetime will be checked for the user: TRUE/ FALSE. |
| USER_DEACTIVATED | VARCHAR(5) | Displays whether the user is deactivated: TRUE/FALSE. |
| DEACTIVATION_TIME | TIMESTAMP | Displays the time given with an explicit deactivation command for the specified user. |
| IS_PASSWORD_ENABLED | VARCHAR(5) | Displays whether authentication using a password is enabled: TRUE/FALSE. |
| IS_KERBEROS_ENABLED | VARCHAR(5) | Displays whether authentication using KERBEROS is enabled: TRUE/FALSE. |
| IS_SAML_ENABLED | VARCHAR(5) | Displays whether authentication using SAML is enabled: TRUE/FALSE. |
| IS_X509_ENABLED | VARCHAR(5) | Displays whether authentication using an X.509 certificate is enabled: TRUE/ FALSE. |
| IS_SAP_LOGON_TICKET_ENABLED | VARCHAR(5) | Displays whether authentication using an SAP logon ticket is enabled: TRUE/ FALSE. |
| IS_SAP_ASSERTION_TICKET_ENABLED | VARCHAR(5) | Displays whether authentication using an SAP assertion ticket is enabled: TRUE/FALSE. |
| IS_RESTRICTED | VARCHAR(5) | Indicates whether the user is missing the PUBLIC role and privilege on their own schema: TRUE/FALSE. |
| IS_RESTRICTED_DETAILS | VARCHAR(40) | Displays the missing privilege(s): ROLE PUBLIC/CREATE ANY ON OWN SCHEMA. |
| IS_CLIENT_CONNECT_ENABLED | VARCHAR(5) | Displays whether the user is allowed to connect outside of applications: TRUE/ FALSE. |
| HAS_REMOTE_USERS | VARCHAR(5) | Displays whether the user has a remote identity mapping: TRUE/FALSE. |
| PASSWORD_CHANGE_TIME | TIMESTAMP | Deprecated. |
| AUTHORIZATION_MODE | VARCHAR(5) | Displays the Authorization mode of the user: LOCAL/LDAP. |
| IS_JWT_ENABLED | VARCHAR(5) | Displays whether authentication using JWT is enabled: TRUE/FALSE. |
| IS_LDAP_ENABLED | VARCHAR(5) | Displays whether authentication using LDAP is enabled:TRUE/FALSE. |
| CREATE_PROVIDER_TYPE | VARCHAR(16) | If the user was created by a provider using automatic user provisioning, then value indicates the type of provider: LDAP PROVIDER/SAML PROVIDER. If the user was created by another user with USER ADMIN privilege (using a CREATE USER statement), then the value is NULL. |
| CREATE_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the provider that created the user, or NULL if the user was created by a user with USER AD MIN privilege (using a CREATE USER statement). |

## Additional Information

Users see different values in this view depending on their privileges, as follows:

- Users with on of the following privileges can see everything for all users: USER ADMIN, CATALOG READ, DATA ADMIN, USERGROUP OPERATOR
- All other users see only information specific to themselves.

## Related Information

CREATE USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USER-Statement-Access-Control.md) ALTER USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USER-Statement-Access-Control.md) VALIDATE USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/VALIDATE-USER-Statement-Access-Control.md) DROP USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-USER-Statement-Access-Control.md) USERGROUPS System View [→](USERGROUPS-System-View.md)
