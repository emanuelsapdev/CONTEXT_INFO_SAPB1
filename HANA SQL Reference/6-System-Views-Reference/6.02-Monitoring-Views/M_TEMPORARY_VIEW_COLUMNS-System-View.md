# 6.2.330 M_TEMPORARY_VIEW_COLUMNS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2107–2109

Provides information about temporary view columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the view name. |
| VIEW_OID | BIGINT | Displays the object ID of the view. |
| COLUMN_NAME | NVARCHAR(256) | Displays the view column name. |
| POSITION | INTEGER | Displays the ordinal position of the view column. |
| DATA_TYPE_ID | SMALLINT | Displays the SQL data type ID of the column. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| OFFSET | SMALLINT | Displays the offset of the column in a record. |
| LENGTH | INTEGER | Displays the number of:<br>• Characters for char types.<br>• Max digits for numeric types.<br>• Characters for datetime types.<br>• Bytes for LOB types. |
| SCALE | INTEGER | Displays the maximum number of digits to the right of the decimal point: TIME or TIMESTAMP. The decimal digits are defined as the number of digits to the right of the decimal point in the second's component of the data. |
| IS_NULLABLE | VARCHAR(5) | Displays whether the column is allowed to accept null value: TRUE/FALSE. |
| DEFAULT_VALUE | NVARCHAR(5000) | Displays the default value in bytes. |
| COLLATION | NVARCHAR(5000) | Displays the collation. |
| COMMENTS | NVARCHAR(5000) | Displays the description for this column. |
| MAX_VALUE | NVARCHAR(5000) | Deprecated. |
| MIN_VALUE | NVARCHAR(5000) | Deprecated. |
| CS_DATA_TYPE_ID | INTEGER | Displays the column store data type ID. |
| CS_DATA_TYPE_NAME | VARCHAR(16) | Displays the column store data type name. |
| DDIC_DATA_TYPE_ID | INTEGER | Displays the DDIC data type ID. |
| DDIC_DATA_TYPE_NAME | VARCHAR(7) | Displays the DDIC data type name. |
| COMPRESSION_TYPE | VARCHAR(9) | Displays the type of compression: DE FAULT, PREFIXED, SPARSE, CLUS TERED, INDIRECT, or RLE. |
| INDEX_TYPE | VARCHAR(4) | Displays the type of index: NONE/ FULL. |
| COLUMN_ID | BIGINT | Displays the ID of the column. |
| PRELOAD | VARCHAR(5) | Displays whether the column is pre loaded: TRUE/FALSE. |

## Related Information

M_TEMPORARY_VIEWS System View [→](M_TEMPORARY_VIEWS-System-View.md) M_TEMPORARY_TABLES System View [→](M_TEMPORARY_TABLES-System-View.md) M_TEMPORARY_OBJECT_DEPENDENCIES System View [→](M_TEMPORARY_OBJECT_DEPENDENCIES-System-View.md)

[M_TEMPORARY_JOIN_CONSTRAINTS System View](M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md)
