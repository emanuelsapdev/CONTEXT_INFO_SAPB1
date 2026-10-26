# 6.1.157 ST_SPATIAL_REFERENCE_SYSTEMS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1576–1578

Provides information about spatial reference systems.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OWNER_NAME | NVARCHAR(256) | Displays the owner name of the spatial reference system (SRS). |
| SRS_ID | INTEGER | Displays the numeric identifier (SRID) of this spatial reference system. |
| SRS_NAME | NVARCHAR(256) | Displays the name of the spatial reference system. |
| ROUND_EARTH | VARCHAR(7) | Indicates whether the SRS type is ROUND EARTH (TRUE) or PLANAR (FALSE). |
| AXIS_ORDER | VARCHAR(12) | Displays how the database server interprets points with regards to latitude and longitude: x/y/z/m, long/lat/z/m, lat/ long/z/m. |
| SNAP_TO_GRID | DOUBLE | Defines the size, in bytes, of the grid when performing calculations. |
| TOLERANCE | DOUBLE | Defines the precision to use when com paring points. |
| SEMI_MAJOR_AXIS | DOUBLE | Displays the distance from the center of the ellipsoid to the equator for a ROUND EARTH SRS. |
| SEMI_MINOR_AXIS | DOUBLE | Displays the distance from the center of the ellipsoid to the poles for a ROUND EARTH SRS. |
| INV_FLATTENING | DOUBLE | Displays the inverse flattening used for the ellipsoid in a ROUND EARTH SRS. |
| MIN_X | DOUBLE | Displays the minimum x value allowed in coordinates. |
| MAX_X | DOUBLE | Displays the maximum x value allowed in coordinates. |
| MIN_Y | DOUBLE | Displays the minimum y value allowed in coordinates. |
| MAX_Y | DOUBLE | Displays the maximum y value allowed in coordinates. |
| MIN_Z | DOUBLE | Displays the minimum z value allowed in coordinates. |
| MAX_Z | DOUBLE | Displays the maximum z value allowed in coordinates. |
| ORGANIZATION | NVARCHAR(256) | Displays the name of the organization that created the coordinate system used by this spatial reference system. |
| ORGANIZATION_COORDSYS_ID | INTEGER | Displays the ID given to the coordinate system by the organization that created it. |
| SRS_TYPE | VARCHAR(11) | Displays the type of SRS as defined by the SQL/MM standard: GEOGRAPHIC, PROJECTED, or ENGINEERING. |
| LINEAR_UNIT_OF_MEASURE | NVARCHAR(256) | Displays the linear unit of measure used by this spatial reference system. |
| ANGULAR_UNIT_OF_MEASURE | NVARCHAR(256) | Displays the angular unit of measure used by this spatial reference system. |
| POLYGON_FORMAT | VARCHAR(16) | Displays the orientation of the rings in a polygon: COUNTERCLOCKWISE, CLOCKWISE, or EVENODD. |
| STORAGE_FORMAT | VARCHAR(8) | Indicates whether the data is stored in normalized format (INTERNAL), unnor malized format (ORIGINAL), or both (MIXED). |
| DEFINITION | NVARCHAR(256) | Displays the WKT definition of the spatial reference system in the format defined by the OGC standard. |
| TRANSFORM_DEFINITION | NVARCHAR(256) | Displays the transform definition settings for use when transforming data from this SRS to another. |

## Related Information

ST_GEOMETRY_COLUMNS System View [→](ST_GEOMETRY_COLUMNS-System-View.md) ST_UNITS_OF_MEASURE System View [→](ST_UNITS_OF_MEASURE-System-View.md) Spatial Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.09-Spatial-Data-Types.md)
