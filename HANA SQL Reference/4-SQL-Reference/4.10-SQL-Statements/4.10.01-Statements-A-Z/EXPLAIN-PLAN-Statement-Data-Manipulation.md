# 4.10.1.116 EXPLAIN PLAN Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 937–942

Evaluates the execution plan that the database follows when executing an SQL statement.

## Syntax

```sql
EXPLAIN PLAN [ SET STATEMENT_NAME = <statement_name> ] FOR <explain_plan_entry>
```

## Syntax Elements

#### statement_name

Specifies the name of a specific execution plan in the output table for a given SQL statement.

```sql
<statement_name> ::= <string_literal>
```

#### explain_plan_entry

Specifies the entry to explain.

```sql
<explain_plan_entry> ::=
 <subquery>
 | SQL PLAN CACHE ENTRY <plan_id>
<plan_id> ::= <integer_literal>
```

The `<plan_id>` specifies the identifier of an entry to be explained, which is already in the SQL plan cache. Refer to the M_SQL_PLAN_CACHE monitoring view to find the `<plan_id>` for the desired cache entry.

##### subquery

Specifies the subquery to explain the plan for. For more information about subqueries, see the SELECT statement.

## Permissions

The EXPLAIN PLAN [SET STATEMENT_NAME = `<statement_name>`] FOR SQL PLAN CACHE ENTRY `<plan_id>` command can only be run by users with the OPTIMIZER_ADMIN privilege.

## Description

Using this command, a user can see the execution plan of a subquery, or that of an entry already in the SQL plan cache. The result of the evaluation is stored in the EXPLAIN_PLAN_TABLE view for examination.

The SQL `<subquery>` must be one of the following type of statements. INSERT, UPDATE, DELETE, REPLACE, UPSERT, MERGE INTO and SELECT. All other type of statements cannot be used with EXPLAIN PLAN. The same rule is applied to the plan cache entry. That is, the cache entry a user specified using `<plan_id>` should be a one of the statements listed above.

## Example

In the OPERATOR_NAME of the EXPLAIN_PLAN_TABLE system view:

- COLUMN SEARCH denotes the starting position of column engine operators.
- ROW SEARCH denotes the starting position of row engine operators.

In the example below, the intermediate result produced by a COLUMN SEARCH (ID 10) is consumed by a ROW SEARCH (ID 7). The intermediate result produced by the ROW SEARCH (ID 7) is consumed by another COLUMN SEARCH (ID 1).

The operators below the lowest COLUMN SEARCH (ID 10) explain how the COLUMN SEARCH (ID 10) is executed.

The operators between the ROW SEARCH (ID 7) and the COLUMN SEARCH (ID 10) explain how the ROW SEARCH (ID 7) processes the intermediate result produced by the COLUMN SEARCH (ID 10).

The operators between the top COLUMN SEARCH (ID 1) and the ROW SEARCH (ID 7) explain how the top COLUMN SEARCH (ID 1) processes the intermediate result produced by the ROW SEARCH (ID 7).

| **OPERATOR_NAME** | **OPERATOR_ID** | **PARENT_OPERATOR_ID** | **LEVEL** | **POSITION** |
| --- | --- | --- | --- | --- |
| COLUMN SEARCH | 1 | NULL | 1 | 1 |
| LIMIT | 2 | 1 | 2 | 1 |
| ORDER BY | 3 | 2 | 3 | 1 |
| GROUP BY | 4 | 3 | 4 | 1 |
| JOIN | 5 | 4 | 5 | 1 |
| COLUMN TABLE | 6 | 5 | 6 | 1 |
| ROW SEARCH | 7 | 5 | 6 | 2 |
| BTREE INDEX JOIN | 8 | 7 | 7 | 1 |
| BTREE INDEX JOIN | 9 | 8 | 8 | 1 |
| COLUMN SEARCH | 10 | 9< | >9 | 1 |
| FILTER | 11 | 10 | 10 | 1 |
| COLUMN TABLE | 12 | 11 | 11 | 1 |

### SQL plan explanation

Here is an example query plan explanation. In the example, all tables are located on row store.

```sql
DELETE FROM explain_plan_table WHERE statement_name = 'TPC-H Q10';
EXPLAIN PLAN SET STATEMENT_NAME = 'TPC-H Q10' FOR
   SELECT TOP 20
      c_custkey,
      c_name,
      SUM(l_extendedprice * (1 - l_discount)) AS revenue,
      c_acctbal,
      n_name,
      c_address,
      c_phone,
      c_comment
      FROM
         customer,
         orders,
         lineitem,
         nation
      WHERE
         c_custkey = o_custkey
      AND l_orderkey = o_orderkey
      AND o_orderdate >= '1993-10-01'
      AND o_orderdate < ADD_MONTHS('1993-10-01',3)
      AND l_returnflag = 'R'
      AND c_nationkey = n_nationkey
      GROUP BY
         c_custkey,
      c_name,
      c_acctbal,
      c_phone,
      n_name,
      c_address,
      c_comment
   ORDER BY
      revenue DESC;
SELECT operator_name, operator_details, table_name
   FROM explain_plan_table
   WHERE statement_name = 'TPC-H Q10';
```

