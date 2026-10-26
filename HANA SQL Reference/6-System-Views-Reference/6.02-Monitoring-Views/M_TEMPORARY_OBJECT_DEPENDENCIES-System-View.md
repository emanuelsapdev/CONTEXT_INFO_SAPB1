# 6.2.326 M_TEMPORARY_OBJECT_DEPENDENCIES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2101–2102

Provides information about temporary object dependencies for transient objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| BASE_DATABASE_NAME | NVARCHAR(256) | Displays the database name of the base object. |
| BASE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the base object. |
| BASE_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the base object. |
| BASE_OBJECT_TYPE | VARCHAR(32) | Displays the type of base object. |
| BASE_OBJECT_OID | BIGINT | Displays the object ID of the base object. |
| BASE_OBJECT_IS_TEMPORARY | VARCHAR(5) | Displays the temporary property of the base object. |
| DEPENDENT_DATABASE_NAME | NVARCHAR(256) | Displays the database name of the dependent object. |
| DEPENDENT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the dependent object. |
| DEPENDENT_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the dependent object. |
| DEPENDENT_OBJECT_TYPE | VARCHAR(32) | Displays the dependent type. |
| DEPENDENT_OBJECT_OID | BIGINT | Displays the object ID of the dependent. |
| DEPENDENT_OBJECT_IS_TEMPORARY | VARCHAR(5) | Displays the temporary property of the dependent. |

## Related Information

[OBJECTS System View](../6.01-System-Views/OBJECTS-System-View.md)

[OBJECT_DEPENDENCIES System View](../6.01-System-Views/OBJECT_DEPENDENCIES-System-View.md)
