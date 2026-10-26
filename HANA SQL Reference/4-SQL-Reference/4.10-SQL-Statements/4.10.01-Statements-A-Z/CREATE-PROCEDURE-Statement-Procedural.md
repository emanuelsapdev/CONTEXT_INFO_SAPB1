# 4.10.1.56 CREATE PROCEDURE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 733–751

Creates a procedure that uses the specified programming language.

## Syntax

```sql
CREATE [ OR REPLACE ] PROCEDURE <proc_name>
   [ (<input_output_parameter_clause>) ]
   [ LANGUAGE <lang> ]
   [ SQL SECURITY <mode> ]
   [ DEFAULT SCHEMA <default_schema_name> ]
   [ READS SQL DATA [ WITH RESULT VIEW <view_name> ] ]
   [ <variable_cache_clause> ]
   [ DETERMINISTIC ]
   [ WITH ENCRYPTION ]
   [ AUTOCOMMIT DDL { ON | OFF } ]
   AS
     { BEGIN [ SEQUENTIAL EXECUTION ]
        <statement_body>
       END
| HEADER ONLY }
```

## Syntax Elements

#### proc_name

The procedure name, with optional schema name.

```sql
<proc_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### input_output_parameter_clause

Specifies the input and output parameters for the procedure.

```sql
<input_output_parameter_clause> ::= <parameter> [,...]
<parameter> ::= [ IN | OUT | INOUT ] <param_name> <data_or_table_type>
<data_or_table_type> ::=
    <sql_type> [ DEFAULT <constant> ] [ ARRAY ]
    | <table_type>
    | <table_type_definition>
    | <any_table_type>
```

The default `<parameter>` is IN. Input and output parameters must be explicitly typed; un-typed tables are not supported.

The input and output parameters of a procedure can have any of the primitive SQL types or a table type. INOUT parameters can only be of scalar type.

##### sql_type [ DEFAULT constant ] [ ARRAY ]

Specifies the data type of the variable.

```sql
<sql_type> ::=
 DATE
 | TIME
 | SECONDDATE
 | TIMESTAMP
 | TINYINT
 | SMALLINT
 | INTEGER
 | BIGINT
 | SMALLDECIMAL
 | REAL
 | DOUBLE
 | BINTEXT
 | VARCHAR [ (<unsigned_integer>) ]
 | NVARCHAR [ (<unsigned_integer>) ]
 | ALPHANUM [ (<unsigned_integer>) ]
 | VARBINARY [ (<unsigned_integer>) ]
 | DECIMAL [ (<unsigned_integer> [, <unsigned_integer> ]) ]
```

Only for use with IN parameters; use the optional DEFAULT option when you want to specify a default and a constant is correct for the data type. For example, you cannot specify a constant as a default for an ARRAY.

Use the optional ARRAY option when the parameter is an array.

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
<column_list_definition> ::= <column_elem>[,...]
<column_elem> ::= <column_name> <data_type>
<column_name> ::= <identifier>
```

##### any_table_type

Defines the table type at DDL time or query compilation time.

```sql
<any_table_type> ::= TABLE(...)
```

The syntax of `<any_table_type>` requires you to explicitly specify **TABLE(…)** (for example, `CREATE PROCEDURE anyproc_in (IN itab TABLE(...), outtab TABLE(...) ) AS BEGIN…`).

#### LANGUAGE

Specifies the programming language that is used in the procedure.

```sql
LANGUAGE <lang>
<lang> ::= { SQLSCRIPT | R | GRAPH }
```

The default is SQLSCRIPT. Define the language in all procedure definitions.

Specify GRAPH to use graph script, a domainspecific programming language for custom graph algorithms and analytics.

#### mode

Specifies the security mode for the procedure.

```sql
<mode> ::= { DEFINER | INVOKER }
```

The default is DEFINER.

##### DEFINER

Specifies that the procedure is executed with the privileges of the user who defined the procedure.

##### INVOKER

Specifies that the procedure is executed with the privileges of the user who invoked the procedure.

#### DEFAULT SCHEMA

Specifies the schema for unqualified objects in the procedure body.

```sql
DEFAULT SCHEMA <default_schema_name>
<default_schema_name> ::= <identifier>
```

If nothing is specified, then the current_schema of the session is used.

#### READS SQL DATA

Specifies that the procedure is read only and sideeffect free. That is, the procedure does not make modifications to the database data or its structure, even if the procedure body contains dynamic SQL calls.