Or, suppose that you execute the following statement, which is the same as the `<subquery>` in the example above, and then obtain the `<plan_id>` = 2050002 of the entry from PLAN_ID column in M_SQL_PLAN_CACHE monitoring view.

```sql
SELECT TOP 20
   c_custkey,
   c_name,
   SUM(l_extendedprice * (1 - l_discount)) AS revenue,
   c_acctbal,
   n_name,
   c_address,
   c_phone,
   c_comment
    FROM
       customer,
       orders,
       lineitem,
       nation
    WHERE
       c_custkey = o_custkey
       AND l_orderkey = o_orderkey
       AND o_orderdate >= '1993-10-01'
       AND o_orderdate < ADD_MONTHS('1993-10-01',3)
       AND l_returnflag = 'R'
       AND c_nationkey = n_nationkey
    GROUP BY
       c_custkey,
       c_name,
       c_acctbal,
       c_phone,
       n_name,
       c_address,
       c_comment
    ORDER BY
       revenue DESC;
DELETE FROM explain_plan_table WHERE statement_name = 'TPC-H Q10';
EXPLAIN PLAN SET STATEMENT_NAME = 'TPC-H Q10' FOR SQL PLAN CACHE ENTRY 2050002;
SELECT operator_name, operator_details, table_name
   FROM explain_plan_table
   WHERE statement_name = 'TPC-H Q10';
```

The two examples give the same following result table.

| **OPERATOR_NAME** | **OPERATOR_DETAILS** | **TABLE_NAME** |
| --- | --- | --- |
| ROW SEARCH | CUSTOMER.C_CUSTKEY, CUS TOMER.C_NAME, SUM(LINEI TEM.L_EXTENDEDPRICE \* (1 - LINEI TEM.L_DISCOUNT)), CUS TOMER.C_ACCTBAL, NA TION.N_NAME, CUSTOMER.C_ADDRESS, CUSTOMER.C_PHONE, CUS TOMER.C_COMMENT | None |
| LIMIT | NUM RECORDS: 20 |   |
| ORDER BY | SUM(LINEITEM.L_EXTENDEDPRICE \* (1 - LINEITEM.L_DISCOUNT)) DESC | None |
| MERGE AGGREGATION | NUM PARTITIONS: 4 | None |
| GROUP BY | GROUPING: NATION.N_NAME, R_CUSTOMER.C_CUSTKEY, AGGREGATION: SUM(LINEITEM.L_EXTENDEDPRICE \* (1 - LINEITEM.L_DISCOUNT)) | None |
| CPBTREE INDEX JOIN | INDEX NAME: _SYS_TREE_RS_279_#0_#P0,<br>INDEX CONDITION: ORDERS.O_ORDERKEY = LINEITEM.L_ORDERKEY,<br>INDEX FILTER: 'R' = LINEITEM.L_RETURNFLAG | LINEITEM |
| BTREE INDEX JOIN | INDEX NAME: _SYS_TREE_RS_285_#0_#P0,<br>INDEX CONDITION: CUSTOMER.C_NATIONKEY = NATION.N_NATIONKEY | NATION |
| BTREE INDEX JOIN | INDEX NAME: _SYS_TREE_RS_283_#0_#P0,<br>INDEX CONDITION: ORDERS.O_CUSTKEY = CUSTOMER.C_CUSTKEY | CUSTOMER |
| TABLE SCAN | FILTER CONDITION: ORDERS.O_ORDERDATE < '1994-01-01' AND OR DERS.O_ORDERDATE >= '1993-10-01' | ORDERS |

From this plan result we can obtain the following facts about this query:

- TABLE SCAN is executed on ORDERS with the FILTER CONDITION.
- BTREE INDEX JOIN is executed with the B-tree index of CUSTOMER and the result of the TABLE SCAN below.
- BTREE INDEX JOIN is executed with the B-tree index of NATION and the result of the BTREE INDEX JOIN below.
- CPBTREE INDEX JOIN is executed with the CPB-tree index of LINEITEM and the result of the BTREE INDEX JOIN below.
- GROUP BY is executed with the result of the CPBTREE INDEX JOIN below, with 4 threads.
- MERGE AGGREGATION is executed with the result of the GROUP BY below.
