# 4.10.1.11 ALTER PROCEDURE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 441–445

Alters a procedure or manually triggers a recompilation of a procedure by generating an updated execution plan.

## Syntax

```sql
ALTER PROCEDURE <proc_name>
 { [ ( <input_output_parameter_clause> ) ]
   [ LANGUAGE <lang> ]
   [ SQL SECURITY <mode> ]
   [ DEFAULT SCHEMA <default_schema_name> ]
   [ READS SQL DATA ]
 [ <variable_cache_clause> ]
   [ DETERMINISTIC ]
   [ WITH ENCRYPTION ]
   [ AUTOCOMMIT DDL { ON | OFF } }
    AS
     BEGIN  [ SEQUENTIAL EXECUTION ]
       <statement_body>
     END }
 | ALTER PROCEDURE <proc_name> RECOMPILE
 | ALTER PROCEDURE <proc_name> ENCRYPTION ON
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

#### DETERMINISTIC

DETERMINISTIC is for use with SQLScript procedures that produce scalar results. It specifies that the procedure returns the same result any time that it is called with the same input parameters.

#### READS SQL DATA

Specifies that the procedure is read only and sideeffect free. That is, the procedure does not make modifications to the database data or its structure, even if the procedure body contains dynamic SQL calls.

The advantage of using this parameter is that certain optimizations are available for read-only procedures.

#### WITH ENCRYPTION

Encrypts the procedure definition. See the SAP HANA SQLScript Guide for more information on this clause and the impact of encrypting a procedure.

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

Defines the main body of the procedure. See the CREATE PROCEDURE statement for more information on what `<statement_body>` can contain. CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md)

#### AUTOCOMMIT DDL { ON | OFF }

Specifies whether to automatically commit DDL statements in the procedure body. Specify ON when automatic commit of DDL statements is required; for example, during administrative operations such as importing data.

This clause is only supported for SQLScript procedures that are not read-only. The default value is OFF.

#### SEQUENTIAL EXECUTION

Forces sequential execution of the procedure logic. No parallelism takes place.

## Description

For the full description of the clauses for the ALTER PROCEDURE statement with respect to SQLScript procedures, including examples, refer to the CREATE PROCEDURE and ALTER PROCEDURE statements in the SAP HANA SQLScript Guide.

## Example

Trigger the recompilation of the `my_proc` procedure.

```sql
ALTER PROCEDURE my_proc RECOMPILE;
```

### Example - Using variable cache

Alters an SQLScript procedure to cache variable X:

```sql
CREATE TABLE test_cache (a INT);
INSERT INTO test_cache VALUES(5);
CREATE OR REPLACE PROCEDURE test_result_cache
LANGUAGE SQLSCRIPT AS
 BEGIN
  x = SELECT * FROM test_cache;
  SELECT * FROM :x;
 END;
ALTER PROCEDURE test_result_cache ADD VARIABLE CACHE ON X ENABLE;
```

## Related Information

CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md) M_SQLSCRIPT_VARIABLE_CACHE System view [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md) CREATE TYPE Statement (Procedural) [→](CREATE-TYPE-Statement-Procedural.md)
