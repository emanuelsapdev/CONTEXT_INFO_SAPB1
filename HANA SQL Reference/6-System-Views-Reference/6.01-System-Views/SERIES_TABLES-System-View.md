# 6.1.150 SERIES_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1568–1570

Provides series definitions for tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the series table name. |
| PERIOD_TYPE_ID | TINYINT | Displays the SQL data type ID of the period columns. |
| PERIOD_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the period columns. |
| IS_EQUIDISTANT | VARCHAR(5) | Displays the series table has equidistant elements: TRUE/FALSE. |
| IS_INSTANT | VARCHAR(5) | Displays the series represents instants rather than a period with a start/end: TRUE/FALSE. |
| INCREMENT_BY | NVARCHAR(51) | Displays the delta value for an equidistant series or NULL for a non-equidistant series. When the PERIOD_TYPE is a numeric type, a string represents the number. For datetime, a string in an interval form of `<number-units>`, where units means either year, month, day, hour, minute, or second, represents the number. |
| IS_MISSING_ALLOWED | VARCHAR(5) | Indicates whether missing values are allowed in a non-equidistant series: TRUE/FALSE, or NULL for a non-equidistant series. |
| PERIOD_START_COLUMN | NVARCHAR(256) | Displays the starting series column name, or NULL if it is an implied or an instant series. |
| PERIOD_END_COLUMN | NVARCHAR(256) | Displays the ending series column name, or NULL if it is implied or an instant series. |
| PERIOD_INSTANT_COLUMN | NVARCHAR(256) | Displays the instant series column name, or NULL for an interval series. |
| MIN_VALUE | NVARCHAR(5000) | Displays the minimum value allowed in the series columns. |
| MAX_VALUE | NVARCHAR(5000) | Displays the maximum value allowed in the series columns. |
| CALENDAR_SCHEMA_NAME | NVARCHAR(256) | Reserved. |
| CALENDAR_TABLE_NAME | NVARCHAR(256) | Reserved. |
| CALENDAR_TABLE_OID | BIGINT | Reserved. |
| CALENDAR_KEY | NVARCHAR(256) | Reserved. |

## Related Information

SERIES_KEY_COLUMNS System View [→](SERIES_KEY_COLUMNS-System-View.md) Series Data Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.12-Series-Data-Functions.md)
