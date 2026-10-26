# 6.1.60 EFFECTIVE_APPLICATION_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1469–1471

Provides information about the application privileges of the specified user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user for whom effective privileges are shown. |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the grantee |
| GRANTEE | NVARCHAR(256) | Displays the user or role that has the privilege. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the type of grant: USER/ROLE. |
| GRANTOR_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the role that provided the privilege. |
| GRANTOR | NVARCHAR(256) | Displays the user or role that provided the privilege. |
| GRANTOR_TYPE | VARCHAR(4) | Displays the grantor type: USER/ROLE. |
| PRIVILEGE | NVARCHAR(256) | Displays the privilege granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the privilege was granted with WITH GRANT OPTION or WITH ADMIN OPTION: TRUE/FALSE. |
| IS_VALID | VARCHAR(5) | Displays whether the privilege is valid or has become invalid due to of implicit revoking: TRUE/FALSE. |

## Related Information

EFFECTIVE_PRIVILEGE_GRANTEES System View [→](EFFECTIVE_PRIVILEGE_GRANTEES-System-View.md) EFFECTIVE_PRIVILEGES System View [→](EFFECTIVE_PRIVILEGES-System-View.md) EFFECTIVE_STRUCTURED_PRIVILEGES System View [→](EFFECTIVE_STRUCTURED_PRIVILEGES-System-View.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md)
