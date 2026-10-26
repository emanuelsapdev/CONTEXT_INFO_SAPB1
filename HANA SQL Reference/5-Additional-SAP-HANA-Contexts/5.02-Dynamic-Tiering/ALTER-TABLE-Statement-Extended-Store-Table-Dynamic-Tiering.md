# 5.2.9 ALTER TABLE Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1244–1250

Changes the definition of an extended store table.

## Syntax

#### Syntax 1 – Alter an Extended Store Table

```sql
ALTER TABLE <table_name>
   [<add_column_clause>]
   [<drop_column_clause>]
   [<alter_column_clause>]
   [<add_constraint_clause>]
   [<drop_primary_key_clause>]
   [<drop_constraint_clause>]
   [<owner_to_clause>]
```

#### Syntax 2 – Convert an Existing Column Store Table to an Extended Store Table

```sql
ALTER TABLE <table_name> <using_extended_storage_clause>
```

## Syntax Elements

#### table_name

Specifies the identifier of the table to be altered, with optional schema name.

```sql
<table_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

#### add_column_clause

Adds one or more columns to the specified table.

```sql
<add_column_clause> ::=
ADD ( {<column_definition> [<column_constraint_short>] [COMMENT
<string_literal>] } [, …] )
```

#### drop_column_clause

Removes one or more columns from the specified table.

```sql
<drop_column_clause> ::= DROP ( <column_name>[,...] )
```

#### alter_column_clause

Alters one or more column definitions.

```sql
<alter_column_clause> ::=
 ALTER ( {<column_definition> [<column_constraint>] [COMMENT
<string_literal>] }  [,…] )
```

Restrictions:

- For column tables, changing data type from a string to number (and back) is supported as long as the data fits into the target column size.
- For row tables, only increasing the size of VARCHAR and NVARCHAR type column is allowed. Other data type changes are not allowed.
- ALTER does not currently follow data type conversion rules.
- Adding NOT NULL constraint to an existing column is allowed if either of the following cases are true:
  - The table is empty.
  - The default value is specified when the table contains data.
  - The table does not contain a NULL-value in that column.
- You can only alter the comment for a column while making another change to the column (such as changing the data type).

##### column_definition

Defines a table column.

```sql
<column_definition> ::= <column_name> {<data_type>
  | <lob_data_type>} [<default_value_clause>]
```

##### column_name

Specifies the table column name.

```sql
<column_name> ::= <identifier>
```

##### data_type

The available data types.

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
   | DECIMAL
   | REAL
   | DOUBLE
   | VARCHAR
   | NVARCHAR
   | ALPHANUM
   | SHORTTEXT
   | VARBINARY
   | TEXT
   | BINTEXT
```

```sql
<lob_data_type> ::= <lob_type_name>
```

```sql
<lob_type_name> ::= BLOB | CLOB | NCLOB
```

##### default_value_clause

Specifies a value to be assigned to the column if an INSERT statement does not provide a value for the column.

```sql
<default_value_clause> ::= DEFAULT <default_value_exp>
```

```sql
<default_value_exp> ::= NULL
   | <string_literal>
   | <signed_numeric_literal>
   | <unsigned_numeric_literal>
   | <datetime_value_function>
```

```sql
<datetime_value_function> ::= CURRENT_DATE
   | CURRENT_TIME
   | CURRENT_TIMESTAMP
```

##### column_constraint

The column constraint rules.

```sql
<column_constraint> ::= NULL
   | NOT NULL
   | <unique_specification>
```

##### NULL

If NULL is specified it is not considered a constraint, it represents that a column that may contain a null value. The default is NULL.

##### NOT NULL

The NOT NULL constraint prohibits a column value from being NULL.

##### unique_specification

Specifies a unique constraint.

```sql
<unique_specification> ::=
 UNIQUE [<unique_tree_type_index>]
 | PRIMARY KEY [<unique_tree_type_index>]
```

If the index type is omitted, the SAP HANA database chooses the appropriate index by considering the column data type. If the index type is not specified, the SAP HANA database automatically selects an index type as follows:

| **Index type** | **Criteria** |
| --- | --- |
| CPBTREE | • character string types<br>• binary string types.<br>• decimal types<br>• when the constraint is a composite key<br>• when the constraint is a non-unique constraint |
| BTREE | All other cases than specified for CPBTREE |

