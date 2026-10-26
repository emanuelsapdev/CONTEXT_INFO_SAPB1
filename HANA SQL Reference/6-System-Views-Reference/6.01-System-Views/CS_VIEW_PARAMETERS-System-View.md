# 6.1.53 CS_VIEW_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1458–1460

Provides a list of parameters of the objects in the SAP HANA database. Only calculation views are considered. The parameters of a view are parsed from the definition of the underlying scenario.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the object is deployed. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. Only the calculation views are listed. The calculation views are not shown if the underlying calculation scenario has no parameter. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the name of the parameter. If a parameter is referenced by different views, then the parameters are listed for each view separately. Normally, the parameters in a calculation views begins and ends with “$$” character. For example: `$$VAR$$`. |
| IS_MANDATORY | VARCHAR(5) | Displays whether a parameter is mandatory or not: TRUE/FALSE. If TRUE, the value of the parameter should be provided either by setting the default value or through the SQL query. If FALSE, setting the value of the parameter is optional. |
| DEFAULT_VALUE | NVARCHAR(256) | Displays the default value of the parameter. This column is set to an empty string when the parameter has no default value. |
| EVALUATED_DEFAULT_VALUE | NVARCHAR(256) | Displays the result of the evaluation of the expression in the DEFAULT_VALUE column. |
| IS_DEFAULT_VALUE_VOLATILE | BOOLEAN | Displays whether or not the default value is volatile: TRUE/FALSE. |

## Additional Information

Executing a SELECT statement on this monitoring view can be very expensive since the scenarios that have not been cached are fetched from the repository, parsed, and their parameters are extracted. However, providing SCHEMA_NAME and OBJECT_NAME columns can significantly decrease the amount of query time.

## Related Information

VIEW_PARAMETERS System View [→](VIEW_PARAMETERS-System-View.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md)
