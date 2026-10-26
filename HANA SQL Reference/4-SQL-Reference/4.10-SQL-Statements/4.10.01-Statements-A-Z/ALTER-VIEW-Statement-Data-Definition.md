# 4.10.1.23 ALTER VIEW Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 636–644

Alters the definition, restrictions, or options on a view.

## Syntax

```sql
ALTER VIEW <view_name> {
 [ ( <column_name_list> ) ] AS <subquery> [ <view_option_list> ] [ <view_cache> ]
 | <cache_clause>
 | <mask_clause>
 | <expression_macros>
 | <view_access_modes>
 | WITH ANONYMIZATION ( ALGORITHM <algorithm_name> { [ <view_level_parameters> ]
[ <column_level_parameters> ] } )
}
<view_option_list> ::=  <view_restriction> <view_associations> <view_annotations>
```

## Syntax Elements

#### view_name

Specifies the identifier of the view to be altered, with optional schema name.

```sql
<view_name> ::= [ <schema_name>. ]<identifier>
```

#### column_name_list

Specifies the column names in the view. **AS subquery** Specifies the subquery to use for populating the view with data.

#### view_restrictions

Sets restrictions based on structured privileges.

```sql
<view_restriction> ::=
 WITH CHECK OPTION [ <column_mask_clause> ] [ <structured_privilege_check> ]
 | WITH NO CHECK OPTION [ <column_mask_clause> ]
[ <structured_privilege_check> ]
 | WITH READ ONLY [ <column_mask_clause> ] [ <structured_privilege_check> ]
 | WITH NO READ ONLY [ <column_mask_clause> ] [ <structured_privilege_check> ]
 | WITH <column_mask_clause> [ <structured_privilege_check> ]
 | WITH <structured_privilege_check>
<column_mask_clause> ::= MASK ( <column_mask_list> )
<column_mask_list> ::= <column_mask> [, <column_mask> [,…] ]
<column_mask> ::= <column_name> USING <mask_expression>
<structured_privilege_check> ::= { STRUCTURED PRIVILEGE CHECK | NO STRUCTURED
PRIVILEGE CHECK }
```

`<mask_expression>` can be any type of expression, including a userdefined function, but it cannot be a subquery.

> **Note**
>
> This DDL is only supported for SQL views.

For more information on data masking, see the SAP HANA Security Guide.

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

#### with_annotation_clause

Alters table-, column-, and parameter-level annotations. You can reference annotations in subsequent queries to filter results.

```sql
<with_annotation_clause> ::=
 WITH ANNOTATIONS ( { [ <view_annotations> ] [ <column_annotations> ]
[ <parameter_annotations> ] } )
<view_annotations> ::= { [ <key_set_operation> ] [ <key_unset_operation> ] }
<column_annotations> ::= <column_annotation> [ <column_annotation> […] ]
<column_annotation> ::= COLUMN <column_ref> { <key_set_operation> |
<key_unset_operation> }
<parameter_annotations> ::= <parameter_annotation> [ <parameter_annotation>
[…] ]
<parameter_annotation> ::= PARAMETER <column_ref> { <key_set_operation> |
<key_unset_operation> }
<key_set_operation> ::= SET <key_value_pair_list>
<key_unset_operation> ::= UNSET <key_list>
<key_value_pair_list> ::= <key_value_pair> [, <key_value_pair> [,…] ]
<key_value_pair> ::= '<key>'='<value>'
<key_list> ::= { '<key>'[,'<key>'[,…]] | ALL }
<column_ref> ::= <identifier>
<key> ::= <string>
<value> ::= <string>
```

While you must specify annotation on at least one object with the WITH ANNOTATION clause (view, column, or parameter), there is no limit on the number of annotations or types of annotations you can specify.

`<key>` and `<value>` represent the annotations you are configuring for the object (view, column, or parameter).

#### cache_clause

Changes result cache settings for a vew.

```sql
<cache_clause> ::=
   { <add_cache_clause>
   | <alter_cache_clause>
   | <drop_cache_clause> }
```

##### add_cache_clause

Caches the result of a table function with an optional projection list and filter conditions. A result cache can improve performance for subsequent queries on the view.

```sql
<add_cache_clause> ::=
   ADD [ <cache_type> ] CACHE
   [ RETENTION <minute_value> ]
   [ OF <projection_list> ]
   [ FILTER <filter_condition> ]
   [ <location_clause> ]
   [ FORCE ]
```

