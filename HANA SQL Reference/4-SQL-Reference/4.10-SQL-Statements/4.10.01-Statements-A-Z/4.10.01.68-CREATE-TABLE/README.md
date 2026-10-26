# 4.10.1.68 CREATE TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 778–815

Creates a base or temporary table. See the CREATE VIRTUAL TABLE statement for creating virtual tables.

## Syntax

```sql
CREATE [ <table_type> ] { <table_name> | <replica_name> }
   <table_contents_source>
   [<system_versioning_spec>]
   [<application_time_period_configuration>]
   [<bi_temporal_table_spec>]
   [<with_association_clause>]
   [<with_annotation_clause>]
   [<with_mask_clause>]
   [<logging_option>]
   [<auto_merge_option>]
   [<unload_priority_clause>]
   [<schema_flexibility_option>]
   [<partition_clause>]
   [<persistent_memory_spec_clause>]
   [<group_option_list>]
   [<location_clause>]
   [<replica_clause>]
   [<global_temporary_option>]
   [<series_clause>]
   [<unused_retention_period_option>]
   [<record_commit_timestamp_clause>]
   [COMMENT <comment_string>]
   [<numa_node_preference_clause>]
   [<load_unit>]
```

## Syntax Elements

#### table_type

Defines the type of table to create.

```sql
<table_type> ::=
 { ROW | [ COLUMN ] } TABLE
 | HISTORY COLUMN TABLE
 | HISTORY COLUMN TABLE
 | <temporary_table_type>
 | VIRTUAL TABLE
<temporary_table_type> ::=
 GLOBAL TEMPORARY { [ ROW ] | COLUMN } TABLE
 | LOCAL TEMPORARY { [ ROW ] | COLUMN } TABLE
```

If neither ROW nor COLUMN is specified, the default ROW for temporary tables (local and global), and COLUMN for non temporary tables.

##### ROW and COLUMN TABLE

Creates a row or column table, respectively. If the majority of table access is through a large number of tables with only a few selected attributes, then use COLUMN-based storage. If the majority of table access involves selecting a few records with all attributes selected, then ROW-based storage is preferable. The SAP HANA database uses a combination of table types to enable storage and interpretation in both ROW and COLUMN forms.

##### HISTORY COLUMN TABLE

Creates a column table with a particular transaction session type called HISTORY. Tables with the session type HISTORY support time travel queries. Time travel queries are queries against historical states of the database.

##### temporary_table_type

A simple comparison of the temporary table types is provided in this table. To learn more information about each type, see the descriptions found after the table.

| **Characteristic** | **Global temp (column)** | **Global temp (row)** | **Local temp (column)** | **Local temp (row)** |
| --- | --- | --- | --- | --- |
| Metadata shared across sessions | Yes | Yes | No | No |
| Dropped after session terminates | No | No | Yes | Yes |
| Allows add or drop of primary key | No | Yes | No | No |
| Allows add or drop of identity column | No | Yes | No | No |

##### GLOBAL TEMPORARY ROW TABLE

Creates a global temporary row table and makes the table definition globally available while data is visible only to the current session. Metadata for a global temporary table persists and is shared across sessions. The data in a global temporary table is sessionspecific, meaning only the session owner of a global temporary table can insert, read, or truncate the data for the session. As well, data in a temporary table is automatically dropped when the session is terminated. You can drop a global temporary table, but only after you truncate the sessionspecific data.

Supported operations:

- Create with or without a primary key
- Add or drop a primary key
- Add or drop an identity column
- Add or drop unique constraint
- Rename table
- Add, alter, rename, or drop column
- Truncate
- Drop
- Create or drop a view on a global temporary table
- Create synonym
- Select
- Select into or insert
- Delete
- Update
- Upsert or replace

##### GLOBAL TEMPORARY COLUMN TABLE

Creates a global temporary column table and makes the table definition globally available while data is visible only to the current session.

Metadata for a global temporary table persists and is shared across sessions. The data in a global temporary table is sessionspecific, meaning only the session owner of a global temporary table can insert, read, or truncate the data for the session. As well, data in a temporary table is automatically dropped when the session is terminated. You can drop a global temporary table, but only after you truncate the sessionspecific data.

Supported operations:

- Create without a primary key
- Truncate
- Drop
- Create or drop a view on a global temporary column table
- Create synonym
- Select
- Select into or insert

##### LOCAL TEMPORARY ROW TABLE

Creates a local temporary row table, visible only to the current session.

Metadata exists for the duration of the session and is session specific, meaning only the session owner of the local temporary table can see it. The table is dropped at the end of the session.

Data in a local temporary row table is session specific, meaning only the session owner of the local temporary row table can insert, read, or truncate the data.

Primary keys are supported on LOCAL TEMPORARY ROW tables.

Supported operations:

- Create with or without a primary key
- Truncate
- Drop
- Select
- Select into or insert
- Delete
- Update
- Upsert or replace

##### LOCAL TEMPORARY COLUMN TABLE

Creates a local temporary column table, visible only to the current session.

Metadata exists for the duration of the session and is sessionspecific, meaning only the session owner of the local temporary column table can see. The table is dropped at the end of the session.

Data in a local temporary column table is sessionspecific, meaning only the session owner of the local temporary column table can insert, read, or truncate the data.

Supported operations:

- Create without a primary key
- Truncate
- Drop
- Select
- Select into or insert

##### VIRTUAL TABLE

Creates a virtual table based on an existing table/view inside a remote source.

#### table_name

Specifies a name for the table

```sql
<table_name> ::= [ <schema_name>.]<identifier>
```

#### replica_name

Specifies the schema and a name for the new replica. This clause is for use with creating a replica based on an existing source table (CREATE TABLE...LIKE). See `<like_table_clause>` [→](README.md).

```sql
<replica_name> ::= [ <replica_schema_name>.]<identifier>
```

#### table_contents_source

Specifies the source from which the table definition is derived.

```sql
<table_contents_source> ::=
 (<table_element>, ...) [<with_association_clause>]
 | <like_table_clause>
 | [(<column_name>, ...)] <as_subquery>
```

You can create a table in the following ways:

- Describing the table elements (defined in this section).
- Basing the new table on an existing table (CREATE TABLE...LIKE). See`<like_table_clause>` [→](README.md)).
- From the result of a subquery (CREATE TABLE...AS). See`<subquery>` [→](README.md)).

##### table_element

Defines the table columns with associated column or table constraints.

```sql
<table_element> ::=
 <column_definition> [ <column_constraint> ]
 | <table_constraint>
```

##### column_definition

Defines a table column.

```sql
<column_definition> ::= <column_name> { <data_type> | <lob_data_type> }
   [ <ddic_data_type> ]
   [ <default_value_clause> ]
   [ <clientside_encryption> ]
   [ <col_gen_as_expression> | <col_gen_as_ident> ]
[ <col_calculated_field> ]
[ <schema_flexibility> ]
[ <fuzzy_search_index> ]
[ <fuzzy_search_mode> ]
[ <persistent_memory_spec_clause> ]
[ COMMENT <comment_string> ]
[ <load_unit> ]
[ <numa_node_preference_clause> ]
```

**column_name** Specifies the column name.

```sql
<column_name> ::= <identifier>
```

###### data_type

Specifies the column data types.

```sql
<data_type> ::=
ARRAY
 | DATE
 | TIME
 | SECONDDATE
 | TIMESTAMP
 | TINYINT
 | SMALLINT
 | INT
 | BIGINT
 | SMALLDECIMAL
 | REAL
 | DOUBLE
 | TEXT
 | BINTEXT
 | VARCHAR [ (<unsigned_integer>) ]
 | NVARCHAR [ (<unsigned_integer>) ]
 | ALPHANUM [ (<unsigned_integer>) ]
 | SHORTTEXT [ (<unsigned_integer>) ]
 | VARBINARY [ (<unsigned_integer>) ]
 | DECIMAL [ (<unsigned_integer> [, <unsigned_integer> ]) ]
 | FLOAT [ (<unsigned_integer>) ]
 | BOOLEAN
```

For tables with time-selection partitioning, the data type for the time-selection column must be NVARCHAR(8).

###### lob_data_type

Specifies the LOB data type.

```sql
<lob_data_type> ::=
 <lob_type_name> [ MEMORY THRESHOLD <memory_threshold_value> ]
```

###### lob_type_name

Specifies the type of LOB.

```sql
<lob_type_name> ::= { BLOB | CLOB | NCLOB }
```

###### ddic_data_type

The available data types.

```sql
<ddic_data_type> ::=
 DDIC_ACCP | DDIC_ALNM | DDIC_CHAR | DDIC_CDAY | DDIC_CLNT | DDIC_CUKY
| DDIC_CURR | DDIC_D16D
 | DDIC_D34D | DDIC_D16R | DDIC_D34R | DDIC_D16S | DDIC_D34S |
DDIC_DATS | DDIC_DAY  | DDIC_DEC
 | DDIC_FLTP | DDIC_GUID | DDIC_INT1 | DDIC_INT2 | DDIC_INT4 |
DDIC_INT8 | DDIC_LANG | DDIC_LCHR
 | DDIC_MIN  | DDIC_MON  | DDIC_LRAW | DDIC_NUMC | DDIC_PREC |
DDIC_QUAN | DDIC_RAW  | DDIC_RSTR
 | DDIC_SEC  | DDIC_SRST | DDIC_SSTR | DDIC_STRG | DDIC_STXT |
DDIC_TIMS | DDIC_UNIT | DDIC_UTCM
 | DDIC_UTCL | DDIC_UTCS | DDIC_TEXT | DDIC_VARC | DDIC_WEEK
```

###### memory_threshold_value

Specifies whether LOB data should be stored in memory.

```sql
<memory_threshold_value> ::= { <unsigned_integer> | NULL }
```

- If `<memory_threshold_value>` is not provided, then a hybrid LOB with a memory threshold of 1000 is created by default.
- If `<memory_threshold_value>` is provided and its LOB size is bigger than the memory threshold value, then the LOB data is stored on disk.
- If `<memory_threshold_value>` is provided and its LOB size is equal or less than the memory threshold value, then the LOB data is stored in memory.
- If `<memory_threshold_value>` is NULL, then all LOB data is stored in memory.
- If `<memory_table lobthreshold_value>` is 0, then all LOB data is stored in disk.

This type of index can only be used for column store tables.

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

###### clientside_encryption

Enables client-side encryption on a column.

```sql
CLIENTSIDE ENCRYPTION ON WITH <column_encryption_key_name> [ RANDOM |
DETERMINISTIC ]
<column_encryption_key_name> ::= [ <schema_name>.]<identifier>
```

