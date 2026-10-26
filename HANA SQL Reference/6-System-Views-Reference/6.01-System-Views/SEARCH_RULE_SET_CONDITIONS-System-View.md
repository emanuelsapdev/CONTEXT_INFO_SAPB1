# 6.1.147 SEARCH_RULE_SET_CONDITIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1566–1567

Shows conditions to available search rule sets.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SEARCH_RULE_SET_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the runtime schema of the search rule set. |
| SEARCH_RULE_SET_PACKAGE_ID | NVARCHAR(256) | Displays the name of the repository package of the search rule set. |
| SEARCH_RULE_SET_NAME | NVARCHAR(256) | Displays the name of the search rule set. |
| RULE_NUMBER | INTEGER | Displays the number of the rule that contains the column. |
| RULE_ID | NVARCHAR(256) | Displays the unique ID/name of the rule that contains the column. |
| SEARCHED_COLUMN_NAME | NVARCHAR(256) | Displays the name of a column that is used by a search rule set. |
| SEARCHED_COLUMN_CONDITION | NVARCHAR(20) | Displays the condition: EQUALS, NOT EMPTY, or MISSING. |
| SEARCHED_COLUMN_VALUE | NVARCHAR(5000) | Displays the value the user input is compared to, if condition is EQUALS. |
| SEARCHED_COLUMN_VALUE_REPLACED_BY | NVARCHAR(5000) | Displays the user input is replaced by this value if the action is REPLACE. |
| ACTION | NVARCHAR(20) | Displays the action that is performed when the condition is true: SKIP COL UMN, SKIP RULE, or REPLACE. |

## Related Information

[SEARCH_RULE_SETS System View](SEARCH_RULE_SETS-System-View.md)