The advantage of using this parameter is that certain optimizations are available for read-only procedures.

#### WITH RESULT VIEW

Specifies the result view to use as the output of a read-only procedure.

```sql
WITH RESULT VIEW <view_name>
<view_name> ::= <identifier>
```

When a result view is defined for a procedure, it can be called by an SQL statement in the same way as a table or view. See Example 2 - Using a result view [→](CREATE-PROCEDURE-Statement-Procedural.md).

#### SEQUENTIAL EXECUTION

Forces sequential execution of the procedure logic. No parallelism takes place.

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

#### DETERMINISTIC

DETERMINISTIC is for use with SQLScript procedures that produce scalar results. It specifies that the procedure returns the same result any time that it is called with the same input parameters.

#### WITH ENCRYPTION

Encrypts the procedure definition. See the SAP HANA SQLScript Guide for more information on this clause and the impact of encrypting a procedure.

#### AUTOCOMMIT DDL { ON | OFF }

Specifies whether to automatically commit DDL statements in the procedure body. Specify ON when automatic commit of DDL statements is required; for example, during administrative operations such as importing data.

This clause is only supported for SQLScript procedures that are not read-only. The default value is OFF.

#### statement_body

```sql
<statement_body> ::=
 [ <proc_using_list> ] [ <proc_decl_list> ] [ <proc_handler_list> ]
<proc_stmt_list>
```

Defines the main body of the procedure according to the specified programming language.

##### proc_using_list

Defines the libraries to use.

```sql
<proc_using_list> ::= <proc_using> [ ... ]
<proc_using> ::= USING <library_name> AS <library_alias>;
<library_name> ::= [ <schema_name>.]<identifier>
<library_alias> ::= <identifier>
```

##### proc_decl_list

Defines the declarations for the procedure.

```sql
<proc_decl_list> ::= <proc_declaration> [ <proc_declaration> [...]]
<proc_declaration> ::=
DECLARE {
 <proc_variable>
 | <proc_table_variable>
 | <proc_row_variable>
 | <proc_cursor>
 | <proc_condition> };
```

##### proc_variable

Defines variables for the procedure.

```sql
<proc_variable>::=
 <variable_name_list> [ CONSTANT ] { <sql_type> | <array_datatype> |
AUTO } [ NOT NULL ] [ <default_value> ]

<variable_name_list> ::= <variable_name>[, <variable_name> [,…] ]
 <array_datatype> ::= ARRAY [ := <array_constructor> ]
 <array_constructor> ::= ARRAY (<expression> [, <expression> [,...] )
 <default_value> ::= { DEFAULT | := | = } { <value> | <expression> }
 <value> ::= A value of the type specified by <sql_type> or an expression
```

When you specify AUTO, you must also specify `<default_value>`.

##### proc_table_variable

Defines table variables for the procedure.

```sql
<proc_table_variable> ::= <proc_table_var_def> [ <sort_def> ]
<proc_table_var_def>
 <variable_name_list> <table_type_definition>
 | <table_type>
 | <variable_name_list> [ CONSTANT ] LIKE { <table_name>
 | <table_variable_name>.<column_name> [ AUTO ] [ NOT NULL ]
[ <default_value> ]
 | <variable_name_list> [ CONSTANT ] TABLE LIKE { <table_name>
| :<table_variable_name> } [ AUTO ] [ <default_value> ]
<sort_def> ::= SEARCH KEY ( <col_name> [, <col_name> [,…] ]
```

When you specify AUTO, you must also specify `<default_value>`.

`<sort_def>` is used in SQLScript procedures to sort the table variables. See the SAP HANA SQLScript Guide for more information on sorted table variables.

##### proc_row_variable

Defines row variables for the procedure.

```sql
<proc_row_variable> ::=
<variable_name_list> ROW <row_definition>
 | <variable_name_list> ROW LIKE { <persistent_table_name>
| :<other_table_row_or_cursor_variable_name>
```

##### proc_cursor

Defines the procedure cursors.

```sql
<proc_cursor> ::=
 CURSOR <cursor_name> [ ( <proc_cursor_param_list> ) ] FOR <subquery>;
<proc_cursor_param_list> ::= <proc_cursor_param> [,...]
<variable_name> ::= <identifier>
<cursor_name> ::= <identifier>
<proc_cursor_param> ::= <param_name> <datatype>
```

##### proc_condition

Defines variable conditions.

```sql
<proc_condition> ::=
 <variable_name> CONDITION
 | <variable_name> CONDITION FOR <sql_error_code>
```

