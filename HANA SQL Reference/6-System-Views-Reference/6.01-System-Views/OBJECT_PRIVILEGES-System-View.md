# 6.1.106 OBJECT_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1524–1525

Provides information about the types of objects and privileges that can be granted to those types of objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| PRIVILEGE | VARCHAR(40) | Displays the privilege that can be granted to this type of object. |

## Related Information

OBJECTS System View [→](OBJECTS-System-View.md) OBJECT_DEPENDENCIES System View [→](OBJECT_DEPENDENCIES-System-View.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md)
