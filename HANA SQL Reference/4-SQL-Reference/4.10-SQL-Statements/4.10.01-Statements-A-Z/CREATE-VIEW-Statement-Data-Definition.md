# 4.10.1.73 CREATE VIEW Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 855–867

Creates a view on the database.

## Syntax

```sql
CREATE [ OR REPLACE ] VIEW <view_name> [ COMMENT <string_literal> ]
   [ ( <column_name_list> ) ] [ ( <parameterized_view_clause> ) ]
   <as_subquery> [ <with_association_clause> ]
   [ WITH EXPRESSION MACROS( <expression_macro_list> ) ]
   [ WITH <annotations> ]
   [ WITH ANONYMIZATION ( ALGORITHM <algorithm_name>
{ [ <view_level_parameters> ] [
<column_level_parameters> ] } ) ]
   [ WITH [ CHECK OPTION ][ <mask_clause> ]
      | WITH [READ ONLY] [DDL ONLY] [ <mask_clause> ] ] [,...] ) ] ] ]
   [ <cache_clause> ]
```

## Syntax Elements

#### OR REPLACE

Replaces the view if it already exists; otherwise, if the view does not exist, it is created.

A CREATE OR REPLACE operation does not change the ID of an existing view, and maintains any privileges associated with the view.

OR REPLACE cannot be specified if the WITH ANONYMIZATION clause is specified.

#### view_name

Creates the specified view, with an optional schema name.

