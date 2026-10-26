# 6.2.270 M_SQLSCRIPT_CODE_COVERAGE_RESULTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2011–2012

Provides per-session SQLScript code coverage results.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OBJECT_DEFINITION_ID | BIGINT | Displays the ID of the object definition. This value corresponds to a value in M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS.OBJECT_DEFINITION_ID. |
| DATABASE_NAME | NVARCHAR(256) | Displays the name of the database. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OBJECT_TYPE | VARCHAR(16) | Displays the type of object:<br>• FUNCTION<br>• PROCEDURE<br>• ANONYMOUS BLOCK |
| OBJECT_OID | BIGINT | Displays the ID of the object. |
| LINE | INTEGER | Displays the line number of the code snippet in the object definition. |
| COLUMN | INTEGER | Displays the starting column of the code snippet in the object definition. |
| START_POSITION | INTEGER | Displays the index of the code snippet's first character in the object definition. |
| END_POSITION | INTEGER | Displays the index of the code snippet's last character in the object definition. |
| HIT_COUNT | BIGINT | Displays the hit count for the code snippet during a single invocation of the object; zero if not covered. |
| INVOKER_OBJECT_DEFINITION_ID | BIGINT | Displays the ID of the invoker's object definition; this value is NULL if this is the top-most function or procedure. |
| INVOKER_LINE | INTEGER | Displays the line number in the invoker's object definition; this value is NULL if this is the top-most function or procedure. |
| INVOKER_COLUMN | INTEGER | Displays the column in the invoker's object definition; this value is NULL if this is the top-most function or procedure. |
| INVOKER_START_POSITION | INTEGER | Displays the index of the first character in the invoker's object definition; this value is NULL if this is the top-most function or procedure. |
| INVOKER_END_POSITION | INTEGER | Displays the index of the last character in the invoker's object definition; this value is NULL if this is the top-most function or procedure. |

## Related Information

ALTER SYSTEM {START | STOP} SQLSCRIPT CODE COVERAGE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-SQLSCRIPT-CODE-COVERAGE-Statement.md) M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS System View [→](M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS-System-View.md)
