# 6.1.110 PINNED_SQL_PLANS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1528–1529

Provides information on currently pinned SQL plans and corresponding hints.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PINNED_PLAN_ID | BIGINT | Displays the pinned ID. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| USER_NAME | NVARCHAR(256) | Displays the name of the user who prepared the plan. |
| SESSION_USER_NAME | NVARCHAR(256) | Displays the session user name who prepared the plan. This is the same value as displayed in the USER_NAME column in the M_CONNECTIONS monitored view. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the SQL plan belongs to. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value. |
| IS_INTERNAL | TINYINT | Displays whether the plan is executed from a database internal connection or a remote connection: TRUE/FALSE. |
| ABAP_VARCHAR_MODE | TINYINT | Displays whether the value ABAP VAR CHAR mode is enabled: TRUE/FALSE. |
| PIN_TIME | TIMESTAMP | Displays the timestamp when the plan was pinned. |
| LAST_MODIFY_TIME | TIMESTAMP | Displays the timestamp when the plan was modified. |
| HINT_STRING | NCLOB | Displays the text string to indicate a hint was applied. |
| SESSION_PROPERTIES | NVARCHAR(500) | Displays the composed variables from the session context. |

## Related Information

[ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PIN-UNPIN-SQL-PLAN-CACHE-ENTRY-Statement.md)
