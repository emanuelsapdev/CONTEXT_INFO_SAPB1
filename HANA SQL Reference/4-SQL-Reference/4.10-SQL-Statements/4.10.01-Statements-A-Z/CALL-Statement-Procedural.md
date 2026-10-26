# 4.10.1.39 CALL Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 678–680

Calls a procedure.

## Syntax

```sql
CALL <proc_name> ( <param_list> ) [ WITH OVERVIEW]
 | CALL <sqlscript_lib_member> ( <param_list> )
```

## Syntax Elements

#### proc_name

Specifies the procedure to be called.

```sql
<proc_name> ::= [ <schema_name>.]<identifier>
```

Optionally, specify a schema name for the identifier.

#### param_list

Specifies the procedure parameters.

```sql
<param_list> ::= <proc_param>[,...]
```

##### proc_param

Specifies procedure parameters.

```sql
<proc_param> ::=
 <identifier>
 | <string_literal>
 | <unsigned_integer>
 | <signed_integer>
 | <signed_numeric_literal>
 | <unsigned_numeric_literal>
 | <expressions>
```

Parameters passed to a procedure are scalar constants and can be passed either as IN, OUT, or INOUT parameters. Scalar parameters are assumed to be NOT NULL. Arguments for IN parameters of table type can either be physical tables or views. The actual value passed for tabular OUT parameters must be ?.

#### WITH OVERVIEW

Defines that the result of a procedure call is stored directly into a physical table.

Calling a procedure WITH OVERVIEW returns one result set that contains the information about which table contains the result of which table output variable'. Scalar outputs are returned as regular scalar output parameters. When you pass existing tables to the output parameters, WITH OVERVIEW inserts the result set tuples of the procedure into the provided tables. When you pass NULL to the output parameters, temporary tables holding the result sets are generated. These tables are dropped automatically once the database session is closed.

#### sqlscript_lib_member

Calls a SQLScript library member procedure.

```sql
<lib_member_ref> ::= [ <schema_name>.]<library_name_or_alias>:<member_name>

<schema_name> ::= <identifier>
<library_name_or_alias> ::= <identifier>
<member_name> ::= <identifier>
```

When calling a SQLScript library member procedure, the WITH option is not supported. Also, there is no EXPLAIN PLAN or QUERY EXPORT support when calling a SQLScript library member procedure.

For more information about SQLScript userdefined libraries, see the SAP HANA SQLScript Reference Guide.

## Description

Calls a procedure defined using the CREATE PROCEDURE statement.

CALL conceptually returns list of result sets with one entry for every tabular result. An iterator can be used to iterate over these results sets. For each result set you can iterate over the result table in the same way as for query results. SQL statements that are not assigned to any table variable in the procedure body are added as result sets at the end of the list of result sets. The type of the result structures is determined during compilation time, but it is not visible in the signature of the procedure.

When executed by the client, the CALL syntax behaves in a way consistent with the SQL standard semantics; for example, Java clients can call a procedure using a JDBC CallableStatement. Scalar output variables are a scalar value that can be retrieved from the callable statement directly.

Unquoted identifiers are implicitly treated as upper case. Quoting identifiers respect capitalization and allow for using white spaces which are normally not allowed in SQL identifiers.

## Examples

Call the getOutput procedure in debug mode.

```sql
CALL getOutput (1000, 'EUR', NULL, NULL) IN DEBUG MODE;
```

Call the procedure getOutput using the WITH OVERVIEW option.

```sql
CALL getOutput(1000, 'EUR', ot_publishers, NULL) WITH OVERVIEW;
```

The following example creates a library with one member procedure and then calls the member procedure directly using the CALL statement:

```sql
CREATE LIBRARY MyLib AS BEGIN
  PUBLIC PROCEDURE MemberProc(IN i INT, OUT tv TABLE(Col1 NVARCHAR(10))) AS BEGIN
    tv = SELECT :i * 100 AS Col1 FROM DUMMY;
  END;
END;

CALL MyLib:MemberProc(1, ?);
```

## Related Information

SQL Notation Conventions [→](../../4.02-SQL-Notation-Conventions.md) Data Types [→](../../4.03-Data-Types/README.md) CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md)
