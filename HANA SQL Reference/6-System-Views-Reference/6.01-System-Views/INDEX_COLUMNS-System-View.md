# 6.1.89 INDEX_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1508–1509

Provides information about index columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| INDEX_NAME | NVARCHAR(256) | Displays the index name. |
| INDEX_OID | BIGINT | Displays the object ID of the index. |
| CONSTRAINT | VARCHAR(32) | Displays the type of constraint on the index: UNIQUE, NOT_NULL_UNIQUE, PRIMARY_KEY; Geocode type of the column: GEOCODE COUNTRY, GEO CODE STATE, GEOCODE COUNTY, GE OCODE CITY, GEOCODEPOSTAL_CODE, GEOCODE DISTRICT, GEOCODE STREET, GEOCODEHOUSE_NUMBER, GEOCODE ADDRESS_LINE, or GEOCODE. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the indexed column. |
| POSITION | SMALLINT | Displays the ordinal position of the indexed column. |
| ASCENDING_ORDER | VARCHAR(5) | Displays whether the indexed column is in ascending order: TRUE/FALSE. |

## Related Information

INDEXES System View [→](INDEXES-System-View.md) CREATE INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-INDEX-Statement-Data-Definition.md) ALTER INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-INDEX-Statement-Data-Definition.md) RENAME INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-INDEX-Statement-Data-Definition.md) DROP INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-INDEX-Statement-Data-Definition.md)