RANDOM and DETERMINISTIC describe the type of encryption used by the algorithm to encrypt the data. RANDOM ensures that a given cleartext value is never encrypted into the same ciphertext more than once. DETERMINISTIC ensures that a given cleartext value is always encrypted into the same ciphertext value. Deterministic encryption allows some operations such as equality comparisons on encrypted data, whereas non-deterministic encryption (RANDOM), while stronger, limits operations to basic inserts, updates, and fetches. Choose the type of encryption based on how the data is intended to be used. RANDOM is the default setting.

Client-side encrypted columns are represented physically as VARBINARY.

`<column_encryption_key_name>` must be a valid column encryption key, and you must have the USAGE permission on `<column_encryption_key_name>` to specify it. `<column_encryption_key_name>` and the table whose column is being encrypted must exist in the same schema.

###### col_gen_as_expression

Specifies the expression to generate the column value at runtime.

```sql
<col_gen_as_expression> ::= GENERATED ALWAYS AS <expression>
```

###### col_gen_as_ident

Specifies an identity column. Only one can be specified per table.

Generated columns are only supported in column store table definitions, and can only reference base columns that are defined prior to them in the DDL statement (that is, to the left of them). You cannot define a default for a generated column, and they cannot be used as part of a primary key or unique constraint.

You cannot drop a base column that is referenced by a generated column.

```sql
<col_gen_as_ident> ::=
 GENERATED { ALWAYS | BY DEFAULT } AS IDENTITY [ ( <sequence_option> ) ]

<sequence_option> ::=
 <sequence_param_list>
 | RESET BY <subquery>
 | <sequence_param_list> RESET BY <subquery>

<sequence_param_list> ::= <sequence_parameter> [, <sequence_parameter>
[,…] ]

<sequence_parameter> ::=
 START WITH <start_value>
 | INCREMENT BY <increment_value>
 | MAXVALUE <max_value>
 | NO MAXVALUE
 | MINVALUE <min_value>
 | NO MINVALUE
 | CYCLE
 | NO CYCLE
 | CACHE <cache_size>
 | NO CACHE
 | RESET BY <subquery>
```

There are two types of IDENTITY columns: GENERATED ALWAYS, and GENERATED BY DEFAULT:

###### GENERATED ALWAYS

A GENERATED ALWAYS AS IDENTITY column increments based solely on the sequence parameter settings (`<sequence_param_list>`). With the exception changes to the RESET BY definition, the sequence defined for a GENERATED ALWAYS IDENTITY column cannot be altered or reset after it has been set, and inserting a value into a GENERATED ALWAYS identity column fails and returns an error.

Non-deterministic functions are not allowed for columns defined as GENERATED ALWAYS.

###### GENERATED BY DEFAULT

A GENERATED BY DEFAULT IDENTITY column increments using the sequence parameter settings (`<sequence_param_list>`) only when no identity value is specified in the INSERT statement (that is, the identity column is left out of the insert column list). When a value is specified for the identity column during the INSERT, then the specified value is inserted (assuming the value does not already exist) and the following behavior occurs with respect to the value of the identity column:

- If the specified value is higher than the existing identity value with a positive increment, then this resets the current sequence value to an allowable sequence value that is equal to the specified value, or the next one lower than the specified value.
- If the specified value is lower than the existing value with a negative increment, then this resets the current sequence value to an allowable sequence value that is equal to the specified value, or the next one higher than the specified value.
- Otherwise, the current sequence value is not reset.

Identity columns are supported in global and local temporary tables, both for row store and column store tables. They can be added to, or dropped from, a table. However, they cannot be altered.

If RESET BY `<subquery>` is specified, then during the restart of the database, the database automatically executes the subquery and restarts the sequence value with the returned value. If RESET BY is not specified, then the sequence value is stored persistently in the database. During the restart of the database, the next value of the sequence is generated from the saved sequence value.

For more information on subqueries, see the SELECT statement.

For more information on sequences and sequence parameters, see the CREATE SEQUENCE statement.

###### col_calculated_field

Specifies the expression that replaces the column at query compilation time.

```sql
<col_calculated_field> ::= AS <expression>
```

- The data type of a calculated field column can be a default value.
- The calculated field column can reference not only base columns, but also other calculated field columns.
- The maximum of recursive calculated field is 16.
- Dropping or altering the base columns of a calculated field is not possible.

###### schema_flexibility

Specifies whether the column is dynamic.

```sql
<schema_flexibility> ::= { ENABLE | DISABLE } SCHEMA FLEXIBILITY
```

- ENABLE changes the column into a dynamic column.
- DISABLE (default value) changes the column into a static column.

###### fuzzy_search_index

Turns a fuzzy search index on or off (the default).

```sql
<fuzzy_search_index> ::= FUZZY SEARCH INDEX { ON | OFF }
```

###### fuzzy_search_mode

Sets the fuzzy search mode with the value of `<string_literal>`.

```sql
<fuzzy_search_mode> ::=
 FUZZY SEARCH MODE [ <string_literal> | NULL ]
```

If NULL is specified, then the fuzzy search mode is reset.

###### column_comment_string

Specifies a descriptive comment for the column.

```sql
<comment_string> ::= <string_literal>
```

Specifying COMMENT `<comment_string>` saves you from having to execute a separate COMMENT ON statement later.

##### column_constraint

Specifies a constraint on a column.

```sql
<column_constraint> ::=
 NULL
 | NOT NULL
 | { HIDDEN | NOT HIDDEN }
 | [ CONSTRAINT <constraint_name> ] { <unique_specification> |
<references_specification> }
```

###### NULL

Allows NULL values in the column. If NULL is specified it is not considered a constraint, it represents that a column may contain a null value. The default is NULL.

###### NOT NULL

Prohibits NULL values in the column.

###### HIDDEN | NOT HIDDEN

Specifies whether to hide the column; if not specified, the default behavior is NOT HIDDEN. A hidden column is excluded from a SELECT \* operation on a table. It is also excluded in an INSERT INTO..VALUES operation unless the column list specifically references it. A hidden column still appears in system views such as TABLE_COLUMNS, INDEX_VIEWS, PARTITIONS, and so on. In the TABLE_COLUMNS system view, the IS_HIDDEN column indicates whether a column is hidden. Hidden columns still appear when using smart data access and in federation with other databases.

###### unique_specification

Specifies a uniqueness constraint on a column. There are two uniqueness constraints you can set: UNIQUE and PRIMARY KEY.

```sql
<unique_specification> ::=
 UNIQUE [ <rs_tree_type_index> | <cs_inverted_type_index> ]
 | PRIMARY KEY [ <rs_tree_type_index> | <cs_inverted_type_index> ]
```

When the optional index type (`<rs_tree_type_index>` or `<cs_inverted_type_index>`) is omitted, the database server chooses the appropriate type by considering the table type and the column data type.

'rs_' and 'cs_' at the beginning of the specification types indicate which type of table the specification corresponds to (row store and column store, respectively). If you mistakenly specify a row store index type and the table is a column store table, then the specification is ignored and the index is created as INVERTED VALUE (default). If you mistakenly specify a column store index type and the table is a row store table, an error is returned.

###### UNIQUE

Specifies that the index must have unique values. The optional `<rs_tree_type_index>` specification is only applicable to row store tables.

A composite unique key enables the specification of multiple columns as a unique key. With a unique constraint, multiple rows cannot have the same value in the same column.

A UNIQUE column can contain multiple NULL values.

###### PRIMARY KEY

Specifies a primary key constraint, which is a combination of a NOT NULL constraint and a UNIQUE constraint.

###### rs_tree_type_index

Specifies the tree type for the index. Tree type specification is only applicable to row store tables.

```sql
<rs_tree_type_index> ::= { BTREE | CPBTREE }
```

###### CPBTREE

Specifies a CPB+-tree index for row store tables. CPB+-tree stands for Compressed Prefix B+-Tree, which is based on pkB-tree. CPB+-tree is a very small index because it uses 'partial key' that is only part of full key in index nodes. CPB+-tree shows better performance than B+-Tree for larger keys. Specify this type of tree for the following scenarios:

- for character string types
- for binary string types
- for decimal types
- when the constraint is a composite key
- when the constraint is a non-unique constraint

###### BTREE

Specifies a B+-tree index. B+-tree indexes maintain sorted data, which performs efficient insertion, deletion, and search of records. Specify this type of tree for scenarios not described for CPBTREE.

###### cs_inverted_type_index

Specifies the inverted index type for column store tables. Inverted index types are only applicable to column store tables.

```sql
<cs_inverted_type_index> ::= INVERTED { HASH | VALUE | INDIVIDUAL }
```

###### INVERTED HASH

INVERTED HASH should not be used as a composite type in cases where range queries or similar queries on the composite keys are a significant part of the workload. In these cases, use INVERTED VALUE instead.

###### INVERTED VALUE

INVERTED VALUE is the default index type for column store tables.

###### INVERTED INDIVIDUAL

An INVERTED INDIVIDUAL index is a lightweight index type for column store tables with reduced memory footprint. The name INVERTED INDIVIDUAL reflects that internally only inverted indexes on individual columns are created (that is, no concat attributes are created). This type of index is only available for multi-column unique constraints, which may be defined as secondary unique index or primary key.

###### references_specification

For `<references_specification>`, see References Specification [→](README.md).

#### table_constraint

The table constraint can be either a unique constraint, a referential constraint, or a check constraint.

```sql
<table_constraint> ::=
 [ CONSTRAINT <constraint_name> ]
 { <unique_constraint_definition>
  | <referential_constraint_definition>
  | <check_constraint_definition> }
```

##### unique_constraint_definition

Specifies unique constraints.

```sql
<unique_constraint_definition> ::=
 <unique_specification> ( <unique_column_name_list> )
```

##### unique_column_name_list

Specifies the unique column name list of one or more column names.

```sql
<unique_column_name_list> ::=
 <unique_column_name>[, <unique_column_name> [,…] ]
```

##### unique_column_name

Specifies a column name identifier.

```sql
<unique_column_name> ::= <identifier>
```

##### referential_constraint_definition

Specifies a referential constraint.

```sql
<referential_constraint_definition> ::=
 FOREIGN KEY ( <referencing_column_name_list> ) <references_specification>
```

To ensure uniqueness, the target of a foreign key constraint must be either a full primary key or a unique column. Self-referencing foreign key constraints are supported.

##### referencing_column_name_list

Specifies the target column(s) of the foreign key constraint.

