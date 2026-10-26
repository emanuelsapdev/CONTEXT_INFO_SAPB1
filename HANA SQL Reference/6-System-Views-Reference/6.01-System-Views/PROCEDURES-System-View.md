# 6.1.112 PROCEDURES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1530–1532

Provides information about available stored procedures.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the name of the stored procedure. |
| PROCEDURE_OID | BIGINT | Displays the object ID of the stored procedure. |
| SQL_SECURITY | VARCHAR(7) | Displays the SQL security setting of the stored procedure: DEFINER/INVOKER |
| DEFAULT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the un qualified objects in the procedure. |
| INPUT_PARAMETER_COUNT | INTEGER | Displays the input type parameter count. |
| OUTPUT_PARAMETER_COUNT | INTEGER | Displays the output type parameter count. |
| INOUT_PARAMETER_COUNT | INTEGER | Displays the in/out type parameter count. |
| RESULT_SET_COUNT | INTEGER | Displays the result set count. |
| IS_UNICODE | VARCHAR(5) | Displays whether the stored procedure contains Unicode: TRUE/FALSE. |
| IS_ENCRYPTED | VARCHAR(5) | Displays whether the stored procedure is encrypted: TRUE/FALSE. |
| DEFINITION | NCLOB | Displays the query string of the stored procedure. |
| PROCEDURE_TYPE | VARCHAR(10) | Displays the type of the stored procedure. |
| READ_ONLY | VARCHAR(5) | Displays whether the procedure is read-only: TRUE/FALSE |
| IS_VALID | VARCHAR(5) | Displays whether the procedure is valid: TRUE/FALSE. A procedure become in valid when its base objects are changed or dropped. |
| IS_HEADER_ONLY | VARCHAR(5) | Displays whether the procedure is a header only procedure: TRUE/FALSE. |
| IS_DETERMINISTIC | VARCHAR(5) | Displays whether the stored procedure is deterministic: TRUE/FALSE. |
| HAS_TRANSACTION_CONTROL_STATEMENTS | VARCHAR(5) | Displays whether the procedure has transaction control statements: TRUE/ FALSE. |
| AUTO_COMMIT_DDL | VARCHAR(5) | Displays whether the stored procedure runs with autocommit DDL enabled: TRUE/FALSE. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the owner of the stored procedure. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the procedure. |

## Related Information

CREATE PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PROCEDURE-Statement-Procedural.md) ALTER PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-PROCEDURE-Statement-Procedural.md) DROP PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-PROCEDURE-Statement-Procedural.md) Procedural Statements [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.09-Procedural-Statements.md) PROCEDURE_OBJECTS System View [→](PROCEDURE_OBJECTS-System-View.md) PROCEDURE_PARAMETERS System View [→](PROCEDURE_PARAMETERS-System-View.md) PROCEDURE_PARAMETER_COLUMNS System View [→](PROCEDURE_PARAMETER_COLUMNS-System-View.md)

[PROCEDURE_ROUTES System View](PROCEDURE_ROUTES-System-View.md)