##### proc_handler_list

Declares exception handlers to catch SQL exceptions.

```sql
<proc_handler_list> ::= <proc_handler> [, <proc_handler> [,…] ]
<proc_handler> ::= DECLARE { EXIT | CONTINUE } HANDLER FOR
<proc_condition_value_list> <proc_stmt>;
```

##### proc_condition_value_list

Specifies one or more condition values.

```sql
<proc_condition_value_list> ::=
 <proc_condition_value> [, <proc_condition_value> [,...] ]
```

##### proc_condition_value

Specifies a specific error code number or condition name declared on a condition variable.

```sql
<proc_condition_value> ::=
 SQLEXCEPTION
 | SQLWARNING
 | <sql_error_code>
 | <condition_name>
```

##### proc_stmt_list

Specifies statements for the procedure body.

```sql
<proc_stmt_list> ::= <proc_stmt> [ <proc_stmt> [...] ]
<proc_stmt> ::=
 <proc_block>
 | <proc_assign>
 | <proc_tabvar_search>
 | <proc_single_assign>
 | <proc_multi_assign>
 | <proc_if>
 | <proc_loop>
 | <proc_while>
 | <proc_for>
 | <proc_foreach>
 | <proc_exit>
| <proc_continue>
| <proc_signal>
| <proc_resignal>
| <proc_sql>
| <proc_open>
| <proc_fetch>
| <proc_close>
| <proc_call>
| <proc_exec>
| <proc_return>
| <proc_insert>
| <proc_update>
| <proc_delete>
```

##### proc_block

Nests a section of the procedure by using the BEGIN and END keywords.

```sql
<proc_block> ::=
 BEGIN <proc_block_option>
   [ <proc_decl_list> ]
   [ <proc_handler_list> ]
   <proc_stmt_list>
 END;
```

```sql
<proc_block_option> ::=
 [ SEQUENTIAL EXECUTION ] [ AUTONOMOUS TRANSACTION ]
 | [ AUTONOMOUS TRANSACTION ] [ SEQUENTIAL EXECUTION ]
```

The autonomous transaction is independent from the main procedure. Changes made and committed by an autonomous transaction can persist regardless of whether the main procedure transaction is committed or rolled back. The end of the autonomous transaction block has an implicit commit.

##### proc_assign

Assigns values to variables.

```sql
<proc_assign> ::=
 <variable_name> := { <expression> | <array_function> };
 | <variable_name> '[' <expression> ']' := <expression>;
```

`<expression>` is either a simple expression such as a character, a date, or a number, or it can be a scalar function.

##### proc_tabvar_search

Searches for key value pairs in a table variable.

The position of the first matching record is returned, or NULL if no record matches. This result can be used in conjunction with other table variable operators (DELETE, UPDATE).

```sql
<proc_tabvar_search> ::=
POS = <table_variable>.SEARCH( ( <column_list> ), ( <value_list> ) [,
<start_position> ] )
<column_list> ::= <column1> [, <column2> [,..] ]
<value_list> ::= <value1> [, <value2> [,..] ]
<start_position> ::= <expression>
```

POS= is part of the required syntax. For example, specify `POS=:myTabVar.SEARCH(("key1", "key2"), ("I", 3));` to search for values "I" and 3 in columns key1 and key2, respectively, of the myTabVar table variable.

###### table_variable

Specifies the table variable to search.

###### column_list and value_list

Specifies the values to search for in the columns. The SAP HANA server pairs the columns listed with the values listed, thus forming the key-value pairs to search for. The number of items in `<column_list>` must be the same as the number of items in `<value_list>`. A column can be listed more than once in `<column_list>`, just as a value can be listed more than once in `<value_list>`.

###### start_position

Specifies the row to start with. The default value is 1, which specifies to scan all data starting at the beginning row. `<expression>` can be any valid expression that resolves to a positive integer.

##### array_function

Specifies an array function.

```sql
<array_function> ::=
 ARRAY_AGG ( <table_variable>.<column_name> [ ORDER BY <sort_spec_list> ] )
 | CARDINALITY ( <array_variable_name> )
 | TRIM_ARRAY  ( <array_variable_name>,<array_variable_name>)
 | ARRAY ( <array_variable_name_list> )
<table_variable> ::= <identifier>
<column_name> ::= <identifier>
<array_variable_name> ::= <identifier>
```

