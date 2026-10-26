# 6.1.122 REFERENTIAL_CONSTRAINTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1540–1542

Provides information about referential constraints.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| POSITION | SMALLINT | Displays the column position in this constraint. |
| CONSTRAINT_NAME | NVARCHAR(256) | Displays the constraint name. |
| REFERENCED_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table referenced by this constraint. |
| REFERENCED_TABLE_NAME | NVARCHAR(256) | Displays the name of the table referenced by this constraint. |
| REFERENCED_COLUMN_NAME | NVARCHAR(256) | Displays the name of the column referenced by this column. |
| REFERENCED_CONSTRAINT_NAME | NVARCHAR(256) | Displays the name of the unique constraint referenced by this constraint. |
| UPDATE_RULE | VARCHAR(16) | Displays the update rule: CASCADE, SET NULL, SET DEFAULT, or RESTRICT. |
| DELETE_RULE | VARCHAR(16) | Displays the delete rule: CASCADE, SET NULL, SET DEFAULT, or RESTRICT. |
| IS_ENFORCED | VARCHAR(5) | Displays whether or not this constraint is enforced: TRUE/FALSE. |
| IS_VALIDATED | VARCHAR(5) | Displays whether or not this constraint is validated: TRUE/FALSE. |
| CHECK_TIME | STRING | Displays the time when the constraint is checked: INITIALLY_IMMEDIATE/ INITIALLY DEFERRED. |

## Related Information

CONSTRAINTS System View [→](CONSTRAINTS-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)

[CS_JOIN_CONSTRAINTS System View](CS_JOIN_CONSTRAINTS-System-View.md)
