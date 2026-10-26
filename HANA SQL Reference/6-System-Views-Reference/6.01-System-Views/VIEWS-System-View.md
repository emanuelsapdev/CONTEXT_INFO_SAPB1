# 6.1.180 VIEWS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1612–1614

Lists available views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the view name. |
| VIEW_OID | BIGINT | Displays the object ID of the view. |
| IS_UNICODE | VARCHAR(5) | Displays whether the query string contains Unicode: TRUE/FALSE. |
| IS_READ_ONLY | VARCHAR(5) | Displays whether this view is read-only or updatable: TRUE/FALSE. |
| IS_DDL_ONLY | VARCHAR(5) | Displays whether users can query the view and modify the underlying table. |
| HAS_CHECK_OPTION | VARCHAR(5) | Displays whether this view has an updatable view condition: TRUE/FALSE. |
| HAS_COLUMN_ALIASES | VARCHAR(5) | Displays whether the view has a columns alias: TRUE/FALSE. |
| DEFINITION | NCLOB | Displays the view definition. |
| COMMENTS | NVARCHAR(5000) | Displays the view description. |
| IS_COLUMN_VIEW | VARCHAR(5) | Displays whether this view is a column view: TRUE/FALSE. |
| VIEW_TYPE | VARCHAR(16) | Displays the type of view: ROW, OLAP, JOIN, HIERARCHY, or CALC. |
| IS_TENANT_SHARED_METADATA | VARCHAR(5) | Displays whether the table is a global table or not: TRUE/FALSE. |
| IS_VALID | VARCHAR(5) | Displays whether the view is valid or not. This value is FALSE when its base objects are changed or dropped: TRUE/ FALSE. |
| HAS_STRUCTURED_PRIVILEGE_CHECK | VARCHAR(5) | Displays whether or not the view is registered for a structured privilege check: TRUE/FALSE. |
| HAS_MASKED_COLUMNS | VARCHAR(5) | Displays whether or not the view has a mask definition for at least one column: TRUE/FALSE. |
| MASK_MODE | NVARCHAR(12) | Displays the mask mode to be applied if the view has masked columns: DE FAULT or SESSION USER; otherwise NULL. |
| HAS_PARAMETERS | VARCHAR(5) | Displays whether or not the view has parameters defined: TRUE/FALSE. |
| HAS_ANONYMIZATION | VARCHAR(5) | Displays whether the view is defined as anonymized: TRUE/FALSE. |
| HAS_CACHE | VARCHAR(36) | Displays whether the result cache is enabled for the view: STATIC, FULL/ STATIC, PARTIAL (SELECTED COL UMNS)/STATIC, PARTIAL (FILTERED)/ STATIC, PARTIAL (SELECTED COL UMNS, FILTERED)/DYNAMIC, FULL/ DYNAMIC, or PARTIAL (FILTERED)/ NONE. |
| CACHE_RETENTION | INTEGER | Displays the cache refresh interval in minutes. |
| CACHE_FILTER | NCLOB | Displays the filter condition specified to reduce the cache size. |
| IS_CACHE_FORCED | VARCHAR(5) | Indicates whether the result cache is forced or cachability is checked: TRUE/ FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |

## Related Information

CREATE VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIEW-Statement-Data-Definition.md) ALTER VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIEW-Statement-Data-Definition.md) DROP VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-VIEW-Statement-Data-Definition.md) ANONYMIZATION_VIEWS System View [→](ANONYMIZATION_VIEWS-System-View.md)

VIEW_COLUMNS System View [→](VIEW_COLUMNS-System-View.md) VIEW_EXPRESSION_MACROS System View [→](VIEW_EXPRESSION_MACROS-System-View.md) VIEW_PARAMETERS System View [→](VIEW_PARAMETERS-System-View.md)