The ARRAY_AGG function returns the array by aggregating the set of elements in the specified column of the table variable. Ordering the elements is optional.

The CARDINALITY function returns the number for the element in the array `<array_variable_name>`.

The TRIM_ARRAY function returns the new array by removing the given number of elements, `<numeric_value_expression>`, from the end of the array, `<array_value_expression>`.

The ARRAY function returns an array whose elements are specified in the list `<array_variable_name>`. For more information, see SAP HANA SQLScript Reference.

##### proc_single_assign

Assigns values to a list of variables with only one function evaluation.

```sql
<proc_single_assign> ::=
 <variable_name> = <subquery>
 |  <variable_name> = <proc_ce_call>
 |  <variable_name> = <proc_apply_filter>
 |  <variable_name> = <unnest_function>
 |  <variable_name> = <match_merge_op>
```

##### proc_multi_assign

Assigns values to a list of variables with multiple function evaluations.

```sql
<proc_multi_assign> ::= ( <variable_name_list> ) := <function_expression>
```

`<function_expression>` is a scalar userdefined function and the number of elements in `<variable_name_list>` equal the number of output parameters of the scalar userdefined function.

##### proc_ce_call

Defines the calculation engine plan operators for the procedure.

Use SQL rather than calculation engine plan operators with SQLScript.

| Overview: Mapping between CE_\* Operators and SQL **CE Operator** | **CE Syntax** | **SQL Equivalent** |
| --- | --- | --- |
| `CE_COLUMN_TABLE` | `CE_COLUMN_TABLE(<table_name>[,<attributes>])` | `SELECT [<attributes>]FROM <table_name>` |
| `CE_JOIN_VIEW` | `CE_JOIN_VIEW(<column_view_name>[,<attributes>]) out = CE_JOIN_VIEW("PRODUCT_SA LES", ["PRODUCT_KEY", "PRODUCT_TEXT", "SALES"]);` | `SELECT [<attributes>]FROM <column_view_name> out = SELECT product_key, product_text, sales FROM product_sales;` |
| `CE_OLAP_VIEW` | `CE_OLAP_VIEW (<olap_view_name>[,<attributes>]) out = CE_OLAP_VIEW("OLAP_view" , ["DIM1", SUM("KF")]);` | `SELECT [<attributes>]FROM <olap_view_name> out = select dim1, SUM(kf) FROM OLAP_view GROUP BY dim1;` |
| `CE_CALC_VIEW` | `CE_CALC_VIEW(<calc_view_name>,[<attributes>]) out = CE_CALC_VIEW("TESTCECTAB LE", ["CID", "CNAME"]);` | `SELECT [<attributes>]FROM <calc_view_name> out = SELECT cid, cname FROM "TESTCECTABLE";` |
| `CE_JOIN` | `CE_JOIN(<left_table>,<right_table>,<join_attributes>[<projection_list>]) ot_pubs_books1 = CE_JOIN (:lt_pubs, :it_books, ["PUBLISHER"]);` | `SELECT [<projection_list>] FROM <left_table>,<right_table> WHERE <join_attributes> ot_pubs_books1 = SELECT P.publisher AS publisher, name, street,post_code, city, country, isbn, title, edition, year, price, crcy FROM :lt_pubs AS P, :it_books AS B WHERE P.publisher = B.publisher;` |

