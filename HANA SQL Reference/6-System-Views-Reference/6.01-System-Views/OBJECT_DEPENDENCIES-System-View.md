# 6.1.105 OBJECT_DEPENDENCIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1523–1524

Provides information about dependencies between objects, such as which views refer to a specific table.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| BASE_DATABASE_NAME | NVARHAR(256) | Displays the database name of the base objects. |
| BASE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the base object. |
| BASE_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the base object. |
| BASE_OBJECT_TYPE | VARCHAR(32) | Displays the type of the base object. |
| DEPENDENT_DATABASE_NAME | NVARCHAR(256) | Displays the database name of the dependent object. |
| DEPENDENT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the dependent object. |
| DEPENDENT_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the dependent object. |
| DEPENDENT_OBJECT_TYPE | VARCHAR(32) | Displays the type of the base dependency. |
| DEPENDENCY_TYPE | INTEGER | Displays the type of dependency between the base and dependent objects:<br>1. Direct dependency (for example, the view uses a table) 2. Indirect dependency that is referenced via direct dependency (for example, the view references a table via another view) 3. SAP internal (dependency to an implicit created object in SQLScript) 4. SAP internal (dependency to an implicit created object in SQLScript) 5. Dependency via a referential constraint |

## Related Information

OBJECTS System View [→](OBJECTS-System-View.md) OBJECT_PRIVILEGES System View [→](OBJECT_PRIVILEGES-System-View.md) M_TEMPORARY_OBJECT_DEPENDENCIES System View [→](../6.02-Monitoring-Views/M_TEMPORARY_OBJECT_DEPENDENCIES-System-View.md)