Specifies a column as a unique key. A composite unique key enables the specification of multiple columns as a unique key. With a unique constraint, multiple rows cannot have the same value in the same column.

Specifies a column as a primary key. A primary key constraint is a combination of a NOT NULL constraint and a UNIQUE constraint. It prohibits multiple rows from having the same value in the same column.

##### unique_tree_type_index

Specifies the index type.

```sql
<unique_tree_type_index> ::= BTREE | CPBTREE;
```

Specifies a B+-tree index. B+-tree is a tree that maintains sorted data, which performs efficient insertion, deletion and search of records.

CPBTREE specifies a CPB+-tree index. CPB+-tree stands for Compressed Prefix B+-Tree, which is based on pkB-tree. CPB+-tree is a very small index because it uses 'partial key' that is only part of full key in index nodes. CPB+-tree shows better performance than B+-Tree for larger keys.

#### add_constraint_clause

Adds a table constraint.

```sql
<add_constraint_clause> ::=
 ADD [CONSTRAINT <constraint_name>] <table_constraint>
<constraint_name> ::= <identifier>
```

##### table_constraint

The table constraint can be either a unique constraint.

```sql
<table_constraint> ::= <unique_constraint_definition>
```

##### unique_constraint_definition

The unique specification.

```sql
<unique_constraint_definition> ::= <unique_specification>
(<unique_column_name_list>)
```

##### unique_column_name_list

Specifies the unique column name list, which can have one or more column names.

```sql
<unique_column_name_list> ::=
 <unique_column_name>[{, <unique_column_name>}...]
<unique_column_name> ::= <identifier>
```

#### drop_primary_key_clause

Drops the primary key constraint.

```sql
<drop_primary_key_clause> ::= DROP PRIMARY KEY
```

#### drop_constraint_clause

Drops a unique or referential constraint.

```sql
<drop_constraint_clause> ::= DROP CONSTRAINT <constraint_name>
<constraint_name> ::= <identifier>
```

#### using_extended_storage_clause

Modifies table to be an extended store table.

```sql
<using_extended_storage_clause> ::= [NOT] USING EXTENDED STORAGE [{ENABLE |
DISABLE} DELTA]
```

> **Note**
>
> - Extended storage must already exist.
>
> - DBO, SYS, and PUBLIC are reserved words within extended storage. Schemas with these names cannot have extended store tables.
>
> - DELTA must be enabled on extended storage to enable at enable on extended table.
>
> - DELTA not supported for data types BLOB, CLOB and NCLOB.

##### NOT USING EXTENDED STORAGE

Converts an extended table to a column store table.

##### USING EXTENDED STORAGE

Converts a column store table to an extended table.

##### ENABLE DELTA

Allows row level versioning on an extended table. DELTA facilitates faster inserts.

##### DISABLE DELTA

Disables row level versioning on an extended table.

#### owner_to_clause

Specifies a new owner for the table.

```sql
<owner_to_clause> ::= OWNER TO <user_name>
```

The new owner becomes the grantor for all of the privileges on the table that were granted by the old owner. Also, the old owner is granted all privileges for the table by the new owner so that they can continue running jobs on the table.

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The ALTER TABLE (extended store table) statement changes the definition of an extended store table.

## Examples

To convert table `t1` to an extended store table with DELTA enabled.

```sql
ALTER TABLE t1 USING EXTENDED STORAGE ENABLE DELTA;
```

To convert extended store table `t1` to be an SAP HANA table.

```sql
ALTER TABLE t2 NOT USING EXTENDED STORAGE
```

To enable delta on extended store table `t3`.

```sql
ALTER TABLE t3 USING EXTENDED STORAGE ENABLE DELTA
```

To add a column `C` to extended store table `t4`.

```sql
ALTER TABLE t4 ADD (C INT)
```

To drop column `C` on extended store table `t4`.

```sql
ALTER TABLE t4 DROP (C)
```

To add column constraint `UK` on column `B` on extended store table `t4`.

```sql
ALTER TABLE t4 ADD CONSTRAINT UK UNIQUE (B)
```

To drop column constraint `UK` on extended store table `t4`.

```sql
ALTER TABLE t4 DROP CONSTRAINT UK
```

To rename extended store table `t4` to `t5`.

```sql
RENAME TABLE t4 TO t5
```

To delete extended store table `t5`.

```sql
DROP TABLE t5
```

## Related Information

TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md) TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md)