```sql
<referencing_column_name_list> ::=
 <referencing_column_name>[, <referencing_column_name> ]
```

Specifies that a hash encodes the composite key in a condensed manner. This option allows for faster equality queries over the composite keys, [,…] Specifies that a hash encodes the composite key] in a condensed manner. This option allows for faster equality queries over the composite keys, as well as reduced memory requirements for storage of the composite key.

##### referencing_column_name

The identifier of a referencing column.

```sql
<referencing_column_name> ::= <identifier>
```

##### references_specification

Specifies the referenced table, with optional column=name list and trigger action.

```sql
<references_specification> ::=
  REFERENCES <referenced_table> [ ( <referenced_column_name_list> ) ]
  [ <referential_triggered_action> ]
  [ <constraint_enforcement> ]
  [ <constraint_check_time> ]
<constraint_check_time> ::= INITIALLY { IMMEDIATE | DEFERRED }
```

##### referenced_table

Specifies the identifier of a table to be referenced.

```sql
<referenced_table> ::= <identifier>
```

##### referenced_column_name_list

Specifies the referenced column name list, which can have one or more column names.

If `<referenced_column_name_list>` is specified, then there is a one-to-one correspondence between `<column_name>` of `<column_definition>` (see column definition [→](README.md)) and `<referenced_column_name>`. If it is not specified, then there is a one-to-one correspondence between `<column_name>` of `<column_definition>` and the column name of the referenced table's primary key.

```sql
<referenced_column_name_list> ::=
 <referenced_column_name>[, <referenced_column_name> [,…] ]
```

`<referenced_column_name>` specifies the identifier of the column name to be referenced.

##### constraint_check_time

Specifies when to check constraints. The default is INITIALLY IMMEDIATE.

- IMMEDIATE - referential constraints are checked immediately during statement execution. If a referential constraint is violated, then the statement fails.
- DEFERRED - referential constraints are checked at commit time. If a referential constraint is violated, then the transaction is rolled back. Also, if `<referential_triggered_action>` is set to something other than RESTRICT, then the referential constraint check on the parent (referencing) table is not deferred and instead is checked immediately.

##### referential_triggered_action

Specifies an update rule with an optional delete rule or a delete rule with an optional update rule. The order in which they are specified provides an order of precedence for execution.

```sql
<referential_triggered_action> ::=
 <update_rule> [ <delete_rule> ]
 | <delete_rule> [ <update_rule >]
```

##### update_rule

Specifies the update rule.

```sql
<update_rule> ::= ON UPDATE <referential_action>
<referential_action> ::=
 CASCADE
 | RESTRICT
 | SET DEFAULT
 | SET NULL
```

The following UPDATE referential actions are possible:

| **Action Name** | **Update Action** |
| --- | --- |
| RESTRICT | Any updates to a referenced table are prohibited if there are any matched records in the referencing table. This is the default action. |
| CASCADE | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with the same values. Any updates to a referenced table are prohibited if there are any matched records in the referencing table. This is the default action. |
| SET NULL | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with null values. |
| SET DEFAULT | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with their default values |

##### delete_rule

Specifies the delete rule.

```sql
<delete_rule> ::= ON DELETE <referential_action>
```

The following DELETE referential actions are possible:

| **Action Name** | **Delete Action** |
| --- | --- |
| RESTRICT | Any deletions to a referenced table are prohibited if there are any matched records in the referencing table. This is the default action. |
| CASCADE | If a record in the referenced table is deleted, then the corresponding records in the referencing table are also deleted. When you specify NOT ENFORCED, new or modified rows are not checked to determine whether they violate the foreign key constraint. If a record in the referenced table is deleted, then the corresponding records in the referencing table are also deleted. |
| SET NULL | If a record in the referenced table is deleted, then the corresponding records in the referencing table are set to null. |
| SET DEFAULT | If a record in the referenced table is deleted, then the corresponding records in the referencing table are set to their default values. |

##### check_constraint_definition

```sql
<check_constraint_definition> ::= CHECK ( <search_condition> )
```

Specifies a predicate to use as a table check constraint. A table check constraint is satisfied if `<search_condition>` evaluates to true.

##### constraint_enforcement

Enable or disable constraint enforcement and validation.

```sql
<constraint_enforcement> ::= <constraint_name> <constraint_enforcement>
<constraint_enforcement> ::= <enforcement_option>
 | <validation_option>
 | <enforcement_option> <validation_option>
<enforcement_option> ::= [NOT] ENFORCED
<validation_option> ::= [NOT] VALIDATED
```

When you specify NOT VALIDATED, existing data is not checked to determine whether it violates the foreign key constraint.

Enable or disable constraint enforcement rather than dropping and recreating the constraint.

The default `<enforcement_option>` is ENFORCED and the default `<validation_option>` is VALIDATED.

##### like_table_clause

Specifies a source table to be used for the definition.

```sql
LIKE { <like_table_name> <table_creation_syntax>
 | <like_table_name> <like_table_replica_specification> }
<table_creation_syntax> ::= [ WITH [ NO ] DATA ] [ <like_without_option> ]
```

With the exception of mask definitions, all the column definitions with constraints, default values, and other properties, such as generated columns, schema flexibility, and so on, are copied from the table `<like_table_name>`. All table constraints, indexes, fulltext indexes, and the table location are also copied. Use the ALTER TABLE statement to add mask definitions to the new table.

##### like_table_name

Specifies the table being used for source definition information.

```sql
<like_table_name> ::=
 [ [ <database_name>.]<source_schema_name>.]<source_table_name>
<source_table_name> ::= <identifier>
```

Schema name and database name are optional. `<database_name>` is only for use in a multitenant system where cross-database access is enabled for the given database name.

##### WITH [NO] DATA

Specifies that data is copied from the `<like_table_name>` table. The default value of WITH NO DATA does not copy the table data.

##### like_without_option

Specifies which properties are not copied from the `<like_table_name>` table. For example, when WITHOUT PARTITION is specified, the table is not partitioned. The WITHOUT clause

```sql
<like_without_option> ::=
 WITHOUT AUTO MERGE
 | WITHOUT HISTORY
 | WITHOUT NO LOGGING
 | WITHOUT PARTITION
 | WITHOUT SCHEMA FLEXIBILITY
 | WITHOUT UNLOAD
 | WITHOUT PRELOAD
 | WITHOUT UNLOAD PRIORITY
 | WITHOUT INDEX
 | WITHOUT FUZZY SEARCH INDEX
 | WITHOUT FUZZY SEARCH MODE
 | WITHOUT GLOBAL TEMPORARY
 | WITHOUT LOCAL TEMPORARY
 | WITHOUT CONSTRAINT
 | WITHOUT NUMA NODE
```

When you specify WITHOUT CONSTRAINT, the following restraints are not copied to the new table: PRIMARY KEY, UNIQUE, NOT NULL, CHECK constraints, and REFERENTIAL CONSTRAINT (foreign keys).

Use the WITHOUT NUMA NODE parameter to ignore NUMA NODE preferences that were set on the source table while creating the new table. If you do not include the WITHOUT NUMA NODE parameter, then SAP HANA compares the number of NUMA nodes on the target system with the number on the source system. If the number of NUMA nodes on the target system is greater than, or equal to, the number on the source system, then SAP HANA applies the node preference to the new table. If it has fewer NUMA nodes, then SAP HANA ignores the NUMA node preferences.

##### like_table_replica_specification

Creates a replica based on an existing table.

```sql
<like_table_replica_specification> ::=
 [ <sync_or_async> ] REPLICA [ ( <src_table_column_list> ) ]
 [ <replica_partition> ]
 [ AT '<replica_indexserver_host>:<replica_indexserver_port>' ]
<src_table_column_list> ::= <column_name> [, <column_name> [,...] ]
<replica_partition> ::= <partition_clause>
```

##### replica_partition

Specifies the partitions for the replicated table.

```sql
<replica_partition> ::= <partition_clause>
```

The `<replica_partition>` clause supports all partition types not using time selection. See the definition for `<partition_clause>` later in this topic.

##### as_subquery

Creates a table and fills it with the data computed by the subquery. For more information about subqueries, see the SELECT statement topic.

```sql
<as_subquery> ::= { AS ( <subquery> ) [ WITH [ NO ] DATA ] |
<with_clause> }
 [ ADD <identity_column> ]
<with_clause> :: ( WITH <alias> AS ( <subquery> AS <alias> [,... ] )
SELECT <expression> FROM <alias>
<identity_column> ::=  ( <column_name> INT GENERATED ALWAYS AS
IDENTITY( START WITH <integer> INCREMENT BY <integer> ) )
```

While both the AS `<subquery>` syntax and the `<with_clause>` syntax create a table with data in it, the AS `<subquery>` syntax copies data from the columns derived from `<subquery>`, whereas the `<with_clause>` syntax allows you to define the data to insert into the columns.

If the `<as_subquery>` clause follows a `<column_names>` clause, then the column names specified in `<column_names>` override the column names defined in `<as_subquery>`.

If the table type is a history column, global temporary [column], or local temporary [column], then the memory threshold values of LOB columns are reset to NULL to store all LOB data in memory.

##### subquery

Defines the columns for the new table, If there are constraints on column derived from `<subquery>`, only the NOT NULL constraints are copied over.

WITH DATA inserts copies of the data from the columns in `<subquery>`; this is the default. If you specify WITH NO DATA, the table is created without any data.

##### with_clause

Defines the columns for the table as well as the data to insert into them.

##### ADD identity_column

Defines an ID column to add to columns derived from `<subquery>`. ADD `<identity_column>` syntax is not supported when creating virtual tables.

#### with_annotation_clause

Specifies table-, column-, and parameter-level annotations in the form of key/value pairs. You can reference annotations in subsequent queries to filter results.

```sql
<with_annotation_clause> ::= WITH ANNOTATIONS ( { [ <set_table_annotations> ]
[ <set_column_annotations> ] [ <set_parameter_annotations> ] } )
<set_table_annotations> ::= <key_set_operation>
<set_column_annotations> ::= <column_annotation> [ <column_annotation> […] ]
<column_annotation> ::= COLUMN <column_ref> <key_set_operation>
<set_parameter_annotations> ::= <parameter_annotation>
[ <parameter_annotation> […] ]
<parameter_annotation> ::= PARAMETER <column_ref> <key_set_operation>
<key_set_operation> ::= SET <key_value_pair_list>
<key_value_pair_list> ::= <key_value_pair> [, <key_value_pair> [,…] ]
<key_value_pair> ::= '<key>'='<value>'
<column_ref> ::= <identifier>
<key> ::= <string>
<value> ::= <string>
```

