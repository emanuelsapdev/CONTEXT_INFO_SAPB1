# 6.1.156 ST_GEOMETRY_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1575–1576

Provides information about spatial columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema to which the table containing the spatial column belongs. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table containing the spatial column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the spatial column. |
| SRS_ID | INTEGER | Displays the numeric identifier (SRID) for the spatial reference system (SRS) associated with the spatial column. |
| SRS_NAME | NVARCHAR(256) | Displays the name of the SRS associated with the spatial column. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the spatial data type. |
| COORD_DIMENSION | INTEGER | Displays the dimension of the spatial column. |
| INTERNAL_LAYOUT | VARCHAR(13) | Displays the internal geometry layout: PLAIN or HILBERT CURVE. For details see the column definition and column configuration. |
| SPATIAL_INDEX_PREFERENCE | VARCHAR(8) | Displays the spatial index preference: DEFAULT, RDICT, or RTREE. For details see the column definition and the column configuration. |
| VALIDATION | VARCHAR(4) | Displays the geometry validation level: NONE (checked for bad representation)/FULL (checked for all known invalid representations as defined by the OGC standard). |
| HAS_BOUNDARY_CHECK | VARCHAR(5) | Checks whether the geometries in the column are within the SRS boundaries |

## Related Information

ST_SPATIAL_REFERENCE_SYSTEMS System View [→](ST_SPATIAL_REFERENCE_SYSTEMS-System-View.md) ST_UNITS_OF_MEASURE System View [→](ST_UNITS_OF_MEASURE-System-View.md) Spatial Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.09-Spatial-Data-Types.md) TABLE_COLUMNS System View [→](TABLE_COLUMNS-System-View.md) VIEW_COLUMNS System View [→](VIEW_COLUMNS-System-View.md)
