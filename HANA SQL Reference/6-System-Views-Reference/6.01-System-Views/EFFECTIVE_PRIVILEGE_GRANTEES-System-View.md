# 6.1.63 EFFECTIVE_PRIVILEGE_GRANTEES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1474–1475

Provides information about who was granted (explicitly or implicitly via roles) a specified privilege.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of role that has the privilege. |
| GRANTEE | NVARCHAR(256) | Displays the user or role that has the privilege. |
| GRANTEE_TYPE | VARCHAR(4) | Displays the grantee type: USER/ROLE. |
| GRANTOR_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of role that provided the privilege. |
| GRANTOR | NVARCHAR(256) | Displays the user or role that provided the privilege. |
| GRANTOR_TYPE | VARCHAR(4) | Displays the grantor type: USER/ROLE. |
| OBJECT_TYPE | NVARCHAR(32) | Displays the type of the granted object, for example, TABLE, SCHEMA, and so on. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the object belongs to. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name of granted object. |
| PRIVILEGE | NVARCHAR(256) | Displays the privilege granted. |
| IS_GRANTABLE | VARCHAR(5) | Displays whether the privilege was granted with WITH GRANT OPTION or WITH ADMIN OPTION: TRUE/FALSE. |

## Additional Information

This view requires an equal predicate on PRIVILEGE and OBJECT_TYPE.

## Related Information

EFFECTIVE_PRIVILEGES System View [→](EFFECTIVE_PRIVILEGES-System-View.md) EFFECTIVE_APPLICATION_PRIVILEGES System View [→](EFFECTIVE_APPLICATION_PRIVILEGES-System-View.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md)
