# 6.1.175 TRIGGER_ORDERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1605–1606

Provides information about trigger order for triggers in the database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the trigger. |
| TRIGGER_NAME | NVARCHAR(256) | Displays the trigger name. |
| TRIGGER_OID | BIGINT | Displays the object ID of the trigger. |
| REFERENCED_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the referenced trigger. |
| REFERENCED_TRIGGER_NAME | NVARCHAR(256) | Displays the name of the referenced trigger. |
| REFERENCED_TRIGGER_OID | BIGINT | Displays the object ID of the referenced trigger. |
| ORDER_TYPE | VARCHAR(10) | Displays the type of ordering: FOL LOWS/PRECEDES. |

## Related Information

TRIGGERS System View [→](TRIGGERS-System-View.md) CREATE TRIGGER Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-TRIGGER-Statement-Data-Definition.md) DROP TRIGGER Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TRIGGER-Statement-Data-Definition.md)