While you must specify annotation on at least one object with the WITH ANNOTATION clause (table, column, or parameter), there is no limit on the number of annotations or types of annotations you can specify.

`<key>` and `<value>` represent the annotations you are configuring for the object (table, column, or parameter).

#### system_versioning_spec

Configures system versioning for a table. System-versioning allows change tracking on database tables. This is achieved by adding validity-period columns to a table, and storing change information for the table in an associated history tables (not to be confused with HANA history tables).

```sql
<system_versioning_spec> ::= { <history_table_definition> |
<system_versioned_table_definition> }
<history_table_definition> ::= (
 <column_definition> [,…] ,
 <sys_validfrom_column_name> TIMESTAMP NOT NULL,
 <sys_validto_column_name> TIMESTAMP NOT NULL
 )

<system_versioned_table_definition> ::= (
  <column_definition> [,…] ,
  <sys_validfrom_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
START,
  <sys_validto_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW END,
  PERIOD FOR SYSTEM_TIME( <sys_validfrom_column_name>,
<sys_validto_column_name> )
  [ WITH SYSTEM VERSIONING HISTORY TABLE <history_table_name> ]
  [ [ NOT ] VALIDATED ]
 )
```

##### column_definition

This is the normal data column definition as described in the `<table_elements>` description and is only being included in the `<history_table_definition>` and `<system_versioned_table_definition>` to demonstrate where to locate the system-versioning clauses relative to the overall table creation syntax.

##### sys_validfrom_column_name

In both `<history_table_definition>` and `<system_versioned_table_definition>`, this column defines the column that holds the start time of the validity period. Note that in `<system_versioned_table_definition>`, an additional option GENERATED ALWAYS AS ROW START is added. This is the mechanism by which the system automatically updates the TIMESTAMP value in the column.

##### sys_validto_column_name

In both `<history_table_definition>` and `<system_versioned_table_definition>`, this column defines the column that holds the end time of the validity period. Note that in `<system_versioned_table_definition>`, an additional option GENERATED ALWAYS AS ROW END is added. This is the mechanism by which the system automatically updates the TIMESTAMP value in the column.

##### PERIOD FOR SYSTEM_TIME ( sys_validfrom_column_name, valid_to_column_name )

Specifies the validity period columns, and is for multi-column unique constraints, which may be defined as secondary unique index or primary key.

##### WITH SYSTEM VERSIONING HISTORY TABLE history_table_name

Enables system-versioning for the table. `<history_table_name>` must already exist and not be associated with any other system-versioned table. If you create the table without this clause, system versioning is not enabled; you must subsequently execute an ALTER TABLE statement to add the clause and enable system versioning.

##### [ [ NOT ] VALIDATED ]

Specifies whether to check if `<history_table_name>` is empty. If VALIDATED is specified (the default), an exception is raised if `<history_table_name>` is not empty. If NOT VALIDATED is specified, no emptiness check is performed on `<history_table_name>`, and no exception is raised even if the history table has data in it.

#### application_time_period_spec

Creates an application-time period table. This option is only supported for column store tables.

```sql
<application_time_period_spec> ::= ( <column_definition_list>,
 <validfrom_column_name> <date_type> NOT NULL,
 <validto_column_name> <date_type> NOT NULL,
 PERIOD FOR APPLICATION_TIME ( <validfrom_column_name>,
<validto_column_name> )
)
```

##### column_definition_list

Specifies the column definition for the table. See the definition for `<column_definition>` earlier in this topic for more information about `<column_definition>`.

```sql
<column_definition_list> ::= <column_definition> [, <column_definition> [,
…] ]
```

##### validfrom_column_name and validto_column_name

Specifies the names of the columns that will hold the period start and end times.

##### datetime_type

Specifies the datetime type of `<validfrom_column_name>` and `<validto_column_name>`.

##### PERIOD FOR APPLICATION_TIME

Specifies the validity period columns. The period adds an implicit constraint that `<validfrom_column_name>` must be less than `<validto_column_name>`.

#### bi_temporal_table_spec

Creates a bi-temporal table, which is a table that has both system-versioning and an application-time period defined on it. The syntax for creating a bi-temporal table combines the syntax elements from both types of table. The following syntax block shows this combination. However, see the

`<system_versioning_spec>` and `<application_time_period_spec>` definitions in this topic for descriptions of the syntax elements.

```sql
<bi_temporal_table_spec> ::= { <bi_temporal_history_table_definition> |
<bi_temporal_system_versioned_table_definition> }
<bi_temporal_history_table_definition> ::= (
 <column_definition_list>,
 <sys_validfrom_column_name> TIMESTAMP NOT NULL,
 <sys_validto_column_name> TIMESTAMP NOT NULL,
 <validfrom_column_name> DATE NOT NULL,
 <validto_column_name> DATE NOT NULL
 )

<bi_temporal_system_versioned_table_definition> ::= (
  <column_definition_list>,
  <sys_valid_from_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
START,
  <sys_valid_to_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW END,
  <validfrom_column_name> DATE NOT NULL,
  <validto_column_name> DATE NOT NULL,
  PERIOD FOR APPLICATION_TIME ( <validfrom_column_name>,
<validto_column_name> ),
  PERIOD FOR SYSTEM_TIME ( <sys_validfrom_column_name>,
<sys_validto_column_name> ),
  PRIMARY KEY ( <column_name> [, <column_name> [,…] ] )
  [ WITH SYSTEM VERSIONING HISTORY TABLE <bi_temporal_history_table_name> ]
 )
```

#### with_association_clause

Creates a relationship between the table being created and one or more existing tables.

```sql
<with_association_clause> ::=
 WITH ASSOCIATIONS ( <association_def_list> )
<association_def_list> ::= <association_def>, ...
```

##### association_def

Specifies the association relationship, including the join cardinality and DDL statement. Associations are checked at runtime, not creation time.

```sql
<association_def> ::=
 [ <join_cardinality> ] JOIN <table_name> [ AS <identifier > ] ON
<predicate> WITH DEFAULT FILTER <predicate>
<join_cardinality> ::=
 MANY TO ONE
 | MANY TO MANY
 | ONE TO ONE
 | ONE TO MANY
<table_name> ::= <identifier>
```

Use the WITH DEFAULT FILTER clause to specify a default predicate to filter column values.

#### with_mask_clause

Adds data masking to the contents of the specified columns. Data masking transforms confidential data so that it appears meaningless to users who don't have the privileges required to view it.

```sql
<with_mask_clause> ::= WITH MASK ( <column_name> USING <mask_expression> [,
…] )
<column_name> ::= <identifier>
<mask_expression> ::= <expression>
```

Masking behavior is supported on row and column tables, and SQL row and calculation views. It is not supported on any other type of tables (virtual tables, extended tables, temporary tables etc.) and views (Join/Olap/Hierarchy views).

Only one masking behavior, definer owner-based (DEFAULT MASK) or session user based masking (SESSION USER MASK), is supported on a table or view with masked columns. You can combine both masking behaviors in an object hierarchy. For example, a view with session user based masking can be created on a table with owner-based masking.

If masking is enforced on lower-level objects, results for higher-level objects, for unauthorized users, may be incorrect because some results data is masked; no error is returned indicating lower-level objects are masked.

If not specified, DEFAULT is the default.

`<mask_expression>` can be any type of expression, including a userdefined function, that returns the same data type and length as the original column.

For more information on data masking, see the SAP HANA Cloud, SAP HANA Database Security Guide.

#### logging_option

Specifies logging options for the created table.

```sql
<logging_option> ::=
 LOGGING
 | NO LOGGING [ RETENTION <retention_period> ]
```

##### LOGGING

Activates table logging. This is the default logging option.

##### NO LOGGING

Deactivates logging. A NO LOGGING table means that the definition of the table is persistent and globally available with data that is temporary and global.

##### RETENTION

Specifies the retention time in seconds of the column table created by NO LOGGING. The table is temporary and globally available with data that is temporary and global.

```sql
RETENTION <retention_period>
<retention_period> ::= <unsigned_integer>
```

After the specified retention period elapses, the table is dropped if the used physical memory on the host is above 80%.

> **Note**
>
> A NO LOGGING retention table can also be created on an Active/Active (read enabled) secondary system.

#### auto_merge_option

Specifies that an automatic delta merge is triggered; this is the default.

```sql
<auto_merge_option> ::= [NO] AUTO MERGE
```

NO AUTO MERGE disables automatic delta merging.

#### unload_priority_clause

Specifies the priority of the table to be unloaded from memory.

```sql
<unload_priority_clause> ::= UNLOAD PRIORITY <unload_priority>
```

`<unload_priority>` is a number from 0 and 9, inclusive, where 0 means not-unloadable and 9 means earliest unload.

#### schema_flexibility_option

Specifies that the table schema is flexible. The flexibility option is available for column tables.

```sql
<schema_flexibility_option> ::=
 WITH SCHEMA FLEXIBILITY [(<flexibility_option>...)]
<flexibility_option> ::=
 RECLAIM
 | NO RECLAIM
 | DEFAULT DATA TYPE <default_data_type>
 | NO DEFAULT DATA TYPE
 | AUTO DATA TYPE PROMOTION
 | NO AUTO DATA TYPE PROMOTION
```

Dynamic columns in flexible tables allow you to implicitly add columns and change column data types with INSERT, UPDATE, and REPLACE/UPSERT operations.

Dynamic columns can be created automatically during a data insertion operation, an update operation, or a replace/upsert operation. Spatial and text data types are not available in the dynamic schema of flexible tables. The deletion of automatically created columns is done asynchronously in the background through a dedicated garbage collection mechanism.

Implicit DDL operations during DML operations are auto-committed and cannot be rolled back.

##### RECLAIM

Enables garbage collection for a flexible table. If it is enabled, then dynamic columns are automatically dropped when no values are left for all rows in the column. The garbage collection runs periodically according to the interval specified as reclaim_interval in the flexible_table section of the `indexserver.ini` file. Trigger garbage collection manually with the ALTER SYSTEM RECLAIM FLEXIBLE TABLES statement.

##### NO RECLAIM

Turns off garbage collection.

##### DEFAULT DATA TYPE

Specifies the default data type.

```sql
DEFAULT DATA TYPE {<default_data_type> | *}
```

By default an NVARCHAR with a maximum length of 5000 is chosen as the data type for new dynamic columns in flexible tables. This default behavior of a flexible table can be changed by explicitly specifying a default data type. To let the database automatically detect and choose the best matching data type, specify \* as a wildcard for the default data type.

