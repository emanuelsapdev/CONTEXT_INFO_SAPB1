# 6.1.174 TRIGGERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1604–1605

Provides information about triggers that are defined for tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the trigger. |
| TRIGGER_NAME | NVARCHAR(256) | Displays the trigger name. |
| TRIGGER_OID | BIGINT | Displays the object ID of the trigger. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the trigger owner. |
| OWNER_OID | BIGINT | Displays the object ID of the trigger owner. |
| SUBJECT_TABLE_SCHEMA | NVARCHAR(256) | Displays the schema name of the table, the trigger is defined for. |
| SUBJECT_TABLE_NAME | NVARCHAR(256) | Displays the table name of the table, the trigger is defined for. |
| TRIGGER_ACTION_TIME | VARCHAR(10) | Displays the time the trigger is executed: BEFORE, AFTER, or INSTEAD OF the specified event. |
| TRIGGER_EVENT | VARCHAR(20) | Displays the event the trigger is defined for: combination of DELETE, INSERT, or UPDATE. |
| TRIGGERED_ACTION_LEVEL | VARCHAR(9) | Displays the level of the event where the triggered action happens: ROW/STATE MENT. |
| DEFINITION | NCLOB | Displays the query string of the trigger. |
| IS_VALID | VARCHAR(5) | Displays whether the trigger is valid or not: TRUE/FALSE. This becomes FALSE when its base objects are changed or dropped. |
| IS_ENABLED | VARCHAR(5) | Displays whether the trigger is enabled or not: TRUE/FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the time that the trigger was created. |

## Related Information

TRIGGER_ORDERS System View [→](TRIGGER_ORDERS-System-View.md) CREATE TRIGGER Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-TRIGGER-Statement-Data-Definition.md) DROP TRIGGER Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TRIGGER-Statement-Data-Definition.md)
