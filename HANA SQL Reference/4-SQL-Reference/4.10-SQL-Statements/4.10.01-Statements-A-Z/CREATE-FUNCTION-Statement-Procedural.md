# 4.10.1.50 CREATE FUNCTION Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 711–719

Creates a userdefined function.

Syntax

```sql
CREATE [ OR REPLACE ] FUNCTION <function_name> [ ( <input_parameter_clause> ) ]
 RETURNS <return_type>
 [ LANGUAGE <lang> ]
 [ SQL SECURITY <mode> ]
 [ DEFAULT SCHEMA <default_schema_name> ]
 [ <variable_cache_clause> ]
 [ DETERMINISTIC ]
 [ WITH ENCRYPTION ]
  AS
   { BEGIN
        <statement_body>
     END [ <cache_clause> ]
     | HEADER ONLY }
```

## Syntax Elements

#### function_name

Specifies the function name, and optionally, a schema name.

```sql
<function_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### input_parameter_clause

Specifies the input parameters for the function.

```sql
<input_parameter_clause> ::= <parameter> [,...] ]
<parameter> ::= [ IN ] <param_name> <data_type>
<param_name> ::= <identifier>
<data_type> ::=
    <sql_type> [ ARRAY ]
    | <table_type>
    | <table_type_definition>
    | <any_table_type>
```

Scalar userdefined functions support primitive SQL types, as well as table parameters (actual physical tabes), views, and table variables. Table userdefined functions support table types as input.

##### sql_type [ ARRAY ]

Specifies the SQL type. Use the optional ARRAY keyword with `<sql_type>` if the parameter is an array.

```sql
<sql_type> ::=
 DATE
 | TIME
 | TIMESTAMP
 | SECONDDATE
 | TINYINT
 | SMALLINT
 | INTEGER
 | BIGINT
 | DECIMAL
 | SMALLDECIMAL
 | REAL
 | DOUBLE
 | VARCHAR
 | NVARCHAR
 | ALPHANUM
 | VARBINARY
 | CLOB
 | NCLOB
 | BLOB
```

Scalar userdefined functions do not support ALPHANUM, VARBINARY, CLOB, NCLOB, or BLOB types.

##### table_type

Specifies a table type that was previously defined with the CREATE TYPE statement.

```sql
<table_type> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

##### table_type_definition

Specifies a table type that is implicitly defined within the signature.

```sql
<table_type_definition> ::= TABLE (<column_list_definition>)
<column_list_definition> ::= <column_elem>[, <column_elem> [,…] ]
<column_elem> ::= <column_name> <data_type>
<column_name> ::= <identifier>
```

##### any_table_type

Defines the table type at DDL time or query compilation time.

```sql
<any_table_type> ::= TABLE(...)
```

The syntax of `<any_table_type>` requires you to explicitly specify **TABLE(…)** (for example, `CREATE FUNCTION anyfunc_in (IN itab TABLE(...), outtab TABLE(...) ) AS BEGIN…`).

#### RETURNS return_type

Specifies the return type.

```sql
<return_type> ::= { <return_parameter_list> | <return_table_type> }
```

Scalar functions must return scalar values specified in `<return_parameter_list>`. Table functions must return a table whose type is defined by `<return_table_type>`.

##### return_parameter_list

Specifies the output parameters. Use the optional ARRAY keyword for `<sql_type>` if the return parameter is an array.

```sql
<return_parameter_list> ::= <return_parameter>[, <return_parameter> [,…] ]
<return_parameter> ::= <parameter_name> <sql_type> [ ARRAY ]
```

##### return_table_type

Specifies the structure of the returned table data.

```sql
<return_table_type> ::= TABLE ( <ret_column_list> )
```

##### ret_column_list

Specifies the list of columns returned from the function.

```sql
<ret_column_list> ::= <ret_column_elem>[, <ret_column_elem> [,…] ]
```

##### ret_column_elem

Specifies the name of the column element with its associated data type.

```sql
<ret_column_elem> ::= <column_name> <sql_type>
<column_name> ::= <identifier>
```

#### LANGUAGE lang

Specifies the programming language used in the function.

```sql
LANGUAGE <lang>
<lang> ::= SQLSCRIPT
```

You can only use SQLScript functions.

#### mode

Specifies the security mode of the function.

```sql
<mode> ::= DEFINER | INVOKER
```

##### DEFINER

Executes the function with the privileges of the definer of the function. DEFINER is the default for table userdefined functions.

##### INVOKER

Executes the function with the privileges of the invoker of the function. Invoker is the default for scalar userdefined functions.

#### default_schema_name

##### minute_value

Specifies the result cache retention period.

```sql
<minute_value> ::= <unsigned_integer>
```