| **CE Operator** | **CE Syntax** | **SQL Equivalent** |
| --- | --- | --- |
| `CE_LEFT_OUTER_JOIN` | `CE_LEFT_OUTER_JOIN(<left_table>,<right_table>,<join_attributes>[<projection_list>])` | `SELECT [<projection_list>] FROM <left_table> LEFT OUTER JOIN <right_table> ON <join_attributes>` |
| `CE_RIGHT_OUTER_JOIN` | `CE_RIGHT_OUTER_JOIN(<left_table>,<right_table>,<join_attributes>[<projection_list>])` | `SELECT [<projection_list>] FROM <left_table> RIGHT OUTER JOIN <right_table> ON <join_attributes>` |
| `CE_PROJECTION` | `CE_PROJECTION(<table_variable>,<projection_list >[,<filter>]) ot_books1 = CE_PROJECTION (:it_books, ["TITLE","PRICE", "CRCY" AS "CURRENCY"], '"PRICE" > 50');` | `SELECT <projection_list>FROM <table_variable>where [<filter>] ot_book2= SELECT title, price, crcy AS currency FROM :it_b ooks WHERE price > 50;` |
| `CE_UNION_ALL` | `CE_UNION_ALL(<table_variable1>,<table_variable2>) ot_all_books1 = CE_UNION_ALL (:lt_books, :it_audioboo ks);` | `SELECT * FROM <table_variable1> UNION ALL SELECT * FROM <table_variable2> ot_all_books2 = SELECT * FROM :lt_books UNION ALL SELECT * FROM :it_audiobooks;` |
| `CE_CONVERSION` | `CE_CONVERSION(<table_variable>,<conversion_params>,[<rename_clause>])` | `SQL-FunctionCONVERT_CURRENCY` |
| `CE_AGGREGATION` | `CE_AGGREGATION(<table_variable>,<aggregate_list>[,<group_columns>]) ot_books1 = CE_AGGREGATION (:it_books, [COUNT ("PUBLISHER") AS "CNT"], ["YEAR"]);` | `SELECT <aggregate_list>FROM <table_variable>[GROUP BY <group_columns>] ot_books2 = SELECT COUNT (publisher) AS cnt, year FROM :it_books GROUP BY year;` |
| `CE_CALC` | `CE_CALC(‘<expr>’, <result_type>) TEMP = CE_PROJECTION(:table_var , ["ID" AS "KEY", CE_CALC('rownum()', INTEGER) AS "T_ID"] );` | SQL Function<br> `TEMP = SELECT "ID" AS "KEY", ROW_NUMBER() OVER () AS "T_ID" FROM :table_var` |
| `CE_VERTICAL_UNION` | `CE_VERTICAL_UNION(<table_variable>, <projection_list>[ { ,<table_variable >, <projection_list >}...] )` | `unnest ( <table_variable> [ {, <table_variable> } …] ) as ( (<projection_list>) [ {, ( <projection_list> ) } … ] )` |

For more information about calculation engine plan operators, see SAP HANA SQLScript Reference.

##### proc_apply_filter

Defines a dynamic WHERE condition that is applied at runtime.

```sql
<proc_apply_filter> ::=
 APPLY_FILTER ( {<table_name> | <table_variable>}, <variable_name> );
```

For more information about APPLY_FILTER, see SAP HANA SQLScript Reference.

##### unnest_function

Returns a table, including a row for each element of the specified array.

```sql
<unnest_function> ::=
 UNNEST ( <variable_name_list> ) [ WITH ORDINALITY ] [ <as_col_names> ];
<variable_name_list> ::= <variable_name> [, <variable_name> [,...] ]
```

###### WITH ORDINALITY

Appends an ordinal column to the return values.

###### as_col_names

Specifies the column names of the return table.

```sql
<as_col_names> ::= AS [ <table_name> ] ( <column_name_list> )
<column_name_list> ::= <column_name> [, <column_name> [,...] ]
<column_name> ::= <identifier>
```

##### map_merge_op

Applies each row of the input table to the mapper function and unites all intermediate result tables. For more information about the MAP_MERGE operator, see the SAP HANA SQLScript Reference.

```sql
<map_merge_op> ::=
MAP_MERGE ( <table_or_table_variable>, <mapper_identifier>
( <table_or_table_variable>.<column_name> [,...] [, <param_list> ])
<table_or_table_variable> ::= <table_variable_name> | <identifier>
<table_variable_name> ::= <identifier>
<mapper_identifier> ::= <identifier>
<column_name> ::= <identifier>
<param_list> ::= <param> [,...]
<param> ::=
 <table_or_table_variable>
 | <string_literal>
 | <numeric_literal>
 | <identifier>
```

##### proc_if

Controls the execution flow with conditionals.

```sql
<proc_if> ::=
 IF <condition> THEN [ SEQUENTIAL EXECUTION ]
    [ <proc_decl_list> ]
    [ <proc_handler_list> ]
    <proc_stmt_list>
    [ <proc_elsif_list> ]
    [ <proc_else> ]
 END IF;
<proc_elsif_list> ::=
 ELSEIF <proc_decl_list> ] [ <proc_handler_list> ] <proc_stmt_list>
<proc_else> ::=
 ELSE [ SEQUENTIAL EXECUTION ] [ <proc_decl_list> ]
[ <proc_handler_list> ] <proc_stmt_list>
```

###### proc_loop

Uses a loop to repeatedly execute a set of statements.

```sql
<proc_loop> ::=
 LOOP [ SEQUENTIAL EXECUTION ]
    [ <proc_decl_list> ]
    [ <proc_handler_list> ]
    <proc_stmt_list>
 END LOOP;
```