###### cache_type

Specify whether your result cache is static or dynamic.

```sql
<cache_type> ::= STATIC | DYNAMIC
```

A view has only one type of result cache. The default value is STATIC. Using a static result cache may result in stale data. A dynamic result cache ensures up-to-date data as it is partially or fully refreshed every time you run a query on the result cache.

###### minute_value

Specifies the result cache retention period.

```sql
<minute_value> ::= <unsigned_integer>
```

Specifying a retention period ensures that data does not exceed the specified RETENTION period. Data that exceeds the retention period is refreshed and up-to-date data is returned. Since a dynamic result cache ensures up-to-date data, specifying a retention period of any value other than zero (0) generates an error. Dynamic result caches are only supported for SQL views that are defined as an aggregation on single-column tables.

###### projection_list

For static result caches, allows you to reduce the cached data by specifying a result cached projection list.

```sql
<projection_list> ::= <projection_name> [{, <projection_name>}]
<projection_name> ::= <column_name> | <aggr_type>(<column_name>)
<aggr_type> ::= { SUM | MIN | MAX | COUNT | AVG }
```

If a column that is not part of the projection list is requested or included in the WHERE clause, then the result cache cannot be exploited. You can also direct an aggregation type of a specific column for the SQL view (not supported for calculation view). You specify a result cached projection list, and then the result cache includes aggregated results of that column and returns aggregated results only. This option is not supported for dynamic result caches.

###### filter_condition

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
 <table_expression> { = | != | <> | > | < | >= | <= } [ ANY | SOME |
ALL ] ( <table_expression_list> )

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

###### location_clause

Specifies the location where the result cache entry is created.

```sql
<location_clause> ::= AT [LOCATION] '<hostname>:<port_number>'[, ...]
```

By default, when you execute a query on a static or dynamic result cached view, the optimizer determines the result cache location. In some cases, the same result cache entry is created at multiple indexservers.

##### alter_cache_clause

Changes the result cache.

```sql
<alter_cache_clause> ::=
   ALTER [ <cache_type> ] CACHE
   { <alter_retention_clause > | <alter_location_clause> | <index_clause> }
<cache_type> ::= STATIC | DYNAMIC
<alter_retention_clause > ::= RETENTION <minute_value>
<alter_location_clause> ::=  { ADD | DROP } AT [ LOCATION ]
'<hostname>:<port_number>'[, ...]
<index_clause> ::= { ADD | DROP } INDEX ON <column_name>
```

For static caches, you can change the retention value of the result cache of a view. For dynamic caches, only the value 0 is supported.

Use the `<location_clause>` to change the location where the cache entry is created. By default, when you execute a query on a static or dynamic cached view, the optimizer determines the cache location. In some cases, the same cache entry is created at multiple indexservers. `<host_port>` specifies the hostname and port of an currently running indexserver.

Use the `<index_clause>` to create an index on a dynamic result cache to improve filter evaluation performance on the top of the dynamic result cache. The `<index_clause>` is not supported for static caches. Dynamic result cache indexes are restricted to single-node systems only.

##### drop_cache_clause

Specifies to drop the result cache of a view.

```sql
<drop_cache_clause> ::= DROP [ <cache_type> ] CACHE
<cache_type> ::= { STATIC | DYNAMIC }
```

#### mask_clause

Adds new masking expression or drops an existing mask expression. `<mask_clause>` does not change the view's column definitions. For an example of data masking, see the CREATE VIEW statement.

```sql
<mask_clause> ::=
 { ADD | ALTER } MASK (<column_mask_list>)
 | DROP MASK ( <column_name_list> )
<column_mask_list> ::= ( <column_name> USING <mask_expression> [,…] )
<mask_expression> ::= <expression>
<column_name_list> ::= <column_name>[,...]
```

When adding a mask expression, the mask behavior is defined for the object. New column masks must use the same mask mode. When altering, you can change the mask expression, but not the mode. Once all existing masks are dropped, you can add new masks using a different mask mode.

Masking behavior is supported on row and column tables, and SQL row and calculation views. It is not supported on any other type of tables (virtual tables, extended tables, temporary tables etc.) and views (Join/Olap/Hierarchy views).

