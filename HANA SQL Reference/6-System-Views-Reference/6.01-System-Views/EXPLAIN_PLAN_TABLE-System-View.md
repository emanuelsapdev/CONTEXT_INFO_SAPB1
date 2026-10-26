# 6.1.72 EXPLAIN_PLAN_TABLE System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1486–1491

Provides information about SQL query plan explanation results.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STATEMENT_NAME | VARCHAR(256) | Displays the string specified as STATEMENT_NAME when executing the EX PLAIN PLAN command. This is used to distinguish plans from each other when there are multiple plans in EXPLAIN_PLAN_TABLE view. |
| OPERATOR_NAME | VARCHAR(5000) | Displays a column engine or row engine operator. See the Additional Information section within this topic for more information about the possible values in this column. |
| OPERATOR_DETAILS | NCLOB | Displays details of an operator including predicates and expressions used by the operator. |
| OPERATOR_PROPERTIES. | NCLOB | Displays the internal properties of an operator. |
| EXECUTION_ENGINE | VARCHAR(256) | Displays the execution engine where the plan operator is executed: COL UMN, ROW, or SQLScript. |
| DATABASE_NAME | NVARCHAR(256) | Displays the database name that the object belongs to. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name the dependent object belongs to. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the database tables and views accessed by an operator. |
| TABLE_TYPE | VARCHAR(5000) | Displays the table stored type: COL UMN or ROW. |
| TABLE_SIZE | DOUBLE | Displays the estimated input row count of an operator. This is available only for operators accessing tables and views directly. |
| OUTPUT_SIZE | DOUBLE | Estimated output row count of an operator. |
| SUBTREE_COST | DOUBLE | Displays the estimated cost based on estimated cardinality information. This value is used for the cost-based optimizer to choose the best plan. The value can also be a possible indicator to compare two different plans for the same query; the smaller the subtree cost, typically the better the performance. |
| OPERATOR_ID | INTEGER | Displays the unique ID of an operator. IDs are integers starting from 1. |
| PARENT_OPERATOR_ID | INTEGER | Displays the operator ID of the parent of an operator. The shape of a query plan is a tree and the topology of the tree can be reconstructed using OPERATOR_ID and PARENT_OPERATOR_ID. The PARENT_OPERATOR_ID of the root operator appears as NULL. |
| LEVEL | INTEGER | Displays the level from the root operator. The level of the root operator is 1, the level of a child of the root operator is 2, and so on. This can be utilized for output indentation. |
| POSITION | INTEGER | Displays the position in the parent operator. The position of the first child is 1, the position of the second child is 2, and so on. |
| HOST | VARCHAR(256) | Displays the host where the plan operator is generated. |
| PORT | INTEGER | Displays the port where the plan operator is generated. |
| TIMESTAMP | TIMESTAMP | Displays the date and time when the EXPLAIN PLAN command was executed. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |

## Additional Information

The OPERATOR_NAME column can contain **column engine** and **row engine** operators, as shown in the following tables..

Column engine operators:

| **Operator Name** | **Description.** |
| --- | --- |
| COLUMN SEARCH | Displays the starting position of column engine operators. OPERATOR_DETAILS lists the projected columns. |
| LIMIT | Displays the operator for limiting the number of output rows. |
| ORDER BY | Displays the operator for sorting output rows. |
| HAVING | Displays the operator for filtering with predicates on top of grouping and aggregation. |
| GROUP BY | Displays the operator for grouping and aggregation. |
| DISTINCT | Displays the operator for duplicate elimination. |
| FILTER | Displays the operator for filtering with predicates. |
| JOIN | Displays the operator for joining input relations. |
| COLUMN TABLE | Displays information about accessed column tables. |
| MULTIPROVIDER | Displays the operator for producing union-all of multiple results having the same grouping and aggregation. |

Row engine operators:

| **Operator Name** | **Description.** |
| --- | --- |
| ROW SEARCH | Displays the starting position of row engine operators. OPERATOR_DETAILS lists the projected columns. |
| LIMIT | Displays the operator for limiting the number of output rows. |
| ORDER BY | Displays the operator for sorting output rows. |
| HAVING | Displays the operator for filtering with predicates on top of grouping and aggregation. |
| GROUP BY | Displays the operator for grouping and aggregation. |
| MERGE AGGREGATION | Displays the operator for merging the results of multiple parallel grouping and aggregations. |
| DISTINCT | Displays the operator for duplicate elimination. |
| FILTER | Displays the operator for filtering with predicates. |
| UNION ALL | Displays the operator for producing union-all of input relations. |
| MATERIALIZED UNION ALL | Displays the operator for producing union-all of input relations with intermediate result materialization. |
| BTREE INDEX JOIN | Displays the operator for joining input relations through B-tree index searches. Join type suffix can be added, for example, B-tree index join for left outer join is shown as BTREE IN DEX JOIN (LEFT OUTER). Join without join type suffix means inner join. |
| CPBTREE INDEX JOIN | Displays the operator for joining input relations through CPB-tree index searches. Join type suffix can be added. |
| HASH JOIN | Displays the operator for joining input relations through probing hash table built on the fly. Join type suffix can be added. |
| NESTED LOOP JOIN | Displays the operator for joining input relations through nested looping. Join type suffix can be added. |
| MIXED INVERTED INDEX JOIN | Displays the operator for joining an input relation of row store format with a column table without format conversion using an inverted index of the column table. Join type suffix can be added. |
| BTREE INDEX SEARCH | Displays the table access through B-tree index search. |
| CPBTREE INDEX SEARCH | Displays the table access through CPB-tree index search. |
| TABLE SCAN | Displays the table access through scanning. |
| AGGR TABLE | Displays the operator for aggregating base table directly. |
| MONITOR SEARCH | Displays the monitoring view access through a search. |
| MONITOR SCAN | Displays the monitoring view access through scanning. |

## Related Information

EXPLAIN PLAN Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/EXPLAIN-PLAN-Statement-Data-Manipulation.md) ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PIN-UNPIN-SQL-PLAN-CACHE-ENTRY-Statement.md)
