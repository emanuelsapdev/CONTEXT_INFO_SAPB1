# 6.1.67 ELEMENT_TYPES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1479–1480

Provides information about available multivalued types.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema containing the object defining or using the collection type. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the table, view, or procedure that defines or uses the collection type. |
| OBJECT_OID | BIGINT | Displays the identifier of the table, view, or procedure that defines or uses the collection type. |
| OBJECT_TYPE | VARCHAR(8) | Displays the object type: TABLE, VIEW, or FUNCTION. |
| ELEMENT_NAME | NVARCHAR(256) | Displays the name of the table or view column or procedure parameter. |
| DATA_TYPE_ID | SMALLINT | Displays the identifier of the element type. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the name of the element type. |
| LENGTH | INTEGER | Displays the length for a character string type or the precision for a numeric type in bytes. |
| SCALE | INTEGER | Displays the scale for a numeric type. |
| MIN_CARDINALITY | INTEGER | Displays the lower bound of the array. |
| MAX_CARDINALITY | INTEGER | Displays the upper bound of the array. |
| ALLOW_DUPLICATES | VARCHAR(5) | Indicates if duplicates are allowed within one column: TRUE/FALSE. |

## Related Information

Multi-valued Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.07-Multi-valued-Data-Types.md) CREATE TYPE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-TYPE-Statement-Procedural.md) DROP TYPE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TYPE-Statement-Procedural.md)