Only one masking behavior, definer owner-based (DEFAULT MASK) or session user based masking (SESSION USER MASK), is supported on a table or view with masked columns. You can combine both masking behaviors in an object hierarchy. For example, a view with session user based masking can be created on a table with owner-based masking.

If not specified, DEFAULT is the default.

`<mask_expression>` can be any type of expression, including a userdefined function, that returns the same data type and length as the original column.

For more information on data masking, see the SAP HANA Cloud, SAP HANA Database Security Guide.

#### expression_macros

Adds or drops one or more expression macros for the view.

Expression macros perform calculations on the results of a query on a view before the results are returned, and are called using the EXPRESSION_MACRO function.

```sql
<expression_macros> ::=
ADD EXPRESSION MACROS( <expression_macro_list> )
 | DROP EXPRESSION MACROS( <expression_macro_alias_list> )
<expression_macro_list> ::= <expression_macro> [, <expression_macro> [,…] ]
<expression_macro> ::= <expression> AS <expression_macro_alias>
<expression_macro_alias_list> ::= <expression_macro_alias> [,
<expression_macro_alias> [,…] ]
```

`<expression>` can be any calculation or aggregation function expression on one or more columns in the query, including a call to the EXPRESSION_MACRO function. A couple examples for `<expression>` might be `AVG(columnA)`, or `EXPRESSION_MACRO(sum_colA)`, where `sum_colA` is another expression macro.

`<expression_macro_alias>` is the name given to the expression macro. You cannot drop an expression macro if another expression macro references it; you must first drop the referring expression macro.

#### view_access_modes

Specifies the access mode without recompiling the view query or propagating recompilations of dependent view.

```sql
<view_access_modes> ::=
```

**[NO] READ ONLY** Specifies whether the view is read only. If READ ONLY is specified, and one of the base objects is not updatable, then the view cannot be updated. If subsequently the base objects are changed to updatable, and the view is not READ ONLY, then the view becomes updatable without executing the ALTER VIEW statement again.

##### [NO] DDL ONLY

Controls whether users can query the view or update the underlying table. You can include views that are defined WITH DDL ONLY in other object definitions. Specifying WITH DDL ONLY prevents users from querying the view and from modifying the underlying table.

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

Alters the definition, restrictions, or options on a view.

To change the comment on a view, use the COMMENT ON statement.

## Examples

### Result caching examples

The following example creates a table named TAB, and then creates a view, V, that selects all records from it:.

```sql
CREATE COLUMN TABLE TAB (COL1 INT PRIMARY KEY, COL2 INT);
CREATE VIEW V AS SELECT DISTINCT COL1, COL2 FROM TAB;
```

The following example adds the result cache to view V, and enable static result caching.

```sql
ALTER VIEW V ADD STATIC CACHE RETENTION 10;
```

The following example changes the retention value of the result cache of the view V.

```sql
ALTER VIEW V ALTER STATIC CACHE RETENTION 20;
```

The following example drops the result cache of view V.

```sql
ALTER VIEW V DROP STATIC CACHE;
```

The following example enables dynamic result caching on view V.

```sql
ALTER V ADD DYNAMIC CACHE;
```

The following example restricts the cache entry location for `view_a` to the location `myhost2:00002`.

```sql
ALTER VIEW view_a ADD STATIC CACHE AT LOCATION 'myhost2:00002';
```

The following example removes the location specifications so that there are no restrictions on the cache entry location for `view_a`.

```sql
ALTER VIEW view_a ALTER STATIC CACHE DROP AT LOCATION 'myhost2:00002';
```

The following statements show how you can add, alter, or drop the RESULT CACHE on a view:

```sql
CREATE ROW TABLE TAB (COL1 INT PRIMARY KEY, COL2 INT);
CREATE VIEW V AS SELECT * FROM TAB;
ALTER VIEW V ADD STATIC CACHE RETENTION 10;
ALTER VIEW V ALTER STATIC CACHE RETENTION 20;
ALTER VIEW V DROP STATIC CACHE;
```

### Static cache retention example

Create and populate table T and then create view V_1 based on the table:

```sql
CREATE COLUMN TABLE T ( A INT, B INT, C INT );
INSERT INTO T VALUES (1, 1, 10);
INSERT INTO T VALUES (2, 2, 10);
INSERT INTO T VALUES (3, 3, 10);
CREATE VIEW V_1 AS (SELECT A, B, C FROM T);
```

