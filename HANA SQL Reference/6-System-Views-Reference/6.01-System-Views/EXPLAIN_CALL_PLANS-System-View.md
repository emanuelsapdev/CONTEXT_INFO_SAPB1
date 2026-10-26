# 6.1.71 EXPLAIN_CALL_PLANS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1482–1486

Provides information about the compiled plan of a given procedure.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OPERATOR_NAME | NVARCHAR(5000) | Displays the name of logical operator. |
| OPERATOR_STRING | NCLOB | Displays the statement string or code (llvm, expression, ce) string, or se plan/ operation in text format. |
| RETURN_TYPES | VARCHAR(5000) | Displays the list of return types. |
| INPUT_VALUES | NVARCHAR(5000) | Displays the list of values of input parameters. |
| OUTPUT_VALUES | NVARCHAR(5000) | Displays the list of values of output parameters. |
| EXECUTION_ENGINE | VARCHAR(32) | Displays the list of all involved execution frameworks. |
| DEFAULT_SCHEMA_NAME | NVARCHAR(256) | Displays the default schema of each operator. |
| PROCEDURE_DATABASE_NAME | NVARCHAR(256) | Displays the name of database where procedure is defined. |
| PROCEDURE_SCHEMA_NAME | NVARCHAR(256) | Displays the name of schema where procedure is defined. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the name of outermost procedure. |
| SQLSCRIPT_PLAN_ID | INTEGER | Displays the SE plan ID. |
| SQLSCRIPT_OPERATOR_ID | INTEGER | Displays the SE Operation ID. |
| SQLSCRIPT_OPERATOR_NAME | VARCHAR(64) | Displays the internal name used in SQLScript. |
| NESTED_STATEMENT_IDS | VARCHAR(5000) | Displays the concatenated statement position with respect to SQL inlining. |
| SQLSCRIPT_OPERATOR_COST | DOUBLE | Displays the estimated cost from the SQLScript optimizer. |
| OPERATOR_DETAILS | NCLOB | Displays additional information on the operator. |
| OPERATOR_ID | INTEGER | Displays the unique ID of an operator. |
| PARENT_OPERATOR_ID | INTEGER | Displays the operator ID of the parent of an operator. |
| LEVEL | INTEGER | Displays the level from the root operator. |
| POSITION | INTEGER | Displays the position in the parent operator. |
| STATEMENT_NAME | NVARCHAR(64) | Displays the internal EXPLAIN PLAN command. |
| HOST | VARCHAR(64) | Displays the target node where the execution is expected to take place in a distributed system. |
| PORT | INTEGER | Displays the target node where the execution is expected to take place in a distributed system. |
| TIMESTAMP | TIMESTAMP | Displays the date and time when the EXPLAIN PLAN command was executed. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |

## Additional Information

The OPERATOR_NAME column can contain **column engine** and **row engine** operators, as shown in the following tables.

Column engine operators:

| **Operator Name** | **Description** |
| --- | --- |
| COLUMN SEARCH | Displays the starting position of the column engine operators. OPERATOR_DETAILS lists the projected columns. |
| LIMIT | Displays the operator for limiting the number of output rows. |
| ORDER BY | Displays the operator for sorting output rows. |
| HAVING | Displays the operator for filtering with predicates on top of grouping and aggregation. |
| GROUP BY | Displays the operator for grouping and aggregation. |
| DISTINCT | Displays the operator for duplicate elimination. |
| FILTER | Displays the operator for filtering with predicates. |
| JOIN | Displays the operator for joining input relations. |
| COLUMN TABLE | Displays information about the accessed column table. |
| MULTIPROVIDER | Displays the operator for producing union-all of multiple results having the same grouping and aggregation. |

Row engine operators:

| **Operator Name** | **Description** |
| --- | --- |
| ROW SEARCH | Displays the starting position of row engine operators. OPERATOR_DETAILS lists projected columns. |
| LIMIT | Displays the operator for limiting number of output rows. |
| ORDER BY | Displays the operator for sorting output rows. |
| HAVING | Displays the operator for filtering with predicates on top of grouping and aggregation. |
| GROUP BY | Displays the operator for grouping and aggregation. |
| MERGE AGGREGATION | Displays the operator for merging the results of multiple parallel grouping and aggregations. |
| DISTINCT | Displays the operator for duplicate elimination. |
| FILTER | Displays the operator for filtering with predicates. |
| UNION ALL | Displays the operator for producing union-all of input relations. |
| MATERIALIZED UNION ALL | Displays the operator for producing union-all of input relations with intermediate result materialization. |
| BTREE INDEX JOIN | Displays the operator for joining input relations through B-tree index searches. A join type suffix can be added, for example, a B-tree index join for a left outer join is shown as BTREE INDEX JOIN (LEFT OUTER). A join without a join type suffix indicates an inner join. |
| CPBTREE INDEX JOIN | Displays the operator for joining input relations through CPB-tree index searches. A join type suffix can be added. |
| HASH JOIN | Displays the operator for joining input relations through probing a hash table built on the fly. A join type suffix can be added. |
| NESTED LOOP JOIN | Displays the operator for joining input relations through nested looping. A join type suffix can be added. |
| MIXED INVERTED INDEX JOIN | Displays the operator for joining an input relation of row store format with a column table without format conversion using an inverted index of the column table. A join type suffix can be added. |
| BTREE INDEX SEARCH | Displays the table access through a B-tree index search. |
| CPBTREE INDEX SEARCH | Displays the table access through a CPB-tree index search. |
| TABLE SCAN | Displays the table access through scanning. |
| AGGR TABLE | Displays the operator for aggregating a base table directly. |
| MONITOR SEARCH | Displays the monitoring view access through a search. |
| MONITOR SCAN | Displays the monitoring view access through scanning. |

## Related Information

EXPLAIN PLAN Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/EXPLAIN-PLAN-Statement-Data-Manipulation.md) CALL Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CALL-Statement-Procedural.md)
