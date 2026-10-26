# 4.10.1.81 DO BEGIN...END Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 889–893

Executes an anonymous block a single time.

## Syntax

```sql
DO
 [ <named_parameters_list> ] [ ( <bound_parameter_clause> ) ]
  BEGIN [ <block_properties > ]
    <variable_declaration>
    <statement_list>
  END
```

## Syntax Elements

#### named_parameters_list

Specifies the list of named parameters.

```sql
<named_parameters_list> ::= ( [ <named_parameter>] [ { ,<named_parameter> }
… ] )
```

##### named_parameter

Specifies the name of the parameter.

```sql
<named_parameter> ::= <parameter_mode>, <parameter_name>, <type_name>
```

#### bound_parameter_clause

Specifies the input and output parameters for the procedure with value bindings.

```sql
<bound_parameter_clause> ::= <bound_parameter> [, … ]
```

##### bound_parameter

Specifies a procedure parameter with its associated data type and value binding.

```sql
<bound_parameter> ::= <parameter> => <proc_param>
```

##### proc_param

Specifies procedure parameters.

#### block_properties

Specifies one or more properties to apply to the block.

```sql
<block_properties> ::=
 SEQUENTIAL EXECUTION
 | PARALLEL EXECUTION
 | AUTONOMOUS TRANSACTION
```

##### SEQUENTIAL EXECUTION

Specify SEQUENTIAL EXECUTION to sequence the execution of independent DML statements and read-write procedure calls.

##### PARALLEL EXECUTION

Specify PARALLEL EXECUTION to parallelize the execution of independent DML statements and read-write procedure calls.

##### AUTONOMOUS TRANSACTION

Specify AUTONOMOUS TRANSACTION if you want the block to be executed independently of the main procedure. Changes made and committed using AUTONOMOUS TRANSACTION persist regardless of whether the main procedure transaction is committed or rolled back. The end of an AUTONOMOUS TRANSACTION block has an implicit commit.

#### variable_declaration

Declares variables for use in anonymous block.

```sql
<variable_declaration> ::=
 <declaration>
 [ <declaration> ]
 […]
<declaration> ::=
 DECLARE <variable_name> { <sql_data_type> | TABLE ( <column_definition> [,…]
[ SEARCH KEY ( <column_name> [,…] ) ;
 | DECLARE <variable_name> AUTO <default_value>;
 <column_definition> ::= <column_name> <sql_data_type>
 <default_value> ::= { ( DEFAULT | := | = ) { <value> | <expression> }
```

Specifying AUTO allows you to declare a variable and its default value without having to explicitly set the data type.

#### statement_list

Specifies one or more statements to execute as part of the anonymous block.

## Description

An anonymous block is only executed once. All SQLScript statements supported in procedures are also supported in anonymous blocks. Unlike procedures, an anonymous block has no corresponding object created in the catalog.

Anonymous blocks are defined and executed in a single step. Therefore, lifecycle handling like CREATE or DROP is not needed. The body of an anonymous block is similar to the procedure body.

To return a result set, use a SELECT statement because anonymous blocks do not have any parameters defined.

For output parameters, `?` is a valid value and cannot be omitted because otherwise the query parameter cannot be bound. For input parameters, the name of a physical table can be set. For scalar input parameters, any scalar expression can be used, except for scalar UDF. DEFAULT EMPTY and INOUT parameters are not supported.

## Examples

Execute an anonymous block that creates a table and inserts values into that table.

```sql
DO
BEGIN
    DECLARE I INTEGER;
    CREATE ROW TABLE TAB1 (I INTEGER);
    FOR I IN 1..10 DO
        INSERT INTO TAB1 VALUES (:I);
    END FOR;
END;
```

Execute an anonymous block and return the result set by using a SELECT statement.

```sql
DO
BEGIN
    T1 = SELECT I, 10 AS J FROM TAB;
    T2 = SELECT I, 20 AS K FROM TAB;
    T3 = SELECT J, K FROM :T1, :T2 WHERE :T1.I = :T2.I;
    SELECT * FROM :T3;
END;
```

Execute an anonymous block that calls another procedure.

```sql
DO
BEGIN
    T1 = SELECT * FROM TAB;
    CALL PROC3(:T1, :T2);
    SELECT * FROM :T2;
END;
```

Execute an anonymous block that includes an exception handler.

```sql
DO
BEGIN
    DECLARE I, J INTEGER;
    BEGIN
        DECLARE EXIT HANDLER FOR SQLEXCEPTION
        IF ::SQL_ERROR_CODE = 288 THEN
            DROP TABLE TAB;
            CREATE ROW TABLE TAB (I INTEGER PRIMARY KEY);
        ELSE
            RESIGNAL;
        END IF;
        CREATE ROW TABLE TAB (I INTEGER PRIMARY KEY);
    END;
    FOR I in 1..3 DO
        INSERT INTO TAB VALUES (:I);
    END FOR;
    IF :J <> 3 THEN
        SIGNAL SQL_ERROR_CODE 10001;
    END IF;
END;
```

Execute an anonymous block that uses COMMIT and ROLLBACK.

```sql
DO
BEGIN
    CREATE ROW TABLE TAB2 (K INT);
    COMMIT;
    DROP TABLE TAB;
    CREATE ROW TABLE TAB (J INT);
    ROLLBACK;
    DELETE FROM TAB;
END;
```

Execute an anonymous block that calls a procedure to process the selected data.

```sql
DO
  BEGIN
    T1 = SELECT I, 10 AS J FROM TAB;
    T2 = SELECT I, 20 AS K FROM TAB;
    T3 = SELECT J, K FROM :T1, :T2 WHERE :T1.I = :T2.I;
    CALL PROC3(:T3, T4);
    SELECT * FROM :T4;
  END;
```

Execute an anonymous block that runs a loop to insert data into a table.

```sql
DO
  BEGIN
    DECLARE I INTEGER;
    FOR I in 1..3 DO
        INSERT INTO TAB VALUES (:I);
    END FOR;
END;
```

Execute an anonymous block that computes the sum of two integers.

```sql
DO (IN A INT => 1, IN B INT => ?, OUT C INT => ?)
BEGIN
    C = :A + :B;
END;
```

## Related Information

[CREATE PROCEDURE Statement (Procedural)](CREATE-PROCEDURE-Statement-Procedural.md)
