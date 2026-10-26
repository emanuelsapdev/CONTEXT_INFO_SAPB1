# 6.2.279 M_SQL_PLAN_CACHE_PARAMETERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2033

Provides bind parameters for statements cached in SQL Plan Cache. It saves a parameter set of the most expensive execution for each plan.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PLAN_ID | BIGINT | Displays the logical plan ID which is anon-negative value, same with the one in M_SQL_PLAN_CACHE. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the data type of the parameter. |
| POSITION | INTEGER | Displays the position of the parameter in SQL statement. |
| PARAMETER_VALUE | NCLOB | Displays the value of the captured parameter. |
| BATCH_EXECUTION_ORDER | INTEGER | Displays the execution order in a batch processing. |
| EXECUTION_TIMESTAMP | TIMESTAMP | Displays the timestamp when the parameter value is captured. |

## Related Information

[M_SQL_PLAN_CACHE System View](M_SQL_PLAN_CACHE-System-View.md)
