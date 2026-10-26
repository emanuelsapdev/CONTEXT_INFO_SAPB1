# 4.10.1.76 CREATE VIRTUAL TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 875–878

Creates a virtual table at a remote source.

## Syntax

Syntax 1 - Create a virtual table.

```sql
CREATE VIRTUAL TABLE <virtual_table_name>
    AT <remote_location_clause> [ <remote_property_clause> ]
```

Syntax 2 - Create a remote table while creating a virtual table.

```sql
CREATE VIRTUAL TABLE <virtual_table_name> <table_contents_source>
    AT <remote_location_clause> WITH REMOTE
```

## Syntax Elements

#### virtual_table_name

Specifies a unique name for the virtual table.

```sql
<virtual_table_name> ::= [ <schema_name>.]<identifier>
```

#### table_contents_source

Specifies the source from which the table definition is derived.

```sql
<table_contents_source> ::= ( <table_element> [, <table_element> [, ... ] ] )
```

##### table_element

Defines the table columns with associated column or table constraints.

```sql
<table_element> ::=
 <column_definition> [ <column_constraint> ]
```

##### column_definition

Defines a table column.

```sql
<column_definition> ::= <column_name> <data_type>
[ <default_value_clause> ]
```

**column_name** Specifies the column name.

```sql
<column_name> ::= <identifier>
```

###### data_type

Specifies the column data types.

```sql
<data_type> ::=
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
 | VARCHAR [ (<unsigned_integer>) ]
 | NVARCHAR [ (<unsigned_integer>) ]
 | VARBINARY [ (<unsigned_integer>) ]
 | DECIMAL [ (<unsigned_integer> [, <unsigned_integer> ]) ]
 | FLOAT [ (<unsigned_integer>) ]
 | BOOLEAN
```

###### default_value_clause

Specifies a value to be assigned to the column if an INSERT statement does not provide a value for the column.

```sql
<default_value_clause> ::= DEFAULT <default_value_exp>
<default_value_exp> ::=
 NULL
 | <string_literal>
 | <signed_numeric_literal> <unsigned_numeric_literal>
 | <datetime_value_function>
<datetime_value_function> ::=
 CURRENT_DATE
 | CURRENT_TIME
 | CURRENT_TIMESTAMP
 | CURRENT_UTCDATE
 | CURRENT_UTCTIME
 | CURRENT_UTCTIMESTAMP
```

##### column_constraint

Specifies the column constraint rules.

```sql
<column_constraint> ::= NULL | NOT NULL | <unique_specification>
```

###### NULL

Allows NULL values in the column. If NULL is specified it is not considered a constraint, it represents that a column that may contain a null value. The default is NULL.

###### NOT NULL

Prohibits NULL values in the column.

###### unique_specification

Specifies unique constraints.

```sql
<unique_specification> ::= UNIQUE | PRIMARY KEY
```

###### UNIQUE

Specifies a column as a unique key. A composite unique key enables the specification of multiple columns as a unique key. With a unique constraint, multiple rows cannot have the same value in the same column.

A UNIQUE column can contain multiple NULL values.

###### PRIMARY KEY

Specifies a primary key constraint, which is a combination of a NOT NULL constraint and a UNIQUE constraint.

#### remote_location_clause

Identifies a remote object (table or view) at an existing remote source.

```sql
<remote_location_clause> ::=
"<remote_source_name>"."<database_name>"."<schema_name>"."<identifier>"
```

For SAP HANA, SAP IQ, SAP MaxDB, Terradata, and IBM DB2 remote sources, you can use NULL for `<database_name>`.

#### remote_property_clause

Specifies the parameters and their values to be set for the virtual table as XML.

```sql
<remote_property_clause> ::=
 [REMOTE PROPERTY 'dataprovisioning_parameters'=<dataprov_params_value>]
<dataprov_params_value> ::= <string_literal>
```

The REMOTE PROPERTY clause allows you to specify data provisioning parameters for the virtual table that is being created. The parameters list is sent to the adapter as a parameter for the remote object metadata request. **WITH REMOTE** Creates a table on the remote source using the `<table_contents_source>` definition and a corresponding virtual table on the local source. The WITH REMOTE option is supported for remote sources using the following SDA adapters: hanaodbc, iqodbc, aseodbc, tdodbc, voraodbc, odbc (Oracle, Microsoft SQL Server, IBM Netezza, IBM DB2, BigQuery). It is not supported with an SDI adapter.

## Description

The CREATE VIRTUAL TABLE provides a way to access an existing table/view on a remote source from an SAP HANA instance. The list of remote columns is automatically imported into the virtual table.

Use the DROP TABLE `<table_name>` to drop a virtual table.

## Permissions

Syntax 1 - This syntax requires the CREATE VIRTUAL TABLE object privilege.

Syntax 2 - This syntax requires the CREATE VIRTUAL TABLE and REMOTE TABLE ADMIN object privileges. If the credential type of the remote source is PASSWORD, then only the owner of the remote sources who set the technical user credentials has the authorization to use the WITH REMOTE clause. For all other credential types, authorization is a function of the privileges of the user on the remote source.

## Examples

Create virtual table `VT` on existing remote source `S`. The originating table is `tableA`, which is within the schema `SYSTEM` on `HA1`.

```sql
CREATE VIRTUAL TABLE VT AT "S"."HA1"."SYSTEM"."tableA";
```

Create a virtual table where the following string is sent to the adapter as a parameter for the metadata request: `<Parameter name="objects">1,10,1000,300</Parameter><Parameter name="stateHierarchy">USA</Parameter><Parameter name="date”>2014-06-01</Parameter>`

```sql
CREATE VIRTUAL TABLE ….
   REMOTE PROPERTY 'dataprovisioning_parameters'='<Parameter
name="objects">1,10,1000,300</Parameter>
   <Parameter name="stateHierarchy">USA</Parameter><Parameter
name="date">2014-06-01</Parameter>';
```

Create table A1 on remote source Remote1 and create a corresponding virtual table virtual_A1 in the local source.

```sql
CREATE VIRTUAL TABLE virtual_A1 (a int, b int) at "Remote1"."HA1"."SYSTEM"."A1"
WITH REMOTE;
```

## Related Information

[Introduction to SQL](../../4.01-Introduction-to-SQL.md)