###### proc_while

Specifies that a set of trigger statements is repeatedly called while a condition is true.

```sql
<proc_while> ::=
 WHILE <condition> DO [ SEQUENTIAL EXECUTION ]
    [ <proc_decl_list> ]
    [ <proc_handler_list> ]
    <proc_stmt_list>
 END WHILE;
```

###### proc_for

Specifies a FOR...IN loop that iterates over a set of data.

```sql
<proc_for> ::=
 FOR <column_name> IN [ REVERSE ] <expression> [...]  <expression>
   DO [ SEQUENTIAL EXECUTION ]
     [ <proc_decl_list> ]
     [ <proc_handler_list> ]
     <proc_stmt_list>
 END FOR;
```

###### proc_foreach

Specifies a FOR...EACH loops that iterates over all elements in a set of data.

```sql
<proc_foreach> ::=
 FOR <column_name> AS <column_name> [ <open_param_list> ]
   DO [ SEQUENTIAL EXECUTION ]
     [ <proc_decl_list> ]
     [ <proc_handler_list> ]
     <proc_stmt_list>
 END FOR;
<open_param_list> ::= ( <expression> [, <expression> [,...] )
```

###### proc_exit

Terminates a loop.

```sql
<proc_exit> ::= BREAK;
```

###### proc_continue

Skips a current loop iteration and continues with the next value.

```sql
<proc_continue> ::= CONTINUE;
```

###### proc_signal

Explicitly raises an exception from within your trigger procedures.

```sql
<proc_signal> ::=
 SIGNAL <signal_value> [ <set_signal_info> ];
```

###### proc_resignal

Raises an exception on the action statement in an exception handler.

```sql
<proc_resignal> ::=
 RESIGNAL [ <signal_value> ] [ <set_signal_info> ];
```

If an error code is not specified, then RESIGNAL throws the caught exception.

###### signal_value

Specifies a SIGNAL or RESIGNAL for a signal name or an SQL error code.

```sql
<signal_value> ::= <signal_name> | <sql_error_code>
<signal_name> ::= <identifier>
<sql_error_code> ::= <unsigned_integer>
```

###### set_signal_info

Specifies that an error message is delivered to users when a specified error is thrown during procedure execution.

```sql
<set_signal_info> ::= SET MESSAGE_TEXT = '<message_string>'
<message_string> ::= <any_character>
```

###### proc_sql

Specifies an SQL statement.

```sql
<proc_sql> ::=
<subquery>
| <select_into_stmt>
| <select_from_embedded_function_stmt>
| <insert_stmt>
| <delete_stmt>
| <update_stmt>
| <replace_stmt>
| <call_stmt>
| <create_table_stmt>
| <drop_table_stmt>
```

`<select_from_embedded_function_stmt>` and `<select_into_stmt>` are for use exclusively in a SQLScript procedure body context. For all other SQL statements in `<proc_sql>`, refer to the topic for that specific statement found in this guide. For example, for more information on `<insert_stmt>`, see the INSERT Statement topic in this guide.

###### select_from_embedded_function_stmt

Selects from an embedded function.

```sql
<select_from_embedded_function> ::=
SELECT <select_list> FROM SQL FUNCTION <embedded_func_returns> BEGIN
<sqlscript_body> END
<embedded_func_returns> = RETURNS { <table_ref> |
( <opt_cv_array_column_list> ) | <proc_param_name> <func_data_type> }
```

Any query with SQL FUNCTION in the body is not cached in SQL plan cache.

Queries with SQL FUNCTION can be used in SELECT or DML statements, not inside a DDL definition, and not inside a DO BEGIN...END or another SQL FUNCTION block.

For examples of how to use embedded SQL functions in the body of a SQLScript procedure, see the SAP HANA SQLScript reference guide.

###### select_into_stmt

Specifies a query.

```sql
<select_into_stmt> ::= SELECT <select_list> INTO
<variable_name_list> [ DEFAULT <scalar_expr_list> ]
 <from_clause>
 [ <where_clause> ]
 [ <group_by_clause> ]
 [ <having_clause> ]
 [ {<set_operator> <subquery>, ... } ]
 [ <order_by_clause> ]
 [ <limit> ];
```

For information on `<select_list>`, `<from_clause>`, `<where_clause>`, `<group_by_clause>`, `<having_clause>`, `<set_operator>`, `<subquery>`, `<order_by_clause>`, and `<limit>`, see the SELECT statement.