```sql
<view_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### COMMENT string_literal

Specifies a descriptive comment for the view.

Specifying this clause saves you from having to execute a separate COMMENT ON statement for the view after it is created.

#### column_list

Specifies the column names for the view.

```sql
<column_list> ::= <column_name> [, <column_name> [,…] ]
```

When a column name is specified along with the view name, a query result is displayed with that column name. If a column name is omitted, then a query result gives an appropriate name to the column automatically. The number of column names must be the same as the number of columns returned from `<subquery>`.

#### parameterized_view_clause

Defines the view columns by using parameters that can take input when queried.

```sql
<parameterized_view_clause> ::= <parameter_definition> [,...]
<parameter_definition> ::= IN <parameter_name> <parameter_datatype>
[ <default_value> ]
```

`<parameterized_view_clause>` can be specified with or without a `<column_name_list>` specification, as shown respectively below:

```sql
CREATE VIEW myView2 (c1, c2) (IN p1 int, IN p2 VARCHAR(10)) AS SELECT col1,
col2 FROM myTable1 WHERE col1=:p1 AND col2=:p2;
CREATE VIEW myView1 (IN p1 INT, IN p2 VARCHAR(10)) AS SELECT col1, col2 FROM
myTable1 WHERE col1=:p1 AND col2=:p2;
```

The parameter references in the WHERE clause must be preceded by a colon (for example, **:p1**) to differentiate the parameter reference from a column reference.

Parameterizing a view allows you to pass values to search for as parameters when querying the view. For example, `SELECT * FROM v1(1, 'abc');` is semantically equivalent to `SELECT * FROM (SELECT col1, col2 FROM myTable1 WHERE col1=1 AND col2='abc') v1;`.

`<default_value>` specifies the value to use, based on the `<parameter_datatype>`, if no value is specified.

#### as_subquery

The query that forms the definition for the data in the view.

```sql
<as_subquery> ::= { AS ( <subquery> ) | <with_clause> }
<with_clause> :: ( WITH <alias> AS ( <subquery> AS <alias> [,... ] ) SELECT
<expression> FROM <alias>
```

##### with_clause

Defines the columns for the view by using a common table expression.

#### with_association_clause

Defines a relationship between the view and one or more tables (or views, in the case of JOIN).

```sql
<with_association_clause> ::= WITH ASSOCIATIONS ( <association_def_list> )
<association_def_list> ::= <association_def> [,<association_def> [,…] ]
<association_def> ::= { <join_definition> | <column_def>  }
<join_definition> ::=
 <join_cardinality> JOIN <table_or_view_identifier> [ AS <table_alias> ] ON
{ <condition> | <column_def> }
<join_cardinality> ::=
 MANY TO ONE
 | MANY TO MANY
 | ONE TO ONE
 | ONE TO MANY
<column_def> ::= [ [ <schema_name>.]<table_ref>.]<column_name> [ AS
<column_name> ]
```

#### mask_clause

Adds new masking expression or drops an existing mask expression.

```sql
<mask_clause> ::= [ { DEFAULT | SESSION USER } ] MASK (< column_name> USING
<mask_expression> [,...] )
<column_name> ::= <identifier>
<mask_expression> ::= <expression>
```

Masking behavior is supported on row and column tables, and SQL row and calculation views. It is not supported on any other type of tables (virtual tables, extended tables, temporary tables etc.) and views (Join/Olap/Hierarchy views).

Only one masking behavior, definer owner-based (DEFAULT MASK) or session user based masking (SESSION USER MASK), is supported on a table or view with masked columns. You can combine both masking behaviors in an object hierarchy. For example, a view with session user based masking can be created on a table with owner-based masking.

If not specified, DEFAULT is the default.

`<mask_expression>` can be any type of expression, including a userdefined function, that returns the same data type and length as the original column.

For more information on data masking, see the SAP HANA Cloud, SAP HANA Database Security Guide.

#### WITH EXPRESSION MACROS (expression_macro_list)

Creates one or more expression macros on the view that can be called later by using the EXPRESSION_MACRO function in a query on the view.

```sql
WITH EXPRESSION MACROS( <expression_macro_list> )
<expression_macro_list> ::= <expression_macro> [, <expression_macro> [,…] ]
<expression_macro> ::=
<expression> AS <alias>
<expression_macro> ::=
{ <expression> | <expression_macro> } AS <alias>
| <expression_macro>
```

**expression_macro_list** Is a list of expression macros being created on the specified view.

##### expression_macro

Use `<expression_macro>` to reference an existing expression macro. When creating a macro expression that references another macro expression, the macro expression that is being referenced must be defined prior to the macro expression that references it.

When using `<expression_macro>` to reference an existing expression macro, then the AS clause is optional. Use the AS clause to give the new expression macro a different alias, or omit the AS clause to use the alias of the referenced expression macro.

An example for `<expression_macro>` is `sum_colA AS sum_colB` where `sum_colA` is a predefined expression macro.

##### expression

`<expression>` can be any calculation or aggregation function expression on one or more columns in the query. When using `<expression>` to create a new expression macro, you must use the AS clause to specify an alias for the expression macro. An example for `<expression>` that is a new expression macro is `AVG(columnA)`.

##### alias

`<alias>` is the name given to the expression macro.

#### WITH annotations

Specifies view-, column-, and parameter-level annotations in the form of key/value pairs. You can reference annotations in subsequent queries to filter results.

```sql
<with_annotation_clause> ::= WITH ANNOTATIONS ( { [ <set_view_annotations> ]
[ <set_column_annotations> ] [ <set_parameter_annotations> ] } )
<set_view_annotations> ::= <key_set_operation>
<set_column_annotations> ::= <column_annotation> [ <column_annotation> […] ]
<column_annotation> ::= COLUMN <column_ref> <key_set_operation>
<set_parameter_annotations> ::= <parameter_annotation>
[ <parameter_annotation> […] ]
<parameter_annotation> ::= PARAMETER <column_ref> <key_set_operation>
<key_set_operation> ::= SET <key_value_pair_list>
<key_value_pair_list> ::= <key_value_pair> [, <key_value_pair> [,…] ]
<key_value_pair> ::= '<key>'='<value>'
<column_ref> ::= <identifier>
<key> ::= <string>
<value> ::= <string>
```

While you must specify annotation on at least one object with the WITH ANNOTATION clause (view, column, or parameter), there is no limit on the number of annotations or types of annotations you can specify.

`<key>` and `<value>` represent the annotations you are configuring for the object (view, column, or parameter).

#### WITH STRUCTURED PRIVILEGE CHECK

Specifies that a user must have an SQL-based analytic privilege to access the view.

#### cache_clause

Controls whether the user can dynamically or statically cache the result of the view and get stale data. A result cache can improve performance for subsequent queries on the view.

```sql
<cache_clause> ::= [ WITH [ <cache_type> ] CACHE [ NAME <cache_name> ]
   [ RETENTION <minute_value> ]
   [ OF <projection_list> ]
   [ FILTER <filter_condition> ]
   [ <location_clause> ]
   [ FORCE ]
```

##### cache_type

Specify whether your result cache is static or dynamic.

```sql
<cache_type> ::= STATIC | DYNAMIC
```

A view has only one type of result cache. The default value is STATIC. Using a static result cache may result in stale data. A dynamic result cache ensures up-to-date data as it is partially or fully refreshed every time you run a query on the result cache.

##### minute_value

Specifies the result cache retention period.

```sql
<minute_value> ::= <unsigned_integer>
```

Specifying a retention period ensures that data does not exceed the specified RETENTION period. Data that exceeds the retention period is refreshed and up-to-date data is returned. Since a dynamic result cache ensures up-to-date data, specifying a retention period of any value other than zero (0) generates an error. Dynamic result caches are only supported for SQL views that are defined as an aggregation on single-column tables.

##### projection_list

For static result caches, allows you to reduce the cached data by specifying a result cached projection list.

```sql
<projection_list> ::= <projection_name> [{, <projection_name>}]
<projection_name> ::= <column_name> | <aggr_type>(<column_name>)
<aggr_type> ::= { SUM | MIN | MAX | COUNT | AVG }
```

If a column that is not part of the projection list is requested or included in the WHERE clause, then the result cache cannot be exploited. You can also direct an aggregation type of a specific column for the SQL view (not supported for calculation view). You specify a result cached projection list, and then the result cache includes aggregated results of that column and returns aggregated results only. This option is not supported for dynamic result caches.

##### filter_condition

Reduces the result cached data by specifying a filter condition.

```sql
<filter_condition> ::=
 <condition> OR <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>

<predicate> ::=
 <comparison_predicate>
 | <range_predicate>
 | <in_predicate>
 | <like_predicate>
 | <null_predicate>

<comparison_predicate> ::=
 <table_expression> { = | != | <> | > | < | >= | <= } [ ANY | SOME | ALL ]
( <table_expression_list> )

<range_predicate> ::=
 <table_expression> [ NOT ] BETWEEN <table_expression> AND
<table_expression>

<in_predicate> ::=
 <table_expression> [ NOT ] IN ( <table_expression_list> )

<like_predicate> ::=
 <table_expression> [ NOT ] LIKE <table_expression> [ ESCAPE
<table_expression> ]

<null_predicate> ::=
 <table_expression> IS [ NOT ] NULL
<table_expression_list> ::= <table_expression> [, <table_expression> [,
… ] ]
```

Only filtered results are cached. Predicates that contain subqueries are not supported.

For static result caches, all forms of non-parameterized query filters are supported. For parameterized query filters, only conjunctive forms are supported. For dynamic result caches, only parameterized query filters on string type columns in conjunctive forms are supported. For example:

```sql
column = ? [ AND <and_column = ?> ]
```

##### location_clause

Specifies the location where the result cache entry is created.

```sql
<location_clause> ::= AT [LOCATION] '<hostname>:<port_number>'[, ...]
```

By default, when you execute a query on a static or dynamic result cached view, the optimizer determines the result cache location. In some cases, the same result cache entry is created at multiple indexservers.

##### FORCE

For static result caches, forces the addition of a result cache without checking its cachability. This feature is only available for calculation views. This option is not supported for dynamic result caches.

#### WITH DDL ONLY

Prevents users from querying the view and from updating the underlying table. **WITH READ ONLY** Prevents the user from updating the view.

#### WITH ANONYMIZATION clause

Specifies data anonymization parameters for the view and its columns. You must execute a REFRESH VIEW statement after configuring anonymization parameters.

```sql
WITH ANONYMIZATION ( ALGORITHM <algorithm_name> { [ <view_level_parameters> ]
[ <column_level_parameters> ] } )
```

##### algorithm_name

Specifies the algorithm to use to anonymize view data.

```sql
<algorithm_name> ::= { 'K-ANONYMITY' | 'DIFFERENTIAL_PRIVACY' | 'L-
DIVERSITY' }
```

##### view_level_parameters

Specifies view-level anonymization parameters.

```sql
<view_level_parameters> ::= PARAMETERS <embedded_hierarchy_expression>
```

`<embedded_hierarchy_expression>` is a string constant containing viewspecific anonomization parameters.

##### column_level_parameters

Specifies column-level anonymization parameters.

```sql
<column_level_parameters> ::= <column_spec> [ <column_spec> […] ]
<column_spec> ::= COLUMN <column_name> PARAMETERS
<embedded_hierarchy_expression>
```

`<embedded_hierarchy_expression>` is a string constant containing columnspecific anonomization parameters.

`<column_name>` must be the name of a column previously specified in `<column_name_list>`.

For more information, see the topics on data anonymization in the SAP HANA Administration Guide.

## Description

The CREATE VIEW statement effectively creates a virtual table based on the results of an SQL statement. It is not a real table as it does not contain any data.

Update operations on views are supported when the following conditions are met:

- Each column in the view maps to the column of a single table.
- If a column in a view base table has a NOT NULL constraint without a default value, then the column must be included in view columns so that inserts can be performed.
- The view cannot contain an aggregate or analytic function in a SELECT list. For example, the following functions are not allowed:
  - TOP, SET, or DISTINCT operator in a SELECT list
  - an ORDER BY clause.
- The view cannot contain a subquery in a SELECT list
- The view cannot contain a sequence value (CURRVAL, NEXTVAL)
- The view cannot contain a column view as the base view

If the base views or tables are updatable, then a view on the base views or tables can also be updatable if the above conditions are met.

When WITH CHECK OPTION is specified, the WHERE clause cannot contain LOB data type columns, spatial data type columns, or GENERATED ALWAYS columns. When WITH CHECK OPTION is specified, the WHERE the clause of the subquery is checked against the values being inserted or updated.

## Examples

### WITH CHECK OPTION example:

Create table A.

```sql
CREATE COLUMN TABLE A (A INT PRIMARY KEY, B INT);
```

Create a view, v, that selects all records from table A.

```sql
CREATE VIEW v AS SELECT * FROM A;
```

Create a view, v, with WITH CHECK OPTION. When WITH CHECK OPTION is specified, the WHERE the clause of the subquery is checked.

```sql
CREATE VIEW v AS SELECT * FROM A WHERE A > 0 WITH CHECK OPTION;
 INSERT INTO v VALUES(1); -- succeeds
 INSERT INTO v VALUES(0); -- fails
UPDATE v set a = 0; -- fails
```

### Static and dynamic result cache examples:

Create a view, V, with a static result cache retention period of 10 minutes.

```sql
CREATE VIEW V AS SELECT DISTINCT A, B FROM A
WITH STATIC CACHE RETENTION 10;
```

Restrict the cache entry location for view_a to the location myhost2:00002.

```sql
CREATE VIEW view_a AS SELECT DISTINCT A, B FROM A
   WITH STATIC CACHE
   AT LOCATION 'myhost2:00002';
```

Create a view with a dynamic result cache.

```sql
CREATE VIEW V AS SELECT DISTINCT A, B FROM A
WITH DYNAMIC CACHE;
```

The cache is refreshed whenever it is queried.

### Masking examples:

Create the credit_card_mask function and then create a view on the fictional table credit_card_tab that uses the credit_card_mask function to mask sensitive data.

```sql
CREATE FUNCTION credit_card_mask(input VARCHAR(19))
   RETURNS output VARCHAR(19)
   LANGUAGE SQLSCRIPT
   AS temp VARCHAR(19);
BEGIN
   SELECT LEFT(input, 4) ||'-XXXX-XXXX-'||
   RIGHT(input, 4) INTO temp
   FROM SYS.DUMMY;
   output:= temp;
END;
```

```sql
CREATE VIEW credit_card_view
   AS SELECT * FROM credit_card_tab
   WITH MASK (CREDIT_CARD USING credit_card_mask(credit_card));
```

In this example for data masking, execute the following statements to create three users.

```sql
CREATE USER mask_owner PASSWORD Password1234 NO FORCE_FIRST_PASSWORD_CHANGE;
CREATE USER data_owner PASSWORD Password1234 NO FORCE_FIRST_PASSWORD_CHANGE;
CREATE USER end_user PASSWORD Password1234 NO FORCE_FIRST_PASSWORD_CHANGE;
```

Connect as data_owner and create a table called credit_tab and populate it with sensitive data.

```sql
CONNECT data_owner PASSWORD Password1234;
CREATE ROW TABLE credit_tab (Name VARCHAR(20), CREDIT_CARD VARCHAR(19));
INSERT INTO credit_tab VALUES ('John', '1111-1111-1111-1111');
INSERT INTO credit_tab VALUES ('James', '2222-2222-2222-2222');
```

Connect as mask_owner and create the userdefined function credit_mask and grant execute permission on the function to data_owner.

```sql
CONNECT mask_owner PASSWORD Password1234;
CREATE FUNCTION credit_mask(INPUT VARCHAR(19))
RETURNS OUTPUT VARCHAR(19) LANGUAGE SQLSCRIPT AS
    temp VARCHAR(19);
BEGIN
     SELECT LEFT(INPUT,4) || '-XXXX-XXXX-' || RIGHT(INPUT,4) INTO temp FROM
SYS.DUMMY;
     OUTPUT := temp;
END;
GRANT EXECUTE ON credit_mask TO data_owner;
```

Connect as data_owner and create the view credit_view using the credit_mask function as the masking expression.

```sql
CONNECT data_owner PASSWORD Password1234;
CREATE VIEW credit_view AS SELECT * FROM credit_tab
WITH MASK (CREDIT_CARD USING mask_owner.credit_mask(credit_card));
GRANT SELECT ON credit_view TO end_user;
```

Connect as end_user and query credit_view.

```sql
CONNECT end_user PASSWORD Password1234;
SELECT * FROM data_owner.credit_view;
```

The query returns the following masked results:

| **NAME** | **CREDIT_CARD** |
| --- | --- |
| John | 1111-XXXX-XXXX-1111 |
| James | 2222-XXXX-XXXX-2222 |

Connect as data_owner and alter the masking definition for credit_view.

```sql
CONNECT data_owner PASSWORD Password1234;
ALTER VIEW credit_view AS SELECT name, credit_card FROM credit_tab
WITH MASK (NAME USING 'AAAA', CREDIT_CARD USING 'XXXX');
```

Connect as end_user and query credit_view again.

```sql
CONNECT end_user PASSWORD Password1234;
SELECT * FROM data_owner.credit_view;
```

The query returns the following masked results:

| **NAME** | **CREDIT_CARD** |
| --- | --- |
| AAAA | XXXX |
| AAAA | XXXX |

Connect as data_owner and drop masking for the name and credit_card columns.

```sql
CONNECT data_owner PASSWORD Password1234;
ALTER VIEW credit_view DROP MASK (NAME, CREDIT_CARD);
```

Connect as end_user and query credit_view.

```sql
CONNECT end_user PASSWORD Password1234;
SELECT * FROM data_owner.credit_view;
```

Because data masking has been dropped, all data contained in the view is now visible.

| **NAME** | **CREDIT_CARD** |
| --- | --- |
| John | 1111-1111-1111-1111 |
| James | 2222-2222-2222-2222 |

Connect as data_owner and mask data in the credit_card column by executing the following statement.

```sql
CONNECT data_owner password Password1234;
ALTER VIEW credit_view ADD MASK (CREDIT_CARD USING 'XXXX');
```

Connect as end_user and query credit_view.

```sql
CONNECT end_user PASSWORD Password1234;
SELECT * FROM data_owner.credit_view;
```

The data in the credit_card column is masked in the result set as follows:

| **NAME** | **CREDIT_CARD** |
| --- | --- |
| John | XXXX |
| James | XXXX |

Connect as data_owner and alter the masking information on the credit card to once again use the credit_mask function.

```sql
CONNECT data_owner PASSWORD Password1234;
ALTER VIEW credit_view ALTER MASK (CREDIT_CARD USING
mask_owner.credit_mask(credit_card));
```

Connect as end_user and query credit_view.

```sql
CONNECT end_user PASSWORD Password1234;
SELECT * FROM data_owner.credit_view;
```

The data in the result set is once again masked by using the credit_mask function.

| **NAME** | **CREDIT_CARD** |
| --- | --- |
| John | 1111-XXXX-XXXX-1111 |
| James | 2222-XXXX-XXXX-2222 |

### WITH EXPRESSION MACROS examples:

The following statements create a table, insert data, and create a view with two expression macros (`sum_a` and `count_a`) that calculate the sum and count of column `t1.a`, respectively:

```sql
CREATE TABLE t1(a INT);
INSERT INTO t1 VALUES(10);
INSERT INTO t1 VALUES(20);
CREATE VIEW v1 AS SELECT * FROM t1 WITH EXPRESSION MACROS(SUM(a) AS sum_a,
COUNT(a) AS count_a);
```

The following statements create a view, v1, with two expression macros:

```sql
CREATE TABLE t(x INT, y INT);
CREATE VIEW v1 AS SELECT * FROM t WITH EXPRESSION MACROS (
   SUM(x) AS sum_x,
   AVG(y) AS avg_y
);
```

Now execute the following statements to create a second view, v2, with three expression macros.

```sql
CREATE VIEW v2 AS SELECT * FROM v1 WITH EXPRESSION MACROS (
   sum_x AS sum_x2,
   avg_y,
   COUNT(x) AS count_x
);
```

The first two expression macros are propagated from v1. sum_x is renamed to sum_x2 for v2, whereas avg_y retains its alias. The third expression macro is newly created as count_x.

### WITH ANNOTATIONS example:

The following example creates a table with annotations and then creates a view that also has annotations:

```sql
CREATE TABLE t1(c1 INT) WITH ANNOTATIONS(
    SET 't_k1' = 't_v1', 't_k2' = 't_v2'
    COLUMN c1 SET 'c_k1' = 'c_v1', 'c_k2' = 'c_v2');
CREATE VIEW v1 AS SELECT * FROM t1 WITH ANNOTATIONS(
    SET 'v_k1' = 'v_v1', 'v_k2' = 'v_v2'
    COLUMN c1 SET 'c_k1' = 'c_v1', 'c_k2' = 'c_v2'
```

### WITH DDL ONLY example:

The following statements show how you to use the WITH DDL ONLY clause to control whether users can query a view:

```sql
CREATE TABLE t1 (a int, b int);
CREATE VIEW v1 AS SELECT * FROM t1 WITH DDL ONLY;
SELECT * FROM v1; -- invalid view name: cannot select the view because it is in
DDL-only mode
SELECT IS_DDL_ONLY from VIEWS where VIEW_NAME = 'V1'; -- returns TRUE
CREATE VIEW v2 AS SELECT * FROM v1; -- you can select from the view
```

### WITH ANONYMIZATION example:

The following statements create a table called `Illness` with sensitive data in a column called `Illness` (illness-related), and populate the table with data:

```sql
CREATE COLUMN TABLE Illness (
  -- Sequential Column
  ID BIGINT NOT NULL PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
  -- Identifiers
  Name VARCHAR(10),
  -- Quasi Identifiers (QIDs) (to be generalized)
  Gender VARCHAR(1) NOT NULL,
  City VARCHAR(10) NOT NULL,
  -- Sensitive Data
  Illness VARCHAR(10) NOT NULL);
INSERT INTO ILLNESS VALUES ('Paul', 'M', 'Paris', 'BRONCHITIS');
INSERT INTO ILLNESS VALUES ('Martin', 'M', 'Munich', 'ANGINA');
INSERT INTO ILLNESS VALUES ('Nils', 'M', 'Nice', 'FLU');
INSERT INTO ILLNESS VALUES ('Annika', 'F', 'Munich', 'BROKEN LEG');
```

You can now create a view that anonymizes the data:

```sql
CREATE VIEW Illness_K_Anon (ID, Gender, Location, Illness)
            AS SELECT ID, Gender, City AS Location, Illness
            FROM Illness
            WITH ANONYMIZATION ( ALGORITHM 'K-ANONYMITY'
            PARAMETERS '{"data_change_strategy": "qualified", "k": 2}'
            COLUMN ID PARAMETERS '{"is_sequence": true}'
            COLUMN Gender PARAMETERS '{"is_quasi_identifier":true, "hierarchy":
{"embedded": [["F"], ["M"]]}}'
            COLUMN Location PARAMETERS '{"is_quasi_identifier":true, "hierarchy":
{"embedded": [["Paris", "France"], ["Munich", "Germany"], ["Nice",
"France"]]}}');
```

After you create the anonymized view, you must refresh it to select from it:

```sql
REFRESH VIEW Illness_K_Anon ANONYMIZATION;
```

View the anonymized data in the view:

```sql
SELECT * FROM Illness_K_Anon;
```

| **ID** | **GENDER** | **LOCATION** | **ILLNESS** |
| --- | --- | --- | --- |
| 1 | \* | France | BRONCHITIS |
| 2 | \* | Germany | ANGINA |
| 3 | \* | France | FLU |
| 4 | \* | Germany | BROKEN LEG |

## Related Information

ALTER VIEW Statement (Data Definition) [→](ALTER-VIEW-Statement-Data-Definition.md) VIEW_EXPRESSION_MACROS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEW_EXPRESSION_MACROS-System-View.md) EXPRESSION_MACRO Function (Miscellaneous) [→](../../4.09-SQL-Functions/4.09.01-Functions-A-Z/EXPRESSION_MACRO-Function-Miscellaneous.md) Expressions [→](../../4.06-Expressions.md) REFRESH VIEW Statement (Data Definition) [→](REFRESH-VIEW-Statement-Data-Definition.md) VIEWS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEWS-System-View.md) VIEW_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEW_COLUMNS-System-View.md)
