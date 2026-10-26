# 6.1.62 EFFECTIVE_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1472–1474

Provides the privileges of the specified user.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user for whom effective privileges are shown. |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema of the grantee |
| GRANTEE | NVARCHAR(256) | Displays the user or role that has the privilege. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| GRANTOR_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the role that provided the privilege. |
| GRANTOR | NVARCHAR(256) | Displays the user or role that provided the privilege. |
| GRANTOR_TYPE | VARCHAR(4) | Displays the grantor type: USER/ROLE. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of the granted object, for example, TABLE, SCHEMA, and so on. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the object belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name of granted object. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PRIVILEGE | NVARCHAR(256) | Displays the privilege granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the privilege was granted with WITH GRANT OPTION, WITH ADMIN OPTION: TRUE/FALSE. |
| IS_VALID | VARCHAR(5) | Displays whether the privilege is valid or has become invalid due to implicit revoking: TRUE/FALSE. |

## Additional Information

This view requires an equal predicate on USER_NAME.

## Related Information

EFFECTIVE_APPLICATION_PRIVILEGES System View [→](EFFECTIVE_APPLICATION_PRIVILEGES-System-View.md) EFFECTIVE_PRIVILEGE_GRANTEES System View [→](EFFECTIVE_PRIVILEGE_GRANTEES-System-View.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md)
