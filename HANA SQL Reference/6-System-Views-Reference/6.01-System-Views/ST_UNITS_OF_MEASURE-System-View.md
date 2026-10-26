# 6.1.158 ST_UNITS_OF_MEASURE System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1578–1579

Provides information about spatial units of measure.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OWNER_NAME | NVARCHAR(256) | Displays the owner name of this unit of measure. |
| UNIT_NAME | NVARCHAR(256) | Displays the name of this unit of measure. |
| UNIT_TYPE | VARCHAR(7) | Displays the type of this unit of measure: ANGULAR/LINEAR. |
| CONVERSION_FACTOR | DOUBLE | Displays the conversion factor of this unit of measure. |

## Related Information

Spatial Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.09-Spatial-Data-Types.md) ST_GEOMETRY_COLUMNS System View [→](ST_GEOMETRY_COLUMNS-System-View.md) ST_SPATIAL_REFERENCE_SYSTEMS System View [→](ST_SPATIAL_REFERENCE_SYSTEMS-System-View.md)