Only stale data access that does not exceed the specified RETENTION period is allowed. For outdated data that exceeds the RETENTION period, internally the result cache is refreshed and up-to-date data is returned.

Specifies the schema for unqualified objects in the function body.

```sql
<default_schema_name> ::= <identifier>
```

If `<default_schema_name>` is not specified, then the `<current_schema>` of the session is used.

#### DETERMINISTIC

DETERMINISTIC applies to scalar-functions. Signifies that the SQLScript function returns the same result any time it is called with the same input parameters.

#### cache_clause

Caches the result of a table function with an optional projection list and filter conditions.

Using a static result cache may result in stale data, and specifying a retention period ensures that data does not exceed the specified RETENTION period. Data that exceeds the retention period is refreshed and up-to-date data is returned.

```sql
<cache_clause> ::= WITH [ STATIC ] CACHE
   [ RETENTION <minute_value> ]
   [ OF <projection_list> ]
   [ FILTER <filter_condition> ]
   [ <location_clause> ]
```

##### minute_value

Specifies the result cache retention period.

```sql
<minute_value> ::= <unsigned_integer>
```

Only stale data access that does not exceed the specified RETENTION period is allowed. For outdated data that exceeds the RETENTION period, internally the result cache is refreshed and up-to-date data is returned.

##### projection_list

Specifies a result cached projection list to reduce the amount of cached data.

```sql
<projection_list> ::= <projection_name> [, <projection_name> [,...] ]
<projection_name> ::=  <column_name>
 | <aggr_type>(<column_name>)
<aggr_type> ::= { SUM | MIN | MAX | COUNT | AVG }
```

If a column that is not part of the projection list is requested or included in the WHERE clause, then the result cache cannot be exploited. In addition, you can direct an aggregation type of a specific column. If the column is specified, then the result cache includes aggregated results of that column and returns aggregated results only.

##### filter_condition

Specifies a filter condition to reduce the amount of cached data.

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

Only filtered results are cached. Predicates with subqueries are not supported. All forms of non-parameterized query filters are supported. For parameterized query filters, only conjunctive forms are supported.

##### location_clause

Specifies the location for the result cache entry.

```sql
<location_clause> ::= AT [LOCATION] '<hostname>:<port_number>'[, ...]
```

By default, when you execute a query on a static result cached view, the optimizer determines the result cache location. In some cases, the same result cache entry is created at multiple indexservers.

#### variable_cache_clause

Caches variable values during execution time so that they do not need to be re-resolved as the operations in `<statement_body>` are executed. Caching a variable removes the risk that its value will change each time it is resolved.

```sql
<variable_cache_clause> ::= VARIABLE CACHE ON
{ <variable_entry_with_mode_list> | <variable_entry_without_mode_list> }
<variable_entry_with_mode_list> ::= <variable_entry_with_mode>  [,
<variable_entry_with_mode> [,...] ]
<variable_entry_with_mode> ::= <variable_entry enable_mode>
<variable_entry> ::= { <variable_name> | <variable_name_clustered_list> }
<variable_name_clustered_list> ::= ( <variable_name> [, <variable_name>
[,...] ] )
<enable_mode> ::= { ENABLE | DISABLE }
<variable_entry_without_mode_list> ::= <variable_entry> [, <variable_entry>
[,...] ]
```

#### WITH ENCRYPTION

Encrypts the definition of the function. You cannot decrypt the definition later.

#### statement_body

Specifies the main body of the table functions and scalar functions.

```sql
<statement_body> ::=
 [ <func_using_list> ] [ <func_decl_list> ] [ <func_handler_list> ]
<func_stmt_list>
```

Since the function is flagged as read-only, neither DDL or DML statements (INSERT, UPDATE, and DELETE) are allowed in the function body. Scalar functions support table-typed input variables and table cell assignments. Other table operations are not supported.

For more information on `<func_using_list>`, `<func_decl_list>`, `<func_handler_list>`, and `<func_stmt_list>`, see the corresponding`<proc_using_list>`, `<proc_decl_list>`, `<proc_handler_list>`, and `<proc_stmt_list>` clause in the CREATE PROCEDURE Statement (Procedure).

## Description

The CREATE FUNCTION statement creates read-only functions that are free of side effects. Neither DDL or DML statements (INSERT, UPDATE, and DELETE) are allowed in the function body. Also, other functions or procedures selected/called from the body of the function must be read only.

There are two kinds of userdefined function (UDF): table and scalar. They differ by input/output parameter, supported functionality in the body, and the way that they are consumed in SQL statements.

Userdefined functions are read-only functions that are free of side effects: DDL or DML statements are not allowed within the function body.

