# 6.1.121 QUERY_PLANS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1540

Plans how to handle query execution.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PLAN_ID | VARCHAR(256) | Displays the plan ID. |
| OPERATOR_NAME | VARCHAR(5000) | Displays the operator name. |
| OPERATOR_DETAILS | NCLOB | Displays the detailed information on operators in the query plan. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| SUBTREE_COST | DOUBLE | Displays the subtree cost. |
| INPUT_CARDINALITY | DOUBLE | Displays the input cardinality. |
| OUTPUT_CARDINALITY | DOUBLE | Displays the output cardinality. |
| OPERATOR_ID | INTEGER | Displays the operator ID. |
| PARENT_OPERATOR_ID | INTEGER | Displays the parent operator ID. |
| LEVEL | INTEGER | Displays the level. |
| POSITION | INTEGER | Displays the position. |
| TIMESTAMP | TIMESTAMP | Displays the timestamp. |
| HOST | VARCHAR(256) | Displays the host where the plan operator is executed. |
| PORT | INTEGER | Displays the port where the plan operator is executed. |
