# 4.10.1.7 ALTER FUNCTION Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 431–436

Modifies a userdefined function.

## Syntax

```sql
ALTER FUNCTION <function_name>
 { [ ( <input_parameter_clause> ) ]
   [ RETURNS <return_type> ]
   [ LANGUAGE <lang> ]
   [ SQL SECURITY <mode> ]
   [ DEFAULT SCHEMA <default_schema_name> ]
   [ <variable_cache_clause> ]
   [ DETERMINISTIC ]
   [ WITH ENCRYPTION ]
   AS
     BEGIN
      <statement_body>
     END
 | ALTER FUNCTION <function_name> ENCRYPTION ON }
```

## Syntax Elements

#### function_name

Specifies the identifier of the function to be altered, with optional schema name.

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

#### WITH ENCRYPTION

Encrypts the definition of the function. You cannot decrypt the definition later.

#### variable_cache_clause

Modifies variable cache settings.

```sql
<variable_cache_clause> ::= {
   <add_variable_cache_option>
   | <alter_variable_cache_option>
   | <drop_variable_cache_option>
 }
```

##### add_variable_cache

Adds variable cache settings.

```sql
<add_variable_cache> ::= ADD VARIABLE CACHE ON
{ <variable_entry_with_mode_list> | <variable_entry_without_mode_list> }
<variable_entry_with_mode_list> ::= <variable_entry_with_mode>  [,
<variable_entry_with_mode> [,...] ]
<variable_entry_without_mode_list> ::= { <variable_name> |
<variable_list_clustered> }
<variable_entry_with_mode> ::= <variable_entry enable_mode>
<variable_entry> ::= { <variable_name> | <variable_name_clustered_list> }
<variable_name_clustered_list> ::= ( <variable_name> [, <variable_name>
[,...] ] )
<enable_mode> ::= { ENABLE | DISABLE }
```

##### alter_variable_cache

Alters variable cache settings.

```sql
<alter_variable_cache> ::= ALTER VARIABLE CACHE ON
<variable_entry_with_mode_list>
<variable_entry_with_mode_list> ::= <variable_entry_with_mode>  [,
<variable_entry_with_mode> [,...] ]
<variable_entry_with_mode> ::= <variable_entry> <enable_mode>
<variable_entry> ::= { <variable_name> | <variable_name_clustered_list> }
<variable_name_clustered_list> ::= ( <variable_name> [, <variable_name>
[,...] ] )
<enable_mode> ::= { ENABLE | DISABLE }
```

##### drop_variable_cache

Drops one or all variable cache settings.

```sql
<drop_variable_cache> ::= DROP VARIABLE CACHE { ON <variable_list> | ALL }<
variable_list> ::= <variable_name> [, <variable_name> [,...] ]
```

#### statement_body

Defines the main body of the function. See the CREATE FUNCTION statement for more information on what `<statement_body>` can contain. CREATE FUNCTION Statement (Procedural) [→](CREATE-FUNCTION-Statement-Procedural.md)

## Description

The RESULT CACHE stores query execution results on the table function to improve query performance when a query is subsequently executed on the same table. With this ALTER FUNCTION command, the result cache can be added to the table function.

Use ALTER FUNCTION `<function_name>` ENCRYPTION ON to encrypt the contents of a function without changing `<statement_body>`. You cannot undo this change.

See the SAP HANA SQLScript Reference guide for more information about creating and modifying userdefined functions.

## Examples

Create a table, Tab, and table function `function_a` that selects all records from table `Tab`.

```sql
CREATE ROW TABLE Tab (COL1 INT PRIMARY KEY, COL2 INT);
CREATE FUNCTION function_a RETURNS TABLE (COL1 INT, COL2 INT) AS
BEGIN
   RETURN SELECT * FROM Tab;
END;
```

Add a static result cache to the `function_a` function with a retention of 10:

```sql
ALTER FUNCTION function_a ADD STATIC CACHE RETENTION 10;
```

Change the retention value of the result cache of the `function_a` function to 20.

```sql
ALTER FUNCTION function_a ALTER CACHE RETENTION 20;
```

Restrict the cache entry location for `function_a` to the (fictitious) indexserver `lbsrv18:31576`.

```sql
ALTER FUNCTION function_a ALTER CACHE ADD AT LOCATION 'lbsrv18:31576';
```

Remove the location specifications so that there are no restrictions on the cache entry location for `function_a`.

```sql
ALTER FUNCTION function_a ALTER CACHE DROP AT LOCATION 'lbsrv18:31576';
```

Drop the result cache of table function `function_a`.

```sql
ALTER FUNCTION function_a DROP CACHE;
```

## Related Information

CREATE FUNCTION Statement (Procedural) [→](CREATE-FUNCTION-Statement-Procedural.md) M_SQLSCRIPT_VARIABLE_CACHE System view [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md) Predicates [→](../../4.07-Predicates/README.md) CREATE TYPE Statement (Procedural) [→](CREATE-TYPE-Statement-Procedural.md)