Database automatic data type detection is only supported for constant values (expressions are not supported).

##### NO DEFAULT DATA TYPE

Explicitly forces the use of the system default for the default data type (NVARCHAR(5000)).

##### AUTO DATA TYPE PROMOTION

Alters the column type of a dynamic column to a more generic data type that is able to store the old and the new data without any loss of information when new data is inserted. Automatic data type promotion can be combined with setting a default data type.

##### NO AUTO DATA TYPE PROMOTION

Explicitly disables auto data type promotion.

#### partition_clause

For clauses for creating heterogeneous and non-heterogeneous partitions, see the topics on Non-heterogeneous Create Partition Clauses Heterogeneous Create Partition Clauses in this guide.

Non-heterogeneous Create Partition Clauses

Heterogeneous Create Partition Clauses

#### persistent_memory_spec_clause

Enables or disables persistent memory storage preference at the table, range partition, or column level, depending on where the clause is situated in the CREATE statement. For example, when specified inside the `<column_definition>` clause, it enables or disables persistent memory storage for the column.

```sql
<persistent_memory_spec_clause> ::= PERSISTENT MEMORY <pm_preference>
<pm_preference> ::= { ON | OFF }
```

#### load_unit

Specifies how to load data into memory when the table is queried. Specifying the load unit is only supported on column-store tables. `<load_unit>` can be set at column, table, and partition levels.

```sql
<load_unit> ::= { COLUMN | PAGE } LOADABLE
```

##### COLUMN LOADABLE

In-memory loading - the entire column is loaded into memory. COLUMN LOADABLE boosts performance at the cost of higher memory usage. This is the default behavior unless another value is inherited.

##### PAGE LOADABLE

Inbuffer cache loading - column data is loaded by page into the buffer cache. PAGE LOADABLE reduces memory usage for specific columns by not requiring those columns to be fully memory resident.

In the case of competing or unspecified `<load_unit>` settings, the following logic is applied.

- If there is a load unit preference specified for a column, apply that value.
- Else if there is a load unit preference specified for the parent partition, apply that value.
- Else if there is a load unit specified for the parent table, apply that value.
- Else apply the default (COLUMN LOADABLE).

#### group_option_list

Specifies the group type, subtype, and name, and whether the table is the leader of the table group.

```sql
<group_option_list> ::= <group_option> [ <group_option> ...]
<group_option> ::=
 GROUP TYPE <identifier>
 | GROUP SUBTYPE <identifier>
 | GROUP NAME <identifier> [ GROUP LEAD ]
```

GROUP LEAD sets the table as the leader of the table group it belongs to.

#### replica_clause

Creates one or more table replicas at the same time the source table is created.

To create a column-wise replica that is based on an existing table (CREATE TABLE LIKE syntax), see the `<like_table_replica_specification>` syntax in this topic.

```sql
<replica_clause> ::=
 [ <sync_or_async> ] [ <column_or_row> ] REPLICA
[ ( <src_table_column_list> ) ] [ <replica_partition> ]
 [ AT <replica_locations> ]
```

##### sync_or_async

Specifies when to activate and populate the replica. The default is SYNCHRONOUS, which means the replica is created, populated with data, and enabled when the source table is created.

```sql
<sync_or_async> ::= { SYNCHRONOUS | ASYNCHRONOUS }
```

Replicas created as ASYNCHRONOUS are created empty and disabled; you must execute an ALTER SYSTEM ENABLE ALL ASYNCHRONOUS TABLE REPLICAS statement to enable them.

##### column_or_row

Specifies whether the replica is a column or row table. If `<column_or_row>` is not specified, then the type is the same as that of the source table.

```sql
<column_or_row> ::= { COLUMN | ROW }
```

##### replica_partition

Specifies the partitions for the replicated table.

```sql
<replica_partition> ::= <partition_clause>
```

The `<replica_partition>` clause supports all partition types not using time selection. See the definition for `<partition_clause>` earlier in this topic.

##### src_table_column_list

Specifies a subset of the columns in the source table. A replica that has a subset of the columns from the source table is called a **column-wise replica**.

```sql
<src_column_list> ::= <src_column_name> [, <src_column_name> [,…] ]
```

Although you can specify the columns in any order, the order of the columns in the replica will match the order of columns in the source table.

##### AT replica_locations

Creates replicas at the specified locations.

```sql
<replica_locations> ::= AT { <indexserver_host_port> |
( <indexserver_host_port>, … )}
<indexserver_host_port> ::= '<hostname>:<port_number>'
```

If you do not specify a location, then the replica table is created based on the table placement rule. If no table placement rule is also defined, then the first replica table is created on one of slave nodes that is not the source table location.

The former syntax, `AT { ALL LOCATIONS | <num_replicas> LOCATIONS }`, is supported but deprecated. Specify locations using the AT `<replica_locations>` syntax instead.

#### location_clause

Specifies the index servers on which the partitions are created in a round-robin scheme.

```sql
<location_clause> ::= [ [ NOT ] MOVABLE ]
 AT [LOCATION] ('<hostname>:<port_number>')
```

A table can be created in the specified location with `<hostname>`:`<port_number>`. `<location_clause>` can be specified when creating partitioned tables that are distributed on multiple instances. When `<location_clause>` is provided without `<partition_clause>`, the table is created on the first location specified. If location information is not provided, then the table is automatically assigned to one node. This option can be used for both row-store and column-store tables in a distributed environment. Even if you specify a location for a global temporary table, the table is always created in the master instance.

Use the [NOT] MOVABLE clause to control whether the table can be moved to another location. When a table is set to NOT MOVABLE, it cannot be moved to another location. By default, tables are movable.

#### global_temporary_option

Sets data availability of global temporary tables within session or transaction level. Only global temporary tables can use this option.

```sql
<global_temporary_option> ::=
 <global_temporary_preserve>
 | <global_temporary_delete>
```

##### global_temporary_preserve

Causes data to remain available within a session. The data is deleted when the session is terminated.

```sql
<global_temporary_preserve> ::= ON COMMIT PRESERVE ROWS
```

PRESERVE is the default value. Therefore, global temporary tables use session data without this option.

##### global_temporary_preserve

Causes data to remain available within a transaction. The data is deleted when the transaction is committed.

```sql
<global_temporary_delete> ::= ON COMMIT DELETE ROWS
```

#### series_clause

Specifies settings for a table that contains series data.

```sql
<series_clause> ::=
 SERIES ( [<series_key>] [<series_equidistant_definition>]
[<series_minvalue>] [<series_maxvalue>]
   <series_period> [<alternate_series>] )
```

##### series_key

Defines one or more columns that uniquely identify a particular series within the table. The table stores a single series when no series key columns are defined. For series tables that do not allow duplicate entries, a PRIMARY KEY can be defined with the SERIES_KEY columns and a period column.

```sql
<series_key> ::= SERIES KEY ( <series_key_column> [ {, <series_key_column>
… } ] )
```

##### series_equidistant_definition

Specifies whether the table is equidistant.

```sql
<series_equidistant_definition> ::=
 NOT EQUIDISTANT
 | EQUIDISTANT INCREMENT BY <increment_by> [ <missing_elements> ]
```

When using an equidistant series for table partitioning, use HASH or RANGE partitioning so that records with the same series key are in the same partition.

##### increment_by

Defines the distance between adjacent elements.

```sql
<increment_by> ::= <real_const> | <datetime_const>
```

The delta is defined by an integer constant, an interval constant, or a defined number of elements between a minimum and maximum. The delta is used in the physical storage representation to optimize an equidistant series table. For numeric series, the increment_by value defines the period boundaries with respect to numeric zero (0). For example, if the increment_by is 3, then valid period boundaries include 0, 3, 6, ... Define `<Increment_by>` as a real_const or a datetime_const. It is either an integer constant, an interval constant, or a defined number of elements between a minimum and maximum, so it can be an integer or a real. If the period type is a DATETIME, then the number needs to be preceded by INTERVAL followed by a unit, such as YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND. Exponential notation is allowed.

##### missing_elements

Indicates whether missing elements are allowed.

```sql
<missing_elements> ::= MISSING ELEMENTS [ NOT ] ALLOWED
```

Equidistant series define a mapping from the series data type to elements. A series table has no missing elements when there is a single contiguous range of elements where every element has a matching row. Otherwise, the table has missing elements.

##### series_minvalue and series_maxvalue

Specifies a minimum or maximum value.

```sql
<series_minvalue> ::=
 NO MINVALUE
 | MINVALUE <datetime_literal>
<series_maxvalue> ::=
 NO MAXVALUE
 | MAXVALUE <datetime_literal>
```

For a non-equidistant series, any representable value between the minimum and maximum values is permitted. When a minimum or maximum value is specified for an equidistant series, the value must be aligned with the increment_by value with respect to the natural zero. For example, a numeric series with an increment_by value of 2 requires the minimum and maximum value to be an even number. For date/time types with an increment_by unit of DAY or smaller, the zero is considered to be midnight. For a unit of MONTH, the zero is the first day of the month, and for a unit of YEAR, the zero is the first day of the year.

```sql
<constant_literal> ::= <real_const> | <datetime_const>
<interval_const> ::= INTERVAL <integer> <unit>
<unit> ::=
 YEAR
 | MONTH
 | DAY
 | HOUR
 | MINUTE
 | SECOND
```

##### series_period

Specifies the period of validity in each row that represents the period of time that the row applies to.

```sql
<series_period> ::= PERIOD FOR SERIES <series_period_columns>
<series_period_columns> ::=
 (<series_instant_column>)
 | (<series_period_start_column>, <series_period_end_column>)
```

There is a single period column when the series table represents instants. For intervals, there can be one or two columns.

##### series_instant_column

Represents the instant in time that the single period row applies to.

```sql
<series_instant_column> ::= <identifier>
```

##### series_period_start_column and series_period_end_column

Defines an interval series table.

```sql
<series_period_start_column> ::= <identifier> | NULL
<series_period_end_column> ::= <identifier> | NULL
```

The start and end of the interval are maintained separately. For an equidistant series, INCREMENT_BY allows the user to find either end point given the other, so you can omit either start or end from the series table without loss of information. In all cases for an interval, the interval is defined with closed-open semantics.

##### alternate_series

Represents one or more columns expected to be offset from the start time by an offset that changes infrequently, such as local-time columns reflecting changes in daylight savings time.

```sql
<alternate_series> ::=
ALTERNATE PERIOD FOR SERIES (<column1> [, <column2> ...] )
```