###### variable_name_list

Specifies a variable list.

```sql
<variable_name_list> ::= <variable_name>[{, <variable_name>}...]
<variable_name> ::= <identifier>
```

`<variable_name>` is a scalar variable. You can assign a selected item value to this scalar variable.

###### proc_open

Controls cursor operations.

```sql
<proc_open> ::=
 OPEN <cursor_name> [ <open_param_list> ];
<proc_fetch> ::=
 FETCH <cursor_name> INTO <column_name_list>;
<proc_close> ::= CLOSE <cursor_name>;
```

###### proc_call

Calls a procedure using the CALL statement. See CALL Statement (Procedural) [→](CALL-Statement-Procedural.md).

###### proc_exec

Makes a dynamic SQL call.

```sql
<proc_exec> ::=
 EXEC '<sql-statement>' [ INTO <variable_name_list> [ DEFAULT
<scalar_expr_list> ] ] [ USING <expression_list> ] [ READS SQL DATA ];
 | EXECUTE IMMEDIATE '<sql-statement>' [ INTO <variable_name_list>
[ DEFAULT <scalar_expr_list> ] ] [ USING <expression_list> ] [ READS
SQL DATA ];
<variable_name_list> ::= <variable_name>[,...]
<variable_name> ::= <identifier>
<expression_list> ::= <expression>[,...]
```

EXEC executes `<sql-statement>` passed as a string argument. EXEC does not return a result set if `<sql-statement>` is a SELECT statement. Use EXECUTE IMMEDIATE for that purpose. If the query returns result sets or output parameters, then you can assign the values to scalar or table variables with the INTO clause.

When `<sql-statement>` is a SELECT statement and table variables are listed in the INTO clause, result sets are assigned to the table variables sequentially. If scalar variables are listed in the INTO clause for a SELECT statement, then it works like `<select_into_stmt>` and assigns the value of each column of the first row to a scalar variable when a single row is returned from a single result set. When the SQL statement is a CALL statement, output parameters represented as ':`<variable_name>`' in the SQL statement are assigned to the variables in the INTO clause according to the variable name.

If `<sql-statement>` returns a single row, then you can assign the value of each column to a scalar variable by specifying the INTO `<variable_name_list>` clause.

Bind scalar values by specifying the USING `<expression_list>` clause. `<expression>` can be either a simple expression, such as a character, a date, or a number, or it can be a scalar variable.

READS SQL DATA specifies that the dynamic SQL call is read only and will not make modifications to the database data or its structure.

###### proc_return

Returns a value from a procedure.

```sql
<proc_return> ::= RETURN [ <proc_expr> ];
```

For more information about SQLScript, see SAP HANA SQLScript Reference.

For more information about the R-Language, see the SAP HANA R Integration Guide.

###### proc_insert

Inserts a new data record into a table variable at a specific position.

```sql
<proc_insert> ::= :<table_variable>.INSERT((<value>[,…] ), <index>)
```

All existing data records at the positions starting from the given index are moved to the next position. If the index is greater than the original table size, then the records between the inserted record and the original last record are initialized with NULL values.

###### proc_update

Updates a data record at a specific position in a table variable. There are two syntaxes for `<proc_update>`:

```sql
<proc_update> ::= :<table_variable>.UPDATE((<value>[,…] ), <index>))
<proc_update> ::= :<table_variable>[ <index> ] = (<value>[,…])
```

If `<index>` is greater than the table size, then no operation is performed.

###### proc_delete

Deletes a data record at a specific position in a table variable.

```sql
<proc_delete> ::= :<table_variable>.DELETE(<index>)
```

If `<index>` is greater than the table size, then no operation is performed.

#### HEADER ONLY

Specifies that only the properties of the procedure are created along with the OID and no procedure dependencies exist.

Once the headers are replaced with full procedure definitions, dependencies are created while the procedure OID remains the same. Dependencies appear in the OBJECT_DEPENDENCIES system view. HEADER ONLY is useful when several dependent procedures must be created.

## Description

The CREATE PROCEDURE statement creates a procedure using the specified programming language `<lang>`.

For more information about SQLScript, see SAP HANA SQLScript Reference.

For more information about the R-Language, see the SAP HANA R Integration Guide.

### CREATE OR REPLACE behavior:

