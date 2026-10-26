# 6.1.183 VIEW_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1618–1619

Provides information about view parameters.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the view. |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the view. |
| VIEW_OID | BIGINT | Displays the object ID of the view. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the parameter name. |
| DATA_TYPE_ID | SMALLINT | Displays the data type ID. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the data type name. |
| LENGTH | INTEGER | Displays the parameter length in bytes. |
| SCALE | INTEGER | Displays the scale of the parameter. |
| POSITION | INTEGER | Displays the ordinal position of the parameter. |
| HAS_DEFAULT_VALUE | VARCHAR(5) | Displays whether the parameter has a default value or not: TRUE/FALSE. |

## Related Information

VIEWS System View [→](VIEWS-System-View.md) VIEW_COLUMNS System View [→](VIEW_COLUMNS-System-View.md) VIEW_EXPRESSION_MACROS System View [→](VIEW_EXPRESSION_MACROS-System-View.md) USER_PARAMETERS System View [→](USER_PARAMETERS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md)