Then alter view V_1 to add to add a static cache retention of 1000 minutes for column A, the aggregated sum of column B, and the aggregated average of column C:

```sql
ALTER VIEW V_1 ADD STATIC CACHE RETENTION 1000 OF A, SUM(B), AVG(C);
```

When you run the following SELECT statement, the new cache is used:

```sql
SELECT A, SUM(B), AVG(C) FROM V_1 GROUP BY A WITH HINT (RESULT_CACHE);
```

### Add/drop dynamic cache index examples

```sql
CREATE COLUMN TABLE tab_a ( A INT, B INT, C INT, D INT);
CREATE VIEW view_a AS (SELECT A, B, sum(D) D from tab_a group by A, B);
ALTER VIEW view_a ADD DYNAMIC CACHE;
```

Execute the following statement to add a dynamic cache index on the column A:

```sql
ALTER VIEW view_a ALTER DYNAMIC CACHE ADD INDEX ON A;
```

Execute the following statement to add an additional dynamic cache index on the column B:

```sql
ALTER VIEW view_a ALTER DYNAMIC CACHE ADD INDEX ON B;
```

Execute the following statement to drop the dynamic cache index on column B:

```sql
ALTER VIEW view_a ALTER DYNAMIC CACHE DROP INDEX ON B;
```

### Expression macros examples

The following statements create a view with two expression macros (`sum_a` and `count_a`) and then alters the view to add another expression macro (`avg_a`) to it:

```sql
CREATE TABLE t1(a INT);
CREATE VIEW v1 AS SELECT * FROM t1 WITH EXPRESSION MACROS(SUM(a) AS sum_a,
COUNT(a) AS count_a);
ALTER VIEW v1 ADD EXPRESSION MACROS(AVG(a) AS avg_a);
```

The following statement alters the view to add an expression macro (`avg2_a`) that also calculates the average of column `a` but by using two of the other expression macros in the calculation:

```sql
ALTER VIEW v1 ADD EXPRESSION MACROS(EXPRESSION_MACRO(sum_a) /
EXPRESSION_MACRO(count_a) AS avg2_a);
```

The following example drops the two expression macros `avg_a` and `avg2_a`:

```sql
ALTER VIEW v1 DROP EXPRESSION MACROS( avg_a, avg2_a );
```

### WITH ANNOTATIONS examples

The following statement alters annotations on the myView view:

```sql
ALTER VIEW myView WITH ANNOTATIONS (
 UNSET 'key1' SET 'key1' = 'value1'
 COLUMN column1 UNSET 'Key2' SET 'Key2' = 'value2' );
```

### WITH DDL ONLY examples

The following statements show how to use the WITH DDL ONLY clause to control whether users can query a view:

```sql
CREATE TABLE t1 (a int, b int);
CREATE VIEW v1 AS SELECT * FROM t1 WITH DDL ONLY;
ALTER VIEW v1 AS SELECT * FROM t1 WITH NO DDL ONLY;
SELECT * FROM v1; -- OK
SELECT IS_DDL_ONLY FROM VIEWS WHERE VIEW_NAME = 'V1'; -- FALSE

ALTER VIEW v1 AS SELECT * FROM t1 WITH DDL ONLY;
SELECT * FROM v1; -- invalid view name: cannot select the DDL only mode view
```

## Related Information

CREATE VIEW Statement (Data Definition) [→](CREATE-VIEW-Statement-Data-Definition.md) VIEW_EXPRESSION_MACROS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEW_EXPRESSION_MACROS-System-View.md) EXPRESSION_MACRO Function (Miscellaneous) [→](../../4.09-SQL-Functions/4.09.01-Functions-A-Z/EXPRESSION_MACRO-Function-Miscellaneous.md) COMMENT ON Statement (Data Definition) [→](COMMENT-ON-Statement-Data-Definition.md) ANNOTATE Statement (Data Definition) [→](ANNOTATE-Statement-Data-Definition.md) ANNOTATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ANNOTATIONS-System-View.md) REFRESH VIEW Statement (Data Definition) [→](REFRESH-VIEW-Statement-Data-Definition.md) Predicates [→](../../4.07-Predicates/README.md)
