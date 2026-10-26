# 6.1.103 LIBRARY_MEMBERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1520–1522

Provides member information for SQLScript userdefined libraries.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the library. |
| LIBRARY_NAME | NVARCHAR(256) | Displays the name of the library. |
| LIBRARY_OID | BIGINT | Displays the object ID of the library. |
| MEMBER_NAME | NVARCHAR(256) | Displays the library member name. |
| MEMBER_TYPE | VARCHAR(9) | Displays the member type: VARIABLE, PROCEDURE, or FUNCTION. |
| ACCESS_MODE | VARCHAR(9) | Displays the access mode of the library member:<br>• PUBLIC when the member is accessible without restriction.<br>• PRIVATE when the member is accessible within the library. |
| DEFINITION | NCLOB | Displays the definition of the library member. |
| PRAGMAS | NVARCHAR(5000) | Displays the SQLScript userdefined test library pragmas. |
| COMMENTS | NVARCHAR(5000) | Displays the comments defined on userdefined libraries and members. |

## Related Information

LIBRARIES System View [→](LIBRARIES-System-View.md) CREATE LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LIBRARY-Statement-SQLScript.md) ALTER LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-LIBRARY-Statement-SQLScript.md) DROP LIBRARY Statement (SQLScript) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LIBRARY-Statement-SQLScript.md)
