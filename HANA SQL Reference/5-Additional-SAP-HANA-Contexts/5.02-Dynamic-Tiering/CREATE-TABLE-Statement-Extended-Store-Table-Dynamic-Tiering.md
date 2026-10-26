# 5.2.21 CREATE TABLE Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1298–1302

Creates a new extended store table in the extended storage.

## Syntax

```sql
CREATE [ COLUMN ] TABLE  <table_name>
   (<table_contents_source>, ...)
   <using_extended_storage_clause>
```

## Syntax Elements

#### table_name

```sql
<table_name> ::= [<schema_name>.]<identifier>
```

```sql
<schema_name> ::= <unicode_name>
```

#### table_contents_source

You can create a table by describing the table elements, see below.

```sql
<table_contents_source> ::=
(<table_element>, ...)
   | [(<column_name>, ...)]
```

##### table_element

Defines the table columns with associated column or table constraints.

```sql
<table_element> ::=
 <column_definition> [<column_constraint>]
 | <table_constraint>
```

##### column_definition

Defines the table columns with associated column or table constraints.

```sql
<column_definition> ::= <column_name> {<data_type>
   | <lob_data_type>} [<default_value_clause>]
```

##### column_constraint

See `<column constraint>`.

##### table_constraint

See `<table constraint>`.

**column_name** Specifies the column name.

```sql
<column_name> ::= <identifier>
```

##### data_type

Specifies the column data types.

```sql
<data_type>  ::= DATE
| TIME
| SECONDDATE
| TIMESTAMP
| TINYINT
| SMALLINT
| INTEGER
| BIGINT
| SMALLDECIMAL
| DECIMAL
| REAL
| DOUBLE
| VARCHAR
| NVARCHAR
| ALPHANUM
| SHORTTEXT
| VARBINARY
| BINTEXT
```

##### lob_data_type

Specifies the LOB data type.

```sql
<lob_data_type> ::= <lob_type_name> [MEMORY THRESHOLD
memory_threshold_value]
```

**lob_type_name** `<lob_type_name>` ::= BLOB | CLOB | NCLOB

##### default_value_clause

Specifies a value to be assigned to the column if an INSERT statement does not provide a value for the column.

```sql
<default_value_clause> ::=
DEFAULT <default_value_exp>
```

```sql
<default_value_exp> ::=
NULL
| <string_literal>
| <signed_numeric_literal>
| <unsigned_numeric_literal>
| <datetime_value_function>
```

```sql
<datetime_value_function> ::=
CURRENT_DATE
| CURRENT_TIME
| CURRENT_TIMESTAMP
```

##### column_constraint

Specifies the column constraint rules.

```sql
<column_constraint> ::=
    NULL
| NOT NULL
| <unique_specification>
```

###### NULL

Allows NULL values in the column. If NULL is specified it is not considered a constraint, it represents that a column that may contain a null value. The default is NULL.

###### NOT NULL

Prohibits NULL values in the column.

###### unique_specification

Specifies unique constraints.

```sql
<unique_specification> ::= UNIQUE [<unique_tree_type_index>]
                         | PRIMARY KEY [<unique_tree_type_index>]
```

If the index type is omitted, the SAP HANA database chooses the appropriate index by considering the column data type. If the index type is not specified, the SAP HANA database automatically selects an index type as follows:

| **Index type** | **Criteria** |
| --- | --- |
| CPBTREE | • character string types<br>• binary string types<br>• decimal types<br>• when the constraint is a composite key<br>• when the constraint is a non-unique constraint |
| BTREE | All other cases than specified for CPBTREE |

###### UNIQUE

Specifies a column as a unique key. A composite unique key enables the specification of multiple columns as a unique key. With a unique constraint, multiple rows cannot have the same value in the same column.

###### unique_tree_type_index

Specifies the index type.

```sql
<unique_tree_type_index> ::= { BTREE | CPBTREE }
```

###### BTREE

Specifies a B+-tree index. B+-tree is a tree that maintains sorted data, which performs efficient insertion, deletion, and search of records. **CPTREE** Specifies a CPB+-tree index. CPB+-tree stands for Compressed Prefix B+-Tree, which is based on pkB-tree. CPB+-tree is a very small index because it uses 'partial key' that is only part of full key in index nodes. CPB+-tree shows better performance than B+- Tree for larger keys.

###### PRIMARY KEY

Specifies a primary key constraint, which is a combination of a NOT NULL constraint and a UNIQUE constraint.

##### table_constraint

```sql
<table_constraint> ::=
<unique_constraint_definition>
```

###### unique_constraint_definition

The unique specification. See `<unique_specification>`.

```sql
<unique_constraint_definition> ::=
<unique_specification> (<unique_column_name_list>)
```

###### unique_column_name_list

Specifies the unique column name list, which can have one or more column names.

```sql
<unique_column_name_list> ::= <unique_column_name>[{,
<unique_column_name>}...]
```

**unique_column_name** A column name identifier.

```sql
<unique_column_name> ::= <identifier>
```

#### using_extended_storage_clause

Creates an extended store table.

```sql
<using_extended_storage_clause> ::=
   USING EXTENDED STORAGE [{ENABLE | DISABLE} DELTA]
```

> **Note**
>
> - Extended storage must already exist.
>
> - DBO, SYS, and PUBLIC are reserved words within extended storage. Schemas with these names cannot have extended store tables.

**ENABLE | DISABLE DELTA** Enable row-level versioning (DELTA) on the extended store table. Enabling DELTA facilitates faster inserts.

> **Note**
>
> DELTA not supported for data types BLOB, CLOB and NCLOB.

## Permissions

You have the EXTENDED STORAGE ADMIN privilege.

## Description

The CREATE TABLE statement with the USING EXTENDED STORAGE clause creates an extended store table.

## Example

You create table t1 as an extended store table where column A and B are INTEGER-type, column A is the primary key constraint, and DELTA is enabled.

```sql
CREATE COLUMN TABLE t1 (A INT PRIMARY KEY, B INT) USING EXTENDED STORAGE ENABLE
DELTA;
```

You create table t2 as an extended store table where columns A, B, and C are INTEGER-type, columns A and B allow NULL values (default when not specified is NULL), but column C does not.

```sql
CREATE COLUMN TABLE t2(A INT, B INT NULL, C INT NOT NULL) USING EXTENDED STORAGE;
```

You create table t3 as an extended store table where all columns are INTEGER-type, column A is the primary key and columns B and C have UNIQUE constraints.

```sql
CREATE COLUMN TABLE t3 (A INT PRIMARY KEY, B INT UNIQUE BTREE, C INT, UNIQUE
CPBTREE(C)) USING EXTENDED STORAGE;
```

You create table t4 as an extended store table where columns A, B, and C are INTEGER-type, columns A and B do not allow NULL values, column C is the primary key and has a UNIQUE constraint.

```sql
CREATE COLUMN TABLE t4 (A INT NOT NULL, B INT NOT NULL, C INT, PRIMARY KEY
CPBTREE(A, B), UNIQUE(C)) USING EXTENDED STORAGE;
```

## Related Information

TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md)
