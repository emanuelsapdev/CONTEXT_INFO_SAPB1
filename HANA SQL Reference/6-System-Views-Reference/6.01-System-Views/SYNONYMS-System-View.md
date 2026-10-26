# 6.1.159 SYNONYMS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1579–1580

Lists available synonyms.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the synonym. |
| SYNONYM_NAME | NVARCHAR(256) | Displays the name of the synonym. |
| SYNONYM_OID | BIGINT | Displays the object ID of the synonym. |
| OBJECT_DATABASE | NVARCHAR(256) | Displays the database name of the referenced object. |
| OBJECT_SCHEMA | NVARCHAR(256) | Displays the schema name of the referenced object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the referenced object. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of the referenced object. |
| IS_COLUMN_OBJECT | VARCHAR(5) | Displays whether this view is a column object or not: TRUE/FALSE. |
| IS_VALID | VARCHAR(5) | Displays whether the synonym is valid or not: TRUE/FALSE. This value be comes FALSE when its base object is dropped. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the synonym. |

## Related Information

CREATE SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SYNONYM-Statement-Data-Definition.md) DROP SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SYNONYM-Statement-Data-Definition.md) CREATE SCHEMA SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SCHEMA-SYNONYM-Statement-Data-Definition.md) DROP SCHEMA SYNONYM Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-SCHEMA-SYNONYM-Statement-Data-Definition.md)
