# 6.1.146 SEARCH_RULE_SETS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1565–1566

Shows information about available search rule sets.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SEARCH_RULE_SET_SCHEMA_NAME | NVARCHAR(256) | Displays the name of the runtime schema of the search rule set. |
| SEARCH_RULE_SET_PACKAGE_ID | NVARCHAR(256) | Displays the name of the repository package of the search rule set. |
| SEARCH_RULE_SET_NAME | NVARCHAR(256) | Displays the name of the search rule set. |
| SEARCHED_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the cata log object that is searched by the given search rule set. |
| SEARCHED_OBJECT_NAME | NVARCHAR(256) | Displays the name of the catalog object that is searched by the given search rule set. |
| SEARCHED_REPOSITORY_PACKAGE_ID | NVARCHAR(256) | Displays the ID of the repository package of the repository object that is searched by the given search rule set. |
| SEARCHED_REPOSITORY_OBJECT_NAME | NVARCHAR(256) | Displays the name of the repository object that is searched by the given search rule set. |

## Related Information

[SEARCH_RULE_SET_CONDITIONS System View](SEARCH_RULE_SET_CONDITIONS-System-View.md)
