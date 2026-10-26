# 6.1.102 LIBRARIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1519–1520

Provides information about available public language libraries.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the library. |
| LIBRARY_NAME | NVARCHAR(256) | Displays the name of the library. |
| LIBRARY_OID | BIGINT | Displays the object ID of the library. |
| DEFAULT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the un qualified objects in the library. |
| DEFINITION | NCLOB | Displays the query string for the library. |
| LIBRARY_TYPE | VARCHAR(20) | Displays the language of the library: SQLSCRIPT, BUILTIN. |
| IS_VALID | VARCHAR(5) | Displays whether the library is valid: TRUE when base objects are valid and the definition is valid. FALSE when the base objects for the library are changed or dropped. |
| CREATE_TIME | TIMESTAMP | Displays the creation time for the library. |

## Related Information

LIBRARY_MEMBERS System View [→](LIBRARY_MEMBERS-System-View.md) CREATE LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LIBRARY-Statement-SQLScript.md) ALTER LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-LIBRARY-Statement-SQLScript.md) DROP LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LIBRARY-Statement-SQLScript.md)
