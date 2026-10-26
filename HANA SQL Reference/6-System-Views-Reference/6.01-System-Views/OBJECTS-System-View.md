# 6.1.104 OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1522–1523

Provides information about available objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OBJECT_CATEGORY | VARCHAR(1) | Displays the object category of the object. The default is NULL. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| OBJECT_OID | BIGINT | Displays the object ID. |

## Related Information

OBJECT_DEPENDENCIES System View [→](OBJECT_DEPENDENCIES-System-View.md) OBJECT_PRIVILEGES System View [→](OBJECT_PRIVILEGES-System-View.md) M_OBJECT_LOCKS System View [→](../6.02-Monitoring-Views/M_OBJECT_LOCKS-System-View.md) M_OBJECT_LOCK_STATISTICS System View [→](../6.02-Monitoring-Views/M_OBJECT_LOCK_STATISTICS-System-View.md) M_OBJECT_LOCK_STATISTICS_RESET System View [→](../6.02-Monitoring-Views/M_OBJECT_LOCK_STATISTICS_RESET-System-View.md) M_MEMORY_OBJECTS System View [→](../6.02-Monitoring-Views/M_MEMORY_OBJECTS-System-View.md)