#### unused_retention_period_option

Defines the retention period for a table or table partitions in seconds.

```sql
<unused_retention_period_option><retention_period> |
( <retention_period>, ...) }
<retention_period> ::= <unsigned_integer>
```

A single value specifies the retention period at table-level, including all of the table partitions. Multiple values specify individual retention periods for each of the table partitions. If multiple values are specified, then the number of values must match the number of table partitions.

The default value and behavior of UNUSED_RETENTION_PERIOD is 0 (inactive) seconds. To activate UNUSED_RETENTION_PERIOD, change the value to something other than 0. However, use of the UNUSED_RETENTION_PERIOD setting on a table requires that the global unused_retention_period setting in the `global.ini` configuration file be set to something other than 0.

#### record_commit_timestamp_clause

Specifies that the COMMIT timestamp of a row is tracked. If this option is enabled, then every row is associated with the COMMIT timestamp of the last transaction that performed a DML operation on the row.

```sql
<record_commit_timestamp_clause> ::= RECORD COMMIT TIMESTAMP
```

You cannot use the RECORD COMMIT TIMESTAMP clause when creating the following tables:

- Temporary tables
- Virtual tables
- Multi-store tables
- Proxy tables
- History tables
- Asynchronous/synchronous replicated tables

Synchronous replicated tables and tables created with the RECORD COMMIT TIMESTAMP clause cannot be updated together or the COMMIT operation fails.

Depending on the table type, DDL statements, such as ALTER TABLE or CREATE TABLE LIKE, can affect the value returned by the RECORD_COMMIT_TIMESTAMP() function:

- For column store tables, the returned value is zero if the result of a CREATE TABLE LIKE statement, otherwise the value is unaffected by the DDL.
- For row store tables, the returned value is changed to the COMMIT timestamp of the transaction that performed the DDL operation.

You cannot use RECORD COMMIT TIMESTAMP with keys or indexes if you are creating a row store table.

For example, the following CREATE TABLE statements cannot be executed:

```sql
CREATE ROW TABLE ROWCTS_LIMIT (X INT PRIMARY KEY) RECORD COMMIT TIMESTAMP;
CREATE ROW TABLE ROWCTS_LIMIT (X INT UNIQUE) RECORD COMMIT TIMESTAMP;
```

The following ALTER TABLE statements cannot be executed for row store tables that have been created with the RECORD COMMIT TIMESTAMP clause:

```sql
ALTER TABLE ROWCTS_LIMIT ADD (B INT PRIMARY KEY);
ALTER TABLE ROWCTS_LIMIT ALTER (X INT PRIMARY KEY);
ALTER TABLE ROWCTS_LIMIT ADD CONSTRAINT UK UNIQUE (X);
ALTER TABLE ROWCTS_LIMIT ADD (c INT UNIQUE);
ALTER TABLE ROWCTS_LIMIT ALTER (X INT CONSTRAINT X_UNIQ UNIQUE);
```

You cannot create an index on the table ROWCTS_LIMIT since it was created with the RECORD COMMIT TIMESTAMP clause.

The following statements cannot be executed if the column table ROWCTS_CS (created with RECORD COMMIT TIMESTAMP) has a primary key or unique index:

```sql
ALTER TABLE ROWCTS_CS ROW;
```

```sql
CREATE TABLE ROWCTS_RS LIKE ROWCTS_CS;
```

#### comment_string

Specifies a descriptive comment for the table.

```sql
<comment_string> ::= <string_literal>
```

Specifying COMMENT `<comment_string>` saves you from having to execute a separate COMMENT ON statement later.

#### numa_node_preference_clause

Sets the NUMA node preferences. Although this clause is defined here at the table level, `<numa_node_preference_clause>` can be set in various locations such as range partition definitions (not hash or round-robin) and column definitions, as indicated in the syntax within the topic. `<numa_node_preference_clause>` is not supported for heterogeneous partitions.

```sql
<numa_node_preference_clause> ::= NUMA NODE { ( <numa_node_index_spec> )
<numa_node_index_spec> :: = <numa_node_spec> [, <numa_node_spec> [,…]
<numa_node_spec> ::= { <single_node_spec> | <range_node_spec> }
<single_node_spec> :: =  <integer_const>
<range_node_spec> :: =  <integer_const> TO <integer_const>
```

##### integer_const

`<integer_const>` cannot be a negative number.

##### numa_node_spec

Specify one or more single NUMA nodes (`<single_node_spec>`), or one or more NUMA node ranges (`<range_node_spec>`), or a mixture of both.

NUMA node indexes should be specified in the range of 0 to one less than max_numa_node_count, where max_numa_node_count is the number of NUMA nodes configured for the system. If the NUMA node index specified is greater than or equal to max_numa_node_count, then a random NUMA node in the range of 0 to one less than max_numa_node_count is selected for allocation. For example, on a system where max_numa_node_count is set to 8, if you specify a NUMA node index of 10, then any node in the range of 0 to 7 (inclusive) is chosen randomly for allocation.

## Description

Tables are created without data except when `<as_subquery>` or `<like_table_clause>` is used with the WITH DATA option.

This statement is not for use with virtual tables. To create a virtual table, use the CREATE VIRTUAL TABLE statement.

## Examples

Create Table A that has INTEGER-type for columns A and B. Column A has a primary key constraint.

```sql
CREATE ROW TABLE A (A INT PRIMARY KEY, B INT);
```

Create table T4 with group type and name.

```sql
CREATE ROW TABLE T4 (C1 INT PRIMARY KEY, C2 DATE) GROUP TYPE group_type1 GROUP
NAME group_name1;
```

Create a history table and a column table with system versioning enabled:

```sql
CREATE COLUMN TABLE account_history (
  account_id INT,
  account_owner_id NVARCHAR(10),
  account_balance DOUBLE,
  valid_from timestamp NOT NULL,
  valid_to timestamp NOT NULL
 );
CREATE COLUMN TABLE account (
  account_id INT PRIMARY KEY,
  account_owner_id NVARCHAR(10),
  account_balance DOUBLE,
  valid_from TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW START,
  valid_to TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW END,
  PERIOD FOR SYSTEM_TIME (valid_from, valid_to)
 )
 WITH SYSTEM VERSIONING HISTORY TABLE account_history;
```

Create table T5 with identity column B that has a start value of 100 and increments by 10.

```sql
CREATE COLUMN TABLE T (A INT, B INT GENERATED ALWAYS AS IDENTITY (START WITH 100
INCREMENT BY 10));
```

Create a table `MyData` that has an NVARCHAR(10) column called My_Field, and specify a comment for both the table and the column.

```sql
CREATE COLUMN TABLE MyData ( My_Field NVARCHAR(10) COMMENT 'My data values')
COMMENT 'Table for data';
```

Create a table by querying another table and including an ID column:

```sql
CREATE TABLE BASE_TABLE (a int, b nvarchar(10));
CREATE LOCAL TEMPORARY TABLE #TARGET_TABLE (RENAME_A, RENAME_B) ADD (ID INT
GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1)) AS (SELECT * FROM
BASE_TABLE);
```

The CREATE TABLE statements in the example below create tables with names that start with “ct” and demonstrate using the WITH clause to define the columns and the data to insert:

```sql
CREATE TABLE t1(a INT, b INT, c INT);
CREATE TABLE t2(a INT, b INT, c INT);
INSERT INTO t1 VALUES(1,12,13);
INSERT INTO t2 VALUES(2,120,130);

CREATE TABLE ct1 AS (WITH alias AS (SELECT * FROM t1) SELECT * FROM alias);
CREATE TABLE ct2 AS (WITH w1 AS (SELECT * FROM t1) SELECT * FROM w1);
CREATE TABLE ct3 AS (WITH t1 AS (SELECT * FROM t2) SELECT * FROM
t1);
CREATE TABLE ct4 AS (WITH w1 AS (SELECT * FROM t2) SELECT w1.a, t2.b FROM w1,t2);
CREATE TABLE ct5 AS (WITH w1 AS (SELECT * FROM t2), w2 AS (SELECT * FROM t1
INNER JOIN t2 ON t1.a=t2.a) SELECT w1.a FROM w1,w2);
CREATE TABLE ct6 AS (WITH d AS (SELECT 1 AS val FROM dummy) SELECT val FROM d);
```

Creates a table, t1, with annotations:

```sql
CREATE COLUMN TABLE t1(c1 INT) WITH ANNOTATIONS(
    SET 't_k1' = 't_v1', 't_k2' = 't_v2'
    COLUMN c1 SET 'c_k1' = 'c_v1', 'c_k2' = 'c_v2');
```

#### Replication

Create table t1 with an asynchronous replica at indexserver seltera17:30040.

```sql
CREATE COLUMN TABLE t1(a INT) ASYNCHRONOUS REPLICA AT 'seltera17:30040';
```

Create table C1 that has the same definition as table A. Table C1 also has the same records as table A.

```sql
CREATE COLUMN TABLE C1 LIKE A WITH DATA;
```

Create table T4 with replicas in all indexservers.

```sql
CREATE ROW TABLE T4 (C1 INT PRIMARY KEY) REPLICA AT ALL LOCATIONS;
```

Create an asynchronous table replica REP_SCHEMA.TAB1 from the existing table SRC_SCHEMA.TAB1.

```sql
CREATE ROW TABLE REP_SCHEMA.TAB1 LIKE SRC_SCHEMA.TAB1 ASYNCHRONOUS REPLICA;
```

Create a table replica REP_TABLE1 with an asymmetric partitioning scheme from source table SRC_TABLE. All source columns are replicated. The partition scheme is HASH 8 and the partition key is C2.

```sql
CREATE COLUMN TABLE SRC_TABLE (C1 INT, C2 INT, C3 INT, primary key (C1, C2,
C3)) PARTITION BY HASH (C1) PARTITIONS 32;
CREATE COLUMN TABLE REP_TABLE1 LIKE SRC_TABLE REPLICA PARTITION BY HASH (C2)
PARTITIONS 8;
```

Create a replica table REP_TABLE2 with an asymmetric partitioning scheme from the source table SRC_TABLE. Only columns C1 and C3 are replicated. The partitioning scheme is RANGE and the partition key is C3.

```sql
CREATE COLUMN TABLE REP_TABLE2 LIKE SRC_TABLE REPLICA (C1, C3) PARTITION BY
RANGE (C3) (PARTITION '1' <= VALUES < '100’, PARTITION OTHERS);
```

The following statements create a source table and a column-wise replica. You can specify a name for the replica that you can reference later to query, drop, or move the replica.

