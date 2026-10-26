# 6.1.25 AUTHORIZATION_GRAPH System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1428–1431

Provides information about authorization dependencies of complex database objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROOT_DEPENDENT_TYPE_ID | SMALLINT | Displays the object type ID of the root object to show as a graph. |
| ROOT_DEPENDENT_OBJECT_ID | BIGINT | Displays the object ID of the root object to show as a graph. |
| DEPENDENT_TYPE_ID | SMALLINT | Displays the object type ID of the dependent object. |
| DEPENDENT_TYPE_ID_NAME | NVARCHAR(256) | Displays the object type name of the dependent object. |
| DEPENDENT_SUBTYPE_ID | SMALLINT | Displays the object subtype ID of the dependent object. |
| DEPENDENT_SUBTYPE_ID_NAME | NVARCHAR(256) | Displays the object subtype name of the dependent object. |
| DEPENDENT_OBJECT_ID | BIGINT | Displays the object ID of the dependent object. |
| DEPENDENT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the dependent object belongs to. |
| DEPENDENT_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the dependent object. |
| DEPENDENT_OWNER_OID | BIGINT | Displays the ID of the user owning the dependent object. |
| DEPENDENT_OWNER_NAME | NVARCHAR(256) | Displays the name of the user owning the dependent object. |
| DEPENDENT_READONLY | INTEGER | Displays the read-only property of the dependent object. |
| UNDERLYING_TYPE_ID | SMALLINT | Displays the object type ID of the underlying object. |
| UNDERLYING_TYPE_ID_NAME | NVARCHAR(256) | Displays the object type name of the underlying object. |
| UNDERLYING_SUBTYPE_ID | SMALLINT | Displays the object subtype ID of the underlying object. |
| UNDERLYING_SUBTYPE_ID_NAME | NVARCHAR(256) | Displays the object subtype name of the underlying object. |
| UNDERLYING_OBJECT_ID | BIGINT | Displays the object ID of the underlying object. |
| UNDERLYING_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the underlying object belongs to. |
| UNDERLYING_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the underlying object. |
| UNDERLYING_OWNER_OID | BIGINT | Displays the ID of the user owning the underlying object. |
| UNDERLYING_OWNER_NAME | NVARCHAR(256) | Displays the name of the user owning the underlying object. |
| UNDERLYING_READONLY | INTEGER | Displays the read-only property of the underlying object. |
| DEPENDENCY_USER_OID | BIGINT | Displays the ID of the user required to have a certain privilege on the underlying object in order to validate the dependent object. |
| DEPENDENCY_USER_NAME | NVARCHAR(256) | Displays the name of the user required to have a certain privilege on the underlying object in order to validate the dependent object. |
| DEPENDENCY_TYPE | SMALLINT | Displays the type of dependency that determines the validation semantics for dependencies sharing the same dependent objects. |
| PRIVILEGE_ID | BIGINT | Displays the ID of the privilege the dependency user is required to have on the underlying object. |
| PRIVILEGE_NAME | NVARCHAR(256) | Displays the name of the privilege the dependency user is required to have on the underlying object. |
| IS_VALID | TINYINT | Displays the current state of the dependency (as integer). It is set by the object validation logic and reflects missing privileges or invalidated objects: 0 - 3. |
| DEPENDENCY_STATUS | VARCHAR(40) | Displays the current state of a privilege for the dependent object: INVALID, NOT AUTHORIZED, AUTHORIZED NON GRANTABLE, or AUTHORIZED GRANT ABLE. |
| AVAILABLE_PRIVILEGES | VARCHAR(256) | Displays the current state of a privilege on upper node (dependent object): IN VALID, NOT GRANTABLE, or GRANTA BLE. |

## Additional Information

This view requires an equal to predicate on ROOT_DEPENDENT_TYPE_ID and ROOT_DEPENDENT_OBJECT_ID.

## Related Information

[AUTHORIZATION_TYPES System View](AUTHORIZATION_TYPES-System-View.md)
