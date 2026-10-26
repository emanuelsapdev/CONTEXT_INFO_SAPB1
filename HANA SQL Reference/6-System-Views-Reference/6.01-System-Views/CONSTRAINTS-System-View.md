# 6.1.40 CONSTRAINTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1444–1445

Provides information about defined constraints for tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| POSITION | SMALLINT | Displays the column position in this constraint. |
| CONSTRAINT_NAME | NVARCHAR(256) | Displays the constraint name. |
| IS_PRIMARY_KEY | VARCHAR(5) | Displays whether the constraint is a primary key constraint: TRUE/FALSE. |
| IS_UNIQUE_KEY | VARCHAR(5) | Displays whether the constraint is a unique constraint: TRUE/FALSE. |
| CHECK_CONDITION | NVARCHAR(5000) | Displays the check condition of the check constraint. |

## Related Information

REFERENTIAL_CONSTRAINTS System View [→](REFERENTIAL_CONSTRAINTS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) M_TEMPORARY_JOIN_CONSTRAINTS System View [→](../6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) System Limitations [→](../../4-SQL-Reference/4.11-System-Limitations.md)