```sql
/* create a source table, and then create a column-wise replica based on the
definition of the source table */
CREATE COLUMN TABLE srcSchema.srcTableName (A INT, B INT, C NVARCHAR(10), D
CHAR(1), E BIGINT, PRIMARY KEY (A));
CREATE COLUMN TABLE repSchema.repName LIKE srcSchema.srcTableName SYNCHRONOUS
REPLICA (A, C, D);
```

Create table H1 that has the same definition as table H. Table H1 also has the same records as table H. You create a column table H2 from the definition of table H without the history property and without any records.

```sql
CREATE HISTORY COLUMN TABLE H (A INT);
 CREATE ROW TABLE H1 LIKE H WITH DATA;
 CREATE ROW TABLE H2 LIKE H WITH NO DATA WITHOUT HISTORY;
```

#### Non-heterogeneous Partitioning

Create a non-heterogeneous range partitioned table named P1 that has a -type column A. Column U has a primary key constraint and is used as a range-partitioning column.

```sql
CREATE COLUMN TABLE P1 (A  PRIMARY KEY)
   PARTITION BY RANGE (A)
      (PARTITION '2010-02-03' <= VALUES < '2011-01-01', PARTITION VALUE =
'2011-05-01');
```

Create a non-heterogeneous hash partitioned table named P2 that has INTEGER-type column I, J and K. Columns I and J make the primary key constraint and are used as hash-partitioning columns.

```sql
CREATE COLUMN TABLE P2 (I INT, J INT, K INT, PRIMARY KEY(I, J))
   PARTITION BY HASH (I, J) PARTITIONS 2;
```

Create a non-heterogeneous hash-hash partitioned table named P3 that has INTEGER-type column I, J and K. Columns I and J make the primary key constraint and are used as hash-partitioning columns. Column K is used as a subpartitioning column.

```sql
CREATE COLUMN TABLE P3 (I INT, J INT, K INT, PRIMARY KEY(I, J))
   PARTITION BY HASH (I, J) PARTITIONS 2, HASH (K) PARTITIONS 2;
```

Create a non-heterogeneous range-range partitioned table named P4. The OTHERS partition is defined on the first level. PERSISTENT MEMORY is enabled for all partitions. The NUMA node preference is set on the first partition only.

```sql
CREATE COLUMN TABLE P4 (A INT, B INT)
   PARTITION BY RANGE (A)
      (PARTITION 10 <= VALUES < 20 PERSISTENT MEMORY ON NUMA NODE ('3'),
PARTITION OTHERS PERSISTENT MEMORY ON),
   RANGE (B) (PARTITION VALUES=100 PERSISTENT MEMORY ON;
```

Create a non-heterogeneous range-range partitioned table named P5 with dynamic range partitioning enabled.

```sql
CREATE COLUMN TABLE P5 (A INT, B INT NOT NULL) PARTITION BY RANGE (A)
(PARTITION VALUES = 10),
   RANGE (B) (PARTITION VALUES = 20, PARTITION OTHERS DYNAMIC THRESHOLD 2);
```

Create a non-heterogeneous range partitioned table named P6 using time selection partitioning.

```sql
CREATE COLUMN TABLE P6 (A INT, B INT PRIMARY KEY, _DATAAGING NVARCHAR(8))
   PARTITION BY RANGE (_DATAAGING)
      (USING DEFAULT STORAGE (PARTITION value = '00000000' IS CURRENT,
         PARTITION '20100101' <= VALUES < '20110101', PARTITION OTHERS))
   WITH PARTITIONING ON ANY COLUMNS ON
   FOR NON CURRENT PARTITIONS UNIQUE CONSTRAINTS OFF
   FOR DEFAULT STORAGE NON CURRENT PARTITIONS PAGE LOADABLE;
```

#### Heterogeneous Partitioning

Create a single level range partitioned heterogeneous table. This table has no subpartitions defined.

```sql
CREATE COLUMN TABLE A1 (I INT, J INT, K INT, PRIMARY KEY(I, J))
   PARTITION BY RANGE (I) ((PARTITION 10 <= VALUES < 20, PARTITION 20 <=
VALUES < 30) );
```

Create a multi-level range-range partitioned heterogeneous table.

```sql
CREATE COLUMN TABLE A2 (I INT, J INT, K INT, PRIMARY KEY(I, J))
   PARTITION BY RANGE (I) ((PARTITION 10 <= VALUES < 20, PARTITION 20 <=
VALUES < 30)
      SUBPARTITION BY RANGE (J) (PARTITION 100 <= VALUES < 150, PARTITION
VALUE = 200) );
```

Create a heterogeneous multi-level partitioned table. The table has three firstlevel partitions. The first partition has the ranges 10-20 and 20-30. The second partition has the target value 40. The final partition is OTHERS for any values outside the scope of the first to partitions. The first two partitions each have a subpartition defined. Each range or target value of the firstlevel partitions has its own properties defined. The two subpartitions are same type (range) and reference the same column (B). The subpartitions also have dynamic range partitioning enabled.

```sql
CREATE COLUMN TABLE A3 (A INT, B INT NOT NULL, C INT) PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20 GROUP NAME 'GRP 1' INSERT OFF, PARTITION 20
<= VALUES < 30 GROUP NAME 'GRP 1' INSERT OFF)
      SUBPARTITION BY RANGE(B) (PARTITION 0 <= VALUES < 10 PAGE LOADABLE
GROUP SUBTYPE 'GRP 1a', PARTITION 10 <= VALUES <
           100 GROUP SUBTYPE 'GRP 1b' INSERT OFF PAGE LOADABLE, PARTITION
OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION VALUES = 40 GROUP NAME 'GRP 2' INSERT OFF COLUMN LOADABLE)
      SUBPARTITION BY RANGE(B) (PARTITION 0 <= VALUES < 10 GROUP SUBTYPE 'GRP
2a', PARTITION OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION OTHERS));
```

Create a heterogeneous partitioned table with dynamic range partitioning enabled. This table has two first level ranges. The first partition has a range of 10-20. The second partition has a target value of 30. Each partition has it own subpartition. The first subpartition has a range of 100-150. The second subpartition has a target value of 200. Both subpartitions have dynamic range partitioning enabled with a threshold of 3.

```sql
CREATE COLUMN TABLE T4 (A INT, B INT NOT NULL) PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20) SUBPARTITION BY RANGE (B) (PARTITION 100 <=
VALUES < 150, PARTITION OTHERS DYNAMIC THRESHOLD 3 ),
    (PARTITION VALUES = 30) SUBPARTITION BY RANGE (B) (PARTITION VALUES =
200, PARTITION OTHERS DYNAMIC THRESHOLD 3));
```

Create a heterogeneous partitioned table. There are three firstlevel (10-20, 30, and 40-50), each with different properties defined. The first two partitions share the same subpartition. There are two second-level hash partitions, each referencing the same group of columns (A, C). On the first subpartition, column A has a DATE data type, with the precision YEAR applied at the subpartition level.

```sql
CREATE COLUMN TABLE A5 (A DATE, B INT, C INT) PARTITION BY RANGE (B)
   ((PARTITION 10 <= VALUES < 20 INSERT ON PAGE LOADABLE, PARTITION VALUES =
30 COLUMN LOADABLE GROUP NAME 'HR')
       SUBPARTITION BY HASH (YEAR(a), c) PARTITIONS 4,
    (PARTITION 40 <= VALUES < 50 PAGE LOADABLE GROUP NAME 'HR')
       SUBPARTITION BY HASH (YEAR(a), c) PARTITIONS 4);
```

#### Data masking

Create a table that masks the data in the SSN column:

```sql
CREATE ROW TABLE PERSONAL_INFO (SSN VARCHAR(20)) WITH MASK (SSN USING '****');
```

#### Constraints

Create table C2 that has the same column data types and NOT NULL constraints as table A without any data.

```sql
CREATE ROW TABLE C2 AS (SELECT * FROM A) WITH NO DATA;
```

Create table F that has a foreign key that references column A of table R with update cascade option.

```sql
CREATE ROW TABLE R (A INT PRIMARY KEY, B NVARCHAR(10));
 CREATE ROW TABLE F (FK INT, B NVARCHAR(10), FOREIGN KEY(FK) REFERENCES R ON
UPDATE CASCADE);
```

Create a self-referencing foreign key.

```sql
CREATE ROW TABLE SELF(A INTEGER PRIMARY KEY, B INTEGER);
ALTER TABLE SELF ADD CONSTRAINT FK_T1 FOREIGN KEY(B) REFERENCES SELF(A);
```

Create a cyclic foreign key.

```sql
CREATE ROW TABLE GRAND_PARENT (A INT, I INT, B INT, PRIMARY KEY (A) );
CREATE ROW TABLE PARENT (A INT, I INT, B INT, PRIMARY KEY (A) );
ALTER TABLE PARENT ADD CONSTRAINT FK_CONSTRAINT_FROM_PARENT_TO_GRAND_PARENT
FOREIGN KEY (B) REFERENCES GRAND_PARENT (A) ON DELETE CASCADE;
ALTER TABLE GRAND_PARENT ADD CONSTRAINT
FK_CONSTRAINT_FROM_GRAND_PARENT_TO_PARENT FOREIGN KEY (B) REFERENCES PARENT
(A) ON DELETE CASCADE;
```

#### Schema flexibility

Create a flexible table, T.

```sql
CREATE COLUMN TABLE T(A INT) WITH SCHEMA FLEXIBILITY;
```

#### Fuzzy searching

Create table T2 with a fuzzy search index and a fuzzy search mode.

```sql
CREATE COLUMN TABLE T2 (KEY INT, COL1 VARCHAR(10) FUZZY SEARCH INDEX ON, COL2
NVARCHAR(10) FUZZY SEARCH MODE 'POSTCODE');
```

#### Temporary tables

Create a session-level global temporary table.

```sql
CREATE GLOBAL TEMPORARY TABLE T (C1 INT, C2 INT) ON COMMIT PRESERVE ROWS;
```

Create a transaction-level global temporary table.

```sql
CREATE GLOBAL TEMPORARY TABLE T (C1 INT, C2 INT) ON COMMIT DELETE ROWS;
```

Create a session-level global temporary table.

```sql
CREATE GLOBAL TEMPORARY TABLE T (C1 INT, C2 INT) ON COMMIT PRESERVE ROWS;
```

Create transaction-level global temporary table.

```sql
CREATE GLOBAL TEMPORARY TABLE T (C1 INT, C2 INT) ON COMMIT DELETE ROWS;
```