- The behavior of CREATE OR REPLACE depends on the existence of a predefined procedure: If there is no existing procedure, then it behaves like CREATE PROCEDURE; otherwise, it behaves like ALTER PROCEDURE.
- Explicitly set all parameters where the desired setting is different from the default (for example, settings for the procedure language, the default schema, whether the procedure is deterministic or encrypted, sequential execution options, and so on). Everything not specified in a CREATE OR REPLACE PROCEDURE statement is reset to its default.
- You cannot use CREATE OR REPLACE PROCEDURE to change the route options or force a recompile of an existing procedure.
- If you specify the security mode or route options, then the behavior depends on the existence of a pre defined procedure: If there is no existing procedure, then the operation succeeds (the procedure is created). If the procedure exists, and the security mode or route option is different, then an error is returned.
- CREATE OR REPLACE does not change any DDL settings for the procedure, such as grant privileges, dependent objects, and so on.

## Examples

### Example - Creating an SQL Script Procedure

Create an SQLScript procedure with the following definition.

```sql
CREATE PROCEDURE orchestrationProc
 LANGUAGE SQLSCRIPT AS
 BEGIN
   DECLARE v_id BIGINT;
   DECLARE v_name VARCHAR(30);
   DECLARE  v_pmnt BIGINT;
   DECLARE v_msg VARCHAR(200);
   DECLARE CURSOR c_cursor1 (p_payment BIGINT) FOR
     SELECT id, name, payment FROM control_tab
       WHERE payment > :p_payment ORDER BY id ASC;
   CALL init_proc();
   OPEN c_cursor1(250000);
   FETCH c_cursor1 INTO v_id, v_name, v_pmnt; v_msg := :v_name || ' (id '
|| :v_id || ') earns ' || :v_pmnt || ' $.';
   CALL ins_msg_proc(:v_msg);
   CLOSE c_cursor1;
 END;
```

The procedure features a number of imperative constructs, including the use of a cursor (with associated state) and local scalar variables with assignments.

### Example - Using a result view

The following example creates an SQLScript procedure that uses a result view ProcView to return its results.

```sql
CREATE PROCEDURE ProcWithResultView(IN id INT, OUT o1 CUSTOMER)
 LANGUAGE SQLSCRIPT
 READS SQL DATA WITH RESULT VIEW ProcView AS
 BEGIN
   o1 = SELECT * FROM CUSTOMER WHERE CUST_ID = :id;
 END;
```

You call this procedure from an SQL statement as follows.

```sql
SELECT * FROM ProcView (PLACEHOLDER."id"=>'5');
```

Procedures and result views produced by procedures are not connected from the security perspective and therefore do not inherit privileges from each other. The security aspects of each object must be handled separately. For example, you must grant the SELECT privilege on a result view and EXECUTE privilege on a connected procedure.

Create the procedure ProcHeader as HEADER only. Later, you use ALTER PROCEDURE to replace the header with the full procedure definitions.

```sql
CREATE PROCEDURE ProcHeader (IN id INTEGER) AS HEADER ONLY;
ALTER PROCEDURE ProcHeader (IN id INTEGER)
AS
  BEGIN
    o1 = SELECT * FROM CUSTOMER WHERE CUST_ID = :id;
  END;
```

### Example - Using variable cache

The following example creates an SQLScript procedure that caches variable X:

```sql
CREATE TABLE test_cache (a INT);
INSERT INTO test_cache VALUES(5);
CREATE OR REPLACE PROCEDURE test_result_cache
LANGUAGE SQLSCRIPT
VARIABLE CACHE ON X ENABLE AS
 BEGIN
  x = SELECT * FROM test_cache;
  SELECT * FROM :x;
 END;
```

**Example - Use of READS SQL DATA with dynamic SQL -** The following examples show how to set dynamic SQL in the body of a procedure to read-only:

```sql
CREATE PROCEDURE Proc1() READS SQL DATA AS
  BEGIN
      EXEC 'SELECT * FROM DUMMY';
  END;

 CREATE PROCEDURE Proc1(IN A NVARCHAR(12)) AS
  BEGIN
      EXECUTE IMMEDIATE 'SELECT * FROM ' || :A READS SQL DATA;
 END;
```

## Related Information

ALTER PROCEDURE Statement (Procedural) [→](ALTER-PROCEDURE-Statement-Procedural.md) CREATE LIBRARY Statement (SQLScript) [→](CREATE-LIBRARY-Statement-SQLScript.md) OBJECT_DEPENDENCIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/OBJECT_DEPENDENCIES-System-View.md) M_SQLSCRIPT_VARIABLE_CACHE System view [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md)