When you specify HEADER ONLY, only the properties of the function are created along with the OID and no function dependencies exist. Once the headers are replaced with full function definitions, dependencies are created while the function OID remains the same. Dependencies appear in the OBJECT_DEPENDENCIES system view. HEADER ONLY is useful when you need to create dependent functions.

### Notes on CREATE OR REPLACE behavior:

- The behavior of CREATE OR REPLACE depends on the existence of a predefined function: If there is no existing function, then it behaves like CREATE FUNCTION; otherwise, it behaves like ALTER FUNCTION.
- You must explicitly set all parameters where the desired setting is different from the default (for example, settings for procedure language, default schema, whether the procedure is deterministic or encrypted, sequential execution options, and so on). Everything not specified in a CREATE OR REPLACE FUNCTION statement is reset to its default.
- You cannot use CREATE OR REPLACE FUNCTION to force a recompile of an existing function.
- If you specify the security mode or route options, then the behavior depends on the existence of a pre defined function: If there is no existing function, then the operation succeeds (the function is created). If the function exists and the security mode is different, then an error is returned.
- CREATE OR REPLACE does not change any DDL settings for the function, such as grant privileges, dependent objects, and so on.

See the SAP HANA SQLScript Reference guide for more information about creating and modifying userdefined functions.

## Examples

Create a table function called `Scale`.

```sql
CREATE FUNCTION Scale (val INT)
 RETURNS TABLE (a INT, b INT) LANGUAGE SQLSCRIPT AS
 BEGIN
     RETURN SELECT a, :val * b AS  b FROM mytab;
 END;
```

Use the `func_add_mul` function like a table. For example:

```sql
SELECT * FROM Scale(10);
SELECT * FROM Scale(10) AS a, Scale(10) AS b WHERE a.a =  b.a;
```

Create a scalar function called `func_add_mul`.

```sql
CREATE FUNCTION func_add_mul(x Double, y Double)
 RETURNS result_add Double, result_mul Double
 LANGUAGE SQLSCRIPT READS SQL DATA AS
 BEGIN
     result_add := :x + :y;
     result_mul := :x * :y;
 END;
```

Use the `func_add_mul` function like a built-in function. For example:

```sql
CREATE ROW TABLE TAB (a Double, b Double);
 INSERT INTO TAB VALUES (1.0, 2.0);
 INSERT INTO TAB VALUES (3.0, 4.0);

SELECT a, b, func_add_mul(a, b).result_add AS ADD, func_add_mul(a, b).result_mul
AS MUL FROM TAB ORDER BY a;
```

The SELECT statement returns the following results:

| **A** | **B** | **ADD** | **MUL** |
| --- | --- | --- | --- |
| 1 | 2 | 3 | 2 |
| 3 | 4 | 7 | 12 |

Create a function called `func_mul` that is assigned to a scalar variable in the `func_mul_wrapper` function.

```sql
CREATE FUNCTION func_mul(input1 INT)
 RETURNS output1 INT LANGUAGE SQLSCRIPT AS
 BEGIN
     output1 := :input1 * :input1;
 END;
CREATE FUNCTION func_mul_wrapper(input1 INT)
RETURNS output1 INT LANGUAGE SQLSCRIPT AS
BEGIN
    output1 := func_mul(:input1);
END;
SELECT func_mul_wrapper(2) as RESULT FROM DUMMY;
```

The SELECT statement returns 4.

Create a function called `FuncHeader` as HEADER ONLY. Later, you use ALTER FUNCTION to replace the header with the full function definitions.

```sql
CREATE FUNCTION FuncHeader (input1 integer) RETURNS  output1  integer AS HEADER
ONLY;
ALTER FUNCTION FuncHeader (input1 integer) RETURNS  output1  integer
AS
BEGIN
  output1 := :input1 * :input1;
END;
```

Create a table function called `FUNC` with a static result cache,

```sql
CREATE FUNCTION FUNC RETURNS TABLE (COL1 INT, COL2 INT) AS
BEGIN
    RETURN SELECT * FROM TAB;
END
WITH CACHE RETENTION 10;
```

## Related Information

CREATE FUNCTION Statement (Procedural) [→](CREATE-FUNCTION-Statement-Procedural.md) M_SQLSCRIPT_VARIABLE_CACHE System view [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md) CREATE TYPE Statement (Procedural) [→](CREATE-TYPE-Statement-Procedural.md) CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md) Expressions [→](../../4.06-Expressions.md) Predicates [→](../../4.07-Predicates/README.md) OBJECT_DEPENDENCIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/OBJECT_DEPENDENCIES-System-View.md) CREATE VIRTUAL FUNCTION Statement (Procedural) [→](CREATE-VIRTUAL-FUNCTION-Statement-Procedural.md)