#### Series

Create a non-equidistant series that records stock market trade price and volume for one year.

```sql
CREATE COLUMN TABLE ExampleStockTrades(
     ticker_symbol VARCHAR(5),
     trade_time TIMESTAMP,
     price DECIMAL(10,2),
     volume INTEGER)
     SERIES(SERIES KEY(ticker_symbol) NOT EQUIDISTANT
         MINVALUE '2013-01-01'
         MAXVALUE '2014-01-01'
         PERIOD FOR SERIES(trade_time));
```

Create an equidistant series that covers one day intervals over a ten year period. The example table stores maximum and minimum temperatures for each day for a number of cities (identified by city_id).

```sql
CREATE COLUMN TABLE ExampleCityTemperature(
     city_id INTEGER,
     day_start TIMESTAMP,
     day_end TIMESTAMP,
     min_temperature DECIMAL(5,2),
     max_temperature DECIMAL(5,2))
     SERIES(SERIES KEY(city_id) EQUIDISTANT INCREMENT BY INTERVAL 1 DAY
         MINVALUE '2010-01-01'
         MAXVALUE '2020-01-01'
         PERIOD FOR SERIES (day_start, day_end));
```

#### Arrays

Create a new column table with an ARRAY column.

```sql
CREATE COLUMN TABLE T1 ( ID INT PRIMARY KEY, C1 INT ARRAY );
```

```sql
CREATE COLUMN TABLE T2 ( ID INT PRIMARY KEY, C1 INT ARRAY (1, 10) );
```

Create a new column table with an ARRAY column that restricts the maximum number(10) of elements.

```sql
CREATE COLUMN TABLE T3 ( ID INT PRIMARY KEY, C1 INT ARRAY (10) );
```

Create a new column table with an ARRAY column that restricts the minimum number(1) of elements.

```sql
CREATE COLUMN TABLE T4 ( ID INT PRIMARY KEY, C1 INT ARRAY (1, *) );
```

Create a new column table with an ARRAY column that doesn't allow duplicates of non-NULL values.

```sql
CREATE COLUMN TABLE T5 ( ID INT PRIMARY KEY, C1 INT ARRAY (1, 5) WITHOUT
DUPLICATES );
```

Create a new column table with an ARRAY column that has a default value.

```sql
CREATE COLUMN TABLE T6 ( ID INT PRIMARY KEY, C1 INT ARRAY DEFAULT ARRAY() );
```

#### Client-side encryption

Create a table, T7, with a column, Name, that is encrypted using the column encryption key myCEK.

```sql
CREATE ROW TABLE T7 (
 ID INT PRIMARY KEY,
 Name NVARCHAR(32) CLIENTSIDE ENCRYPTION ON WITH myCEK RANDOM);
```

#### Persistent memory

Create a table with PERSISTENT MEMORY enabled at the table level:

```sql
CREATE COLUMN TABLE myTable1 (C1 INT, C2 VARCHAR (10)) PERSISTENT MEMORY ON;
```

Create a table with PERSISTENT MEMORY enabled for the specified range partitions:

```sql
CREATE COLUMN TABLE myTable2 (C1 INT) PARTITION BY RANGE (C1) (PARTITION '0'
<= VALUES < '10' PERSISTENT MEMORY ON, PARTITION OTHERS PERSISTENT MEMORY
OFF);
```

Create a table with PERSISTENT MEMORY enabled for the specified columns:

```sql
CREATE COLUMN TABLE PMTABLE (C1 INT PERSISTENT MEMORY ON, C2 VARCHAR (10), C3
INT PERSISTENT MEMORY OFF);
```

#### NUMA node preferences examples

Creates a column table with its NUMA-node preference set at the table level on NUMA node indexes 1, 3-5. Table T1 and all its data are allocated with a preferred NUMA allocation type on NUMA node index 1. If node 1 has an insufficient amount of memory, then SAP HANA uses the node index from the range 3-5 with the shortest distance to node 1. The preferred list of NUMA node indexes is updated in the catalog when the table is created:

```sql
CREATE COLUMN TABLE T1(colint INT, colvarchar VARCHAR(10)) NUMA NODE ('1',
'3' TO '5');
```

Creates a column table with its NUMA-node preference set for a partition on node index 2, and with the partition data allocated on NUMA node index 2. Data that does not belong to this partition is allocated on the node determined by the current HASH scheme available in the attribute engine:

```sql
CREATE COLUMN TABLE T1(colint INT, colvarchar VARCHAR(10)) PARTITION BY RANGE
(colint) (PARTITION '0' <= VALUES < '20' NUMA NODE ('2'))
```

Creates a column table with its NUMA-node preference set for an integer column on node index 3, and with the data for this column allocated to node 3. Columns that do not have their NUMA node preference set inherit their preference from the table- or partition-level settings, if any partitions are set on that column. Otherwise, data is allocated with the current HASH scheme that is avail

```sql
CREATE COLUMN TABLE T1(colint INT NUMA NODE(3), colvarchar VARCHAR(10)) NUMA
NODE ('5');
```

able in the attribute engine. The column colvarchar inherits NUMA node preference from the table-level settings (in this example, node index 5):

Creates table T1 with a configuration that is similar to existing table T2, which has a NUMA NODE preference for node index 3:

```sql
CREATE COLUMN TABLE T1 LIKE T2;
```

Creates table T1 with a configuration that is similar to existing table T2 but does not include a NUMA node, so NUMA NODE preferences are not be created on T1:

```sql
CREATE COLUMN TABLE T1 LIKE T2 WITHOUT NUMA NODE;
```

#### LOAD UNIT examples

Create a table, T, that is page loadable:

```sql
CREATE COLUMN TABLE T (C1 INT, C2 VARCHAR (10)) PAGE LOADABLE;
```

#### WITH ASSOCIATION

These examples demonstrate the creation of a table with associations to other tables.

Execute the following statements to create and populate a table called t1:

```sql
CREATE TABLE t1(x1 INT, y1 INT);
INSERT INTO t1 VALUES(0, 0);
INSERT INTO t1 VALUES(1, 1);
INSERT INTO t1 VALUES(2, 2);
INSERT INTO t1 VALUES(3, 3);
```

Next, create and populate table t2 and set up an association from t2 to t1 and use the WITH DEFAULT FILTER clause to set the predicate filter to y1< 3:

```sql
CREATE TABLE t2(x2 INT, y2 INT) WITH ASSOCIATIONS
(JOIN t1 AS a ON a.x1 = x2 WITH DEFAULT FILTER y1 < 3);
INSERT INTO t2 VALUES(2, 0);
INSERT INTO t2 VALUES(3, -1);
INSERT INTO t2 VALUES(4, -2);
INSERT INTO t2 VALUES(5, -3);
```

Now, the following two statements return the same result (2, 2), as we have set the default predicate filter to y1<3:

```sql
SELECT * FROM t2:1;
SELECT * FROM t2:a[y1<3];
```

However, if you run the following statement, the result is (3, 3), as the specified filter overrides the default:

```sql
SELECT * FROM t2:a[y1>1];
```

Similarly, the following two statements return the same result, (2; None; None; None):

```sql
SELECT a.x1 FROM t2;
SELECT a[y1<3].x1 FROM t2;
```

However, the following statement overrides the default filter and returns (2; 3; None; None):

```sql
SELECT a[y1>1].x1 FROM t2;
```

Execute the following statements to create and populate table t1:

```sql
CREATE TABLE t1(x1 INT, y1 INT);
INSERT INTO t1 VALUES(0, 0);
INSERT INTO t1 VALUES(1, 1);
INSERT INTO t1 VALUES(2, 2);
INSERT INTO t1 VALUES(3, 3);
```

Execute the following statements to create and populate table t2 with associations to table t1 and with the default filter set to filter column values to values less than 3:

```sql
CREATE TABLE t2(x2 INT, y2 INT) WITH ASSOCIATIONS (JOIN t1 AS a ON a.x1 = x2
WITH DEFAULT FILTER y1 < 3);
INSERT INTO t2 VALUES(2, 0);
INSERT INTO t2 VALUES(3, -1);
INSERT INTO t2 VALUES(4, -2);
INSERT INTO t2 VALUES(5, -3);
```

Now, executing `SELECT * FROM t2:a;` returns the following:

```sql
2,2
```

However, executing `SELECT * FROM t2:a[y1>1];` overrides the default filter to return the following values:

```sql
2,2
3,3
```

If you execute `SELECT a.x1 FROM t2;`, the following values are returned:

```sql
2,
--None
--None
--None
```

Executing `SELECT a[y1>1].x1 FROM t2;` returns the following values:

```sql
2,
3,
--None
--None
```

## Related Information

Non-heterogeneous Create Partition Clauses [→](4.10.01.68.01-Non-heterogeneous-Create-Partition-Clauses.md) Heterogeneous Create Partition Clauses [→](4.10.01.68.02-Heterogeneous-Create-Partition-Clauses.md) CREATE SEQUENCE Statement (Data Definition) [→](../CREATE-SEQUENCE-Statement-Data-Definition.md) SELECT Statement (Data Manipulation) [→](../4.10.01.144-SELECT/README.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER TABLE Statement (Data Definition) [→](../4.10.01.20-ALTER-TABLE/README.md) ALTER TABLE Statement (Multistore Table) [Dynamic Tiering] [→](../../../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/ALTER-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md) CREATE VIRTUAL TABLE Statement (Data Definition) [→](../CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) Introduction to SQL [→](../../../4.01-Introduction-to-SQL.md) Predicates [→](../../../4.07-Predicates/README.md) HISTORY COLUMN Option (Time Travel) [→](4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md) CREATE REMOTE SOURCE Statement (Access Control) [→](../CREATE-REMOTE-SOURCE-Statement-Access-Control.md) ALTER SYSTEM RECLAIM FLEXIBLE TABLES Statement (System Management) [→](../4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-FLEXIBLE-TABLES-Statement-System.md) Data Types [→](../../../4.03-Data-Types/README.md)

TABLES System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) Multi-valued Data Types [→](../../../4.03-Data-Types/4.03.07-Multi-valued-Data-Types.md)

## Contenido de esta sección

- [4.10.1.68.1 Non-heterogeneous Create Partition Clauses](4.10.01.68.01-Non-heterogeneous-Create-Partition-Clauses.md)
- [4.10.1.68.2 Heterogeneous Create Partition Clauses](4.10.01.68.02-Heterogeneous-Create-Partition-Clauses.md)
- [4.10.1.68.3 HISTORY COLUMN Option (Time Travel)](4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md)
