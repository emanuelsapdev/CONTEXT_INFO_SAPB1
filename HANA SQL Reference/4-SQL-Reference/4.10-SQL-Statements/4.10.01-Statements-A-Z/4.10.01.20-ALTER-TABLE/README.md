# 4.10.1.20 ALTER TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 563–601

Alters a base or temporary table. See the ALTER VIRTUAL TABLE statement for altering virtual tables.

## Syntax

```sql
ALTER TABLE <table_name>
   [<column_clauses>]
   [<system_versioning_configuration>]
   [<add_drop_application_time_period>]
   [<lob_reorganize_clause>]
   [<clear_column_join_data_statistics_clause>]
   [<constraint_clause>]
   [<primary_key_clauses>]
   [<preload_clause>]
   [<table_conversion_clause>]
   [<association_clauses>]
   [<with_annotation_clause>]
   [<partition_clauses>]
   [<load_unit>]
   [<alter_persistent_memory_spec_clause>]
[<replica_clauses>]
[<redo_log_option>]
[<auto_merge_option>]
[<unload_priority>]
[<schema_flexibility_option>]
[<trigger_option>]
[<group_option_clauses>]
[<row_order_clauses>]
[<unused_retention_period>]
[<reclaim_data_space_clause>]
[<series_reorganize_clause>]
[<owner_to_clause>]
[<alter_mask_settings_clause>]
[<clientside_encryption_clauses>]
[<set_movable_clause>]
[<convert_index_type>]
[<numa_node_preference_clause>]
```

## Syntax Elements

#### table_name

Specifies the identifier of the table to be altered, with optional schema name.

```sql
<table_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

#### column_clauses

Defines the column operations you can perform.

```sql
[<add_columns_clause>]
[<alter_columns_clause>]
[<drop_columns_clause>]
```

##### add_columns_clause

Adds one or more columns to the specified table.

```sql
<add_columns_clause> ::= ADD ( <column_list > )
<column_list> ::= <column_specification> [, <column_specification>
[,...] ] [ ONLINE [ PREFERRED ] ]
<column_specification> ::=
 <column_name> { [ <column_definition> ] [ <column_constraint_short> ]
[ COMMENT <string_literal> ] }
     CLIENTSIDE ENCRYPTION ON WITH <column_encryption_key_name> [ RANDOM |
DETERMINISTIC ] [ <column_load_unit> ]
<column_load_unit> ::= <column_name> <load_unit>
```

###### column_definition

Specifies a definition for a column.

```sql
<column_definition> ::=
 [ { <data_type> | <lob_data_type> } <ddic_data_type> ]
 [ <default_value_clause> ]
 [ <col_gen_as_expression> | <col_gen_as_ident> ]
 [ <col_calculated_field> ]
 [ <schema_flexibility> ]
 [ <fuzzy_search_index> ]
 [ <fuzzy_search_mode> ]
[ <alter_persistent_memory_spec_clause> ]
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
 | TEXT
 | BINTEXT
 | VARCHAR [ (<unsigned_integer>) ]
 | NVARCHAR [ (<unsigned_integer>) ]
 | ALPHANUM [ (<unsigned_integer>) ]
| SHORTTEXT [ (<unsigned_integer>) ]
 | VARBINARY [ (<unsigned_integer>) ]
 | DECIMAL [ (<unsigned_integer> [, <unsigned_integer> ] ) ]
 | FLOAT [ (<unsigned_integer>) ]
 | BOOLEAN
```

For tables with time-selection partitioning, the data type for the time-selection column must be NVARCHAR(8).

###### lob_data_type

Specifies a LOB data type.

```sql
<lob_data_type> ::=
<lob_type_name> [MEMORY THRESHOLD <memory_threshold_value>]
<lob_type_name> ::=
 BLOB
 | CLOB
 | NCLOB
```

`<memory_threshold_value>` controls whether LOB data should be stored in memory, according to the following conditions:

- If `<memory_threshold_value>` is not provided, then a hybrid LOB with a memory threshold of 1000 bytes is created by default.
- If `<memory_threshold_value>` is provided and its LOB size is bigger than the memory threshold value, then LOB data is stored on disk.
- If `<memory_threshold_value>` is provided and its LOB size is equal or less than the memory threshold value, then LOB data is stored in memory.
- If `<memory_threshold_value>` is NULL, then all LOB data is stored in memory.
- If `<memory_threshold_value>` is 0, then all LOB data is stored on disk.

###### ddic_data_type

Specifies a DDIC data type.

```sql
<ddic_data_type> ::=
 DDIC_ACCP | DDIC_ALNM | DDIC_CHAR | DDIC_CDAY | DDIC_CLNT |
DDIC_CUKY | DDIC_CURR | DDIC_D16D
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

###### default_value_clause

Specifies a value to be assigned to the column if an INSERT statement does not provide a value for the column.

```sql
<default_value_clause> ::= DEFAULT <default_value_exp>
<default_value_exp> ::=
 NULL
 | <string_literal><signed_numeric_literal>
 | <unsigned_numeric_literal>
 | <datetime_value_function>
 | <string_value_function>
<datetime_value_function> ::=
CURRENT_DATE
 | CURRENT_TIME
 | CURRENT_TIMESTAMP
 | CURRENT_UTCDATE
 | CURRENT_UTCTIME
 | CURRENT_UTCTIMESTAMP
<string_value_function> ::=
 SYSUUID
 | CURRENT_USER
 | CURRENT_SCHEMA
 | SESSION_USER
```

###### col_gen_as_expression

Specifies the expression to generate the column value in runtime.

```sql
<col_gen_as_expression> ::= GENERATED ALWAYS AS <expression>
```

Generated columns are only supported in column store table definitions, and can only reference base columns that are defined prior to them in the DDL statement (that is, to the left of them). You cannot define a default for a generated column, and they cannot be used as part of a primary key or unique constraint. `<expression>` must not contain a non-deterministic function.

You cannot drop a base column that is referenced by a generated column, and you

###### col_gen_as_ident

Specifies an identity column. Only one identity column is allowed per table

```sql
<col_gen_as_ident> ::= GENERATED { ALWAYS | BY DEFAULT } AS IDENTITY
[(<sequence_option>)]
<sequence_option> ::= {
   <sequence_param_list>
   | RESET BY <subquery>
   | <sequence_param_list>
   RESET BY <subquery> }
<sequence_param_list> ::= <sequence_parameter> [,
<sequence_parameter> ] [,...]
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
RESET BY <subquery>
```

There are two types of IDENTITY columns: GENERATED ALWAYS, and GENERATED BY DEFAULT:

###### GENERATED ALWAYS

A GENERATED ALWAYS AS IDENTITY column increments based solely on the sequence parameter settings (`<sequence_param_list>`). With the exception of changes to the RESET BY definition, the sequence defined for a GENERATED ALWAYS IDENTITY column cannot be altered or reset after it has been set, and inserting a value into a GENERATED ALWAYS identity column fails and returns an error.

###### GENERATED BY DEFAULT

A GENERATED BY DEFAULT IDENTITY column increments using the sequence parameter settings (`<sequence_param_list>`) only when no identity value is specified in the INSERT statement (that is, the identity column is left out of the insert column list). When a value is specified for the identity column during the INSERT, then the specified value is inserted (assuming the value does not already exist) and the following behavior occurs with respect to the value of the identity column:

- If the specified value is higher than the existing identify value with a positive increment, then this resets the current sequence value to an allowable sequence value that is equal to the specified value, or the next one lower than the specified value.
- If the specified value is lower than the existing value with a negative increment, then this resets the current sequence value to an allowable sequence value that is equal to the specified value, or the next one higher than the specified value.
- Otherwise, the current sequence value is not reset.

Identity columns are supported in global and local temporary tables, both for row store and column store tables. They can be added to, or dropped from, a table. However, they cannot be altered.

If RESET BY `<subquery>` is specified, then during the restart of the database, the database automatically executes the subquery and restarts the sequence value with the returned value. If RESET BY is not specified, then the sequence value is stored persistently in database. During the restart of the database, the next value of the sequence is generated from the saved sequence value.

For more information on subqueries, see the SELECT statement.

For more information on sequences and sequence parameters, see the CREATE SEQUENCE statement.

###### col_calculated_field

Specifies the expression that replaces the column at query compilation time.

```sql
<col_calculated_field> ::= AS <expression>
```

The data type of a calculated field column can be a default value. Also, calculated field columns can reference base columns and other calculated field columns.

The maximum value of a recursive calculated field is 16.

Dropping or altering the base columns of a calculated field is not possible.

###### schema_flexibility

Specifies whether the column is dynamic.

```sql
<schema_flexibility> ::= { ENABLE | DISABLE } SCHEMA FLEXIBILITY
```

ENABLE changes the column into a dynamic column. DISABLE (default value) changes the column into a static column.

###### fuzzy_search_index

Turns a fuzzy search index on or off. OFF is the default.

```sql
<fuzzy_search_index> ::= FUZZY SEARCH INDEX [ON | OFF]
```

###### fuzzy_search_mode

Sets the fuzzy search mode with the value of `<string_literal>`. If NULL is specified, then the fuzzy search mode is reset.

```sql
<fuzzy_search_mode> ::= FUZZY SEARCH MODE [ <string_literal> | NULL ]
```

###### column_constraint_short

The description of the syntax for `<column_constraint_short>` and `<column_constraint>` are the same except that `<column_constraint_short>` does not include syntax for specifying `<unique_specification>`, and is used specifically when adding a column (`<add_columns_clause>`).

```sql
<column_constraint_short> ::=
 NULL
 | NOT NULL
 | [<constraint_name_definition>] <references_specification>
```

###### column_constraint

Specifies constraints on a column.

```sql
<column_constraint> ::=
 NULL
 | NOT NULL
 | { HIDDEN | NOT HIDDEN }
 | [ CONSTRAINT <constraint_name> ] { <unique_specification> |
<references_specification> }
```

###### NULL

Allows NULL values in the column. If NULL is specified it is not considered a constraint, it represents that a column that may contain a null value. The default is NULL.

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
<cs_inverted_type_index> ::= INVERTED { HASH | VALUE |
INDIVIDUAL }
```

###### INVERTED HASH

INVERTED HASH should not be used as a composite type in cases where range queries or similar queries on the composite keys are a significant part of the workload. In these cases, use INVERTED VALUE instead.

###### INVERTED VALUE

INVERTED VALUE is the default index type for column store tables.

###### INVERTED INDIVIDUAL

An INVERTED INDIVIDUAL index is a lightweight index type for column store tables with reduced memory footprint. The name INVERTED INDIVIDUAL reflects that internally only inverted indexes on individual columns are created (that is, no concat attributes are created). This type of index is only available for multi-column unique constraints, which may be defined as secondary unique index or primary key.

###### references_specification

For `<references_specification>`, see References Specification [→](README.md).

##### alter_columns_clause

Alters one or more column definitions.

```sql
<alter_columns_clause> ::= ALTER { <column_list > | <column_load_unit> }
<column_list> ::= ( <column_specification> [, <column_specification>
[,...] ] ) [ ONLINE [ PREFERRED ] ]
<column_specification> ::=
 <column_name> { [ <column_definition> ] [ <column_constraint> ] [ COMMENT
<string_literal> ] }
<column_load_unit> ::= ( <column_name> ALTER <load_unit> [ , <column_name>
ALTER <load_unit> [,...] ] )
```

###### ONLINE [ PREFERRED ]

Allows alter column operations that do not serialize with concurrent DML operations. ONLINE is only supported for column-store, non-replicated tables when altering a column to a LOB type without adding a NOT NULL constraint, or when altering only the default value and/or the nullability of a column. Altering a column in a supported case results in an alter column operation that only acquires a shared table lock. The operation is not serialized with concurrent DML operations, but is serialized with any other concurrent DDL on the table, including other ONLINE DDL. The default value must be a constant value and not a function.

When PREFERRED is specified, if ONLINE execution is not supported, then a SQL warning message appears, and the alter operation executes in table x-lock mode.

##### drop_columns_clause

Removes one or more columns from the specified table.

```sql
<drop_columns_clause> ::= DROP ( <column_name> [, ...] ) [ ONLINE
[ PREFERRED ] ]
```

###### ONLINE [ PREFERRED ]

Allows drop column operations that do not serialize with concurrent DML operations. ONLINE is only supported for column-store, non-replicated tables when dropping a non-paged column to a LOB type.

When PREFERRED is specified, if ONLINE execution is not supported, then a SQL warning message appears, and the drop operation executes in table x-lock mode.

#### with_annotation_clause

Alters table-, column-, and parameter-level annotations. You can reference annotations in subsequent queries to filter results.

```sql
<with_annotation_clause> ::=
 WITH ANNOTATIONS ( { [ <alter_table_annotations> ]
[ <alter_column_annotations> ] [ <alter_parameter_annotations> ] } )
<alter_table_annotations> ::= { [ <key_set_operation> ]
[ <key_unset_operation> ] } ]
<alter_column_annotations> ::= <column_annotation> [ <]column_annotation>
[…] ]
<column_annotation> ::= COLUMN <column_ref> { <key_set_operation> |
<key_unset_operation> }
<alter_parameter_annotations> ::= <parameter_annotation>
[ <parameter_annotation> […] ]
<parameter_annotation> ::= PARAMETER <column_ref> { <key_set_operation> |
<key_unset_operation> }
<key_set_operation> ::= SET <key_value_pair_list>
<key_unset_operation> ::= UNSET <key_list>
<key_value_pair_list> ::= <key_value_pair> [, <key_value_pair> [,…] ]
<key_value_pair> ::= '<key>'='<value>'
<key_list> ::= { '<key>'[,'<key>'[,…]] | ALL }
<column_ref> ::= <identifier>
<key> ::= <string>
<value> ::= <string>
```

While you must specify annotation on at least one object with the WITH ANNOTATION clause (table, column, or parameter), there is no limit on the number of annotations or types of annotations you can specify.

`<key>` and `<value>` represent the annotations you are configuring for the object (table, column, or parameter).

#### system_versioning_configuration

Alters system-versioning settings for a table.

```sql
<system_versioning_configuration> ::= {
<add_generated_always_column>
 | <convert_column_to_generated_always_column>
 | <add_drop_periods>
 | <add_drop_system_versioning>
}
<add_generated_always_column> ::= {
ADD ( <valid_from_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
START )
 | ADD ( <valid_to_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
END )
}
<convert_column_to_generated_always_column> ::= {
ALTER ( <valid_from_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
START )
 | ALTER ( <valid_to_column_name> TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
END )
}
<add_drop_periods> ::= {
ADD PERIOD FOR SYSTEM_TIME ( <valid_from_column_name>,
<valid_to_column_name> )
 | DROP PERIOD FOR SYSTEM_TIME
}

<add_drop_system_versioning> :: = {
 ADD SYSTEM VERSIONING HISTORY TABLE <history_table_name> [ [ NOT ]
VALIDATED ]
 | DROP SYSTEM VERSIONING
}
```

##### valid_from_column_name

In both `<history_table_definition>` and `<system_versioned_table_definition>`, this column defines the column that holds the start time of the validity period. Defining a column as a ROW START column initializes the column with the timestamp of the start of the current transaction, and GENERATED ALWAYS is the mechanism by which the system automatically updates the TIMESTAMP value in the column.

##### valid_to_column_name

In both `<history_table_definition>` and `<system_versioned_table_definition>`, this column defines the column that holds the end time of the validity period. Defining a column as a ROW END column initializes the column with the timestamp value '9999-12-31 23:59:59.9999999'.

##### ADD PERIOD FOR SYSTEM_TIME ( valid_from_column_name, valid_to_column_name ) | DROP PERIOD FOR SYSTEM_TIME

Adds or drops a validity period.

For the ADD syntax, `<valid_from_column_name>` is the column containing the start time value, and `<valid_to_column_name>` is the column containing the end time value.

##### ADD SYSTEM VERSIONING HISTORY TABLE history_table_name | DROP SYSTEM VERSIONING

Enables or disable system-versioning for the table.

For the ADD syntax, `<history_table_name>` must already exist and not be associated with any other system-versioned table.

##### [ [ NOT ] VALIDATED ]

Specifies whether to check if `<history_table_name>` is empty. If VALIDATED is specified (the default), an exception is raised if `<history_table_name>` is not empty. If NOT VALIDATED is specified, no emptiness check is performed on `<history_table_name>`, and no exception is raised even if the history table has data in it.

After you import a system-versioned table and its associated history table, you execute an ALTER TABLE statement to enable system-versioning. Since the history table is not empty, you must specify NOT VALIDATED to bypass the emptiness check.

#### add_drop_application_time_period

Defines the application-time period for the table, or drops the existing one.

```sql
ADD PERIOD FOR APPLICATION_TIME ( <validfrom_column_name>,
<validto_column_name> )
| DROP PERIOD FOR APPLICATION_TIME
```

Adding a period adds an implicit constraint that `<validfrom_column_name>` must be less than `<validto_column_name>`.

#### lob_reorganize_clause

Applies the midsizelob_threshold system property to the specified LOB column or to all LOB columns in the specified table.

```sql
<lob_reorganize_clause> ::=
 LOB REORGANIZE [(<column-list>)] [ ONLINE [ PREFERRED ] ]
```

If a comma-separated list is not provided, then the midsizelob_threshold system property is applied to any LOB column in the specified table.

##### ONLINE

Allows LOB reorganize operations that do not serialize with concurrent DML operations. ONLINE is only supported for column-store, non-multistore tables, where specifying ONLINE performs a LOB reorganize operation that only acquires a shared table lock. The operation is still serialized with other concurrent DDL operations on the table, including other ONLINE DDL operations **PREFERRED** When specified with the ONLINE option, if ONLINE execution is not supported, then a SQL warning message appears, and the add operation executes in table x-lock mode.

#### clear_column_join_data_statistics_clause

Clears the join data statistics for the specified table.

```sql
<clear_column_join_data_statistics_clause> ::= CLEAR COLUMN JOIN DATA
STATISTICS
```

#### constraint_clauses

Defines the constraint operations you can perform.

```sql
[<add_constraint_clause>]
[<drop_constraint_clause>]
[<alter_constraint_enforcement_clause>]
```

##### add_constraint_clause

Adds a table constraint.

```sql
<add_constraint_clause> ::=
 ADD [CONSTRAINT <constraint_name>] <table_constraint>
<constraint_name> ::= <identifier>
```

###### table_constraint

Specifies either a unique constraint, a referential constraint, or a check constraint.

```sql
<table_constraint> ::=
 <unique_constraint_definition>
 | <referential_constraint_definition>
| <check_constraint_definition>
```

###### unique_constraint_definition

Specifies a unique constraint.

```sql
<unique_constraint_definition> ::=
<unique_specification> (<unique_column_name_list>)
```

For more information about unique constraints, see the CREATE TABLE statement.

###### unique_column_name_list

Specifies the unique column name list, which can have one or more column names.

```sql
<unique_column_name_list> ::=
 <unique_column_name>[{, <unique_column_name>}...]
<unique_column_name> ::= <identifier>
```

###### referential_constraint_definition

Specifies a referential constraint.

```sql
<referential_constraint_definition> ::=
FOREIGN KEY (<referencing_column_name_list>) <references_specification>
```

To ensure uniqueness, the target of a foreign key constraint must be either a full primary key or a unique column. Self-referencing foreign key constraints are supported.

###### referencing_column_name_list

Specifies the target column(s) of the foreign key constraint.

```sql
<referencing_column_name_list> ::= <referencing_column_name>[{,
<referencing_column_name>}...]
```

###### referencing_column_name

The identifier of a referencing column.

```sql
<referencing_column_name> ::= <identifier>
```

###### references_specification

Specifies the referenced table, with optional column name list and trigger action.

```sql
<references_specification> ::=
 REFERENCES <referenced_table> [ ( <referenced_column_name_list> ) ]
 [ <referential_triggered_action> ]
 [ <constraint_enforcement> ]
 [ <constraint_check_time> ]
<constraint_enforcement> ::= <enforcement_option>
| <validation_option>
| <enforcement_option> <validation_option>
<enforcement_option> ::= [ NOT ] ENFORCED
<validation_option> ::= [ NOT ] VALIDATED
<constraint_check_time> ::=  INITIALLY { IMMEDIATE | DEFERRED }
```

Specifying NOT VALIDATED means that existing data will not be checked to determine whether it violates the foreign key constraint.

Specifying NOT ENFORCED means that new or modified rows will not be checked to determine whether they violate the foreign key constraint.

Enable or disable constraint enforcement rather than dropping and recreating the constraint.

The default `<enforcement_option>` is ENFORCED and the default `<validation_option>` is VALIDATED.

###### referenced_table

Specifies the identifier of a table to be referenced.

```sql
<referenced_table> ::= <identifier>
```

###### referenced_column_name_list

Specifies the referenced column name list, which can have one or more column names.

```sql
<referenced_column_name_list> ::= <referenced_column_name> [,
<referenced_column_name> [,…] ]
```

`<referenced_column_name>` specifies the identifier of the column name to be referenced.

If `<referenced_column_name_list>` is specified, then there is a one-to-one correspondence between `<column_name>` of `<column_definition>` (see column_definition [→](README.md)) and `<referenced_column_name>`. If it is not specified, then there is a one-to-one correspondence between `<column_name>` of `<column_definition>` and the column name of the referenced table's primary key.

###### referential_triggered_action

Specifies an update rule with optional delete rule or a delete rule with optional update rule.

```sql
<referential_triggered_action> ::=
   <update_rule> [ <delete_rule> ]
   | <delete_rule> [ <update_rule> ]
```

The order that you specify the rules in provides an order of precedence for execution.

###### update_rule

Specifies the behavior to perform when data in the column is updated.

```sql
<update_rule> ::= ON UPDATE <referential_action>
<referential_action> ::= { RESTRICT | CASCADE | SET NULL | SET
DEFAULT }
```

| **Action Name** | **Update Action** |
| --- | --- |
| RESTRICT | Any updates to a referenced table are prohibited if there are any matched records in the referencing table. This is the default action. |
| CASCADE | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with the same values. |
| SET NULL | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with null values. |
| SET DEFAULT | If a record is updated in the referenced table, then the corresponding records in the referencing table are also updated with their default values. |

###### delete_rule

Specifies the behavior to perform when data in the column is deleted.

```sql
<delete_rule> ::= ON DELETE <referential_action>
```

The following DELETE referential actions are possible:

| **Action Name** | **Delete Action** |
| --- | --- |
| RESTRICT | Any deletions to a referenced table are prohibited if there are any matched records in the referencing table. This is the default action. |
| CASCADE | If a record in the referenced table is deleted, then the corresponding records in the referencing table are also deleted. |
| SET NULL | If a record in the referenced table is deleted, then the corresponding records in the referencing table are set to null. |
| SET DEFAULT | If a record in the referenced table is deleted, then the corresponding records in the referencing table are set to their default values. |

###### check_constraint_definition

Specifies a condition to check for in the column.

```sql
<check_constraint_definition> ::= CHECK ( <search_condition> )
```

A table check constraint is satisfied if `<search_condition>` evaluates to true.

###### constraint_check_time

Specifies when to check constraints. The default is INITIALLY IMMEDIATE.

- IMMEDIATE - referential constraints are checked immediately during statement execution. If a referential constraint is violated, then the statement fails.
- DEFERRED - referential constraints are checked at commit time. If a referential constraint is violated, then the transaction is rolled back. Also, if `<referential_triggered_action>` is set to something other than RESTRICT, then the referential constraint check on the parent (referencing) table is not deferred and instead is checked immediately.

##### drop_constraint_clause

Drops a unique or referential constraint.

```sql
<drop_constraint_clause> ::= DROP CONSTRAINT <constraint_name>
<constraint_name> ::= <identifier>
```

##### alter_constraint_enforcement_clause

Alters enforcement for a table constraint.

```sql
<alter_constraint_enforcement_clause> ::= ALTER CONSTRAINT
<constraint_name> <constraint_enforcement>
<constraint_enforcement> ::= <enforcement_option>
 | <validation_option>
 | <enforcement_option> <validation_option>
<enforcement_option>  ::= [NOT] ENFORCED
<validation_option> ::= [NOT] VALIDATED
```

When you specify NOT VALIDATED, existing data is not checked to determine whether it violates the foreign key constraint.

When you specify NOT ENFORCED, means that new or modified rows are not checked to determine whether they violate the foreign key constraint.

Enable or disable constraint enforcement rather than dropping and recreating the constraint.

The default `<enforcement_option>` is ENFORCED and the default `<validation_option>` is VALIDATED.

#### convert_index_type

Converts a unique index, unique table constraint, or a primary key on a column store table to an INVERTED index type.

```sql
ALTER CONSTRAINT <constraint_name> UNIQUE <cs_inverted_type_index>
| ALTER PRIMARY KEY <cs_inverted_type_index>
```

##### cs_inverted_type_index

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

#### clientside_encryption_clauses

Defines the alter operations you can perform with regards to client-side encryption.

##### cancel_continue_clientside_encryption

Restarts or cancels (rolls back) an encryption/decryption/re-encryption operation.

```sql
<cancel_continue_clientside_encryption> ::=
 CONTINUE CLIENTSIDE ENCRYPTION
 | CANCEL CLIENTSIDE ENCRYPTION
```

###### CONTINUE CLIENTSIDE ENCRYPTION

Restarts a stopped encryption/decryption/re-encryption operation, avoiding the need to redo the operation from the beginning.

Use the CLIENTSIDE_ENCRYPTION_STATUS column of the TABLE_COLUMNS system view to determine the status of an encryption/decryption/re-encryption operation.

###### CANCEL CLIENTSIDE ENCRYPTION

Rolls back the data to the state it was in before the encryption/decryption/re-encryption operation started.

Only the session owner or an administrator can interrupt (stop) a session that is performing an encryption/decryption/re-encryption operation. After the operation has been interrupted, either this command or a CONTINUE command must be executed.

Use the CLIENTSIDE_ENCRYPTION_STATUS column of the TABLE_COLUMNS system view to determine the status of an encryption/decryption/re-encryption operation.

##### activate_clientside_encryption

Applies the new version of the encryption column key to the table where the data is re-encrypted with the new version of the encryption column key.

```sql
ALTER ( <column_name> ALTER CLIENTSIDE ENCRYPTION ACTIVATE NEW VERSION )
```

Only one column at a time can be altered to activate the new version of the column encryption key on the encrypted column.

##### enable_disable_clientside_encryption

Enables client-side encryption on a column using a specified column encryption key (CEK), or disables client-side encryption on a column. Only one column at a time can be altered to enable or disable client-side encryption.

```sql
<enable_disable_clientside_encryption> ::=
 ALTER ( <column_name> ALTER CLIENTSIDE ENCRYPTION { OFF | ( ON WITH
<column_encryption_key_name> [ RANDOM | DETERMINISTIC ] ) } )
<column_encryption_key_name> ::= [ <schema_name>.]<identifier>
```

`<column_encryption_key_name>` must be a valid column encryption key. Also, `<column_encryption_key_name>` and the table being altered must exist in the same schema.

RANDOM and DETERMINISTIC describe the type of encryption used by the algorithm to encrypt the data. RANDOM ensures that a given cleartext value is never encrypted into the same ciphertext value more than once. DETERMINISTIC means that a given cleartext value is always encrypted into the same ciphertext value. Deterministic encryption allows some operations such as equality comparisons on encrypted data, whereas non-deterministic encryption (RANDOM), while stronger, limits operations to basic inserts, updates, and fetches. Choose the type of encryption based on how the data is intended to be used. RANDOM is the default setting.

OFF disables client-side encryption on the column and decrypts the column data.

##### rotate_clientside_encryption_key

Re-encrypts the column data using a different column encryption key. Only one column at a time can be altered to rotate the column encryption key on the encrypted column.

```sql
ALTER ( <column_name> ALTER CLIENTSIDE ENCRYPTION WITH
<new_column_encryption_key_name> [ RANDOM | DETERMINISTIC ] )
<new_column_encryption_key_name> ::= [ <schema_name>.]<identifier>
```

RANDOM and DETERMINISTIC describe the behavior used by the encryption algorithm to encrypt the data.

`<new_column_encryption_key_name>` must be a valid column encryption key, and you must have key copies of the old column encryption key and the new column encryption key when re-encrypting.

#### primary_key_clauses

Defines the primary key operations that you can perform.

```sql
[<add_primary_key_clause>]
[<drop_primary_key_clause>]
```

##### add_primary_key_clause

Adds a primary key on a table.

```sql
<add_primary_key_clause> ::=
 ADD PRIMARY KEY ( <column_name> [, <column_name> [,...] ] )
```

###### rs_tree_type_index

Specifies the tree type for the index. Tree type specification is only applicable to row store tables.

```sql
<rs_tree_type_index> ::= { BTREE | CPBTREE }
```

###### CPBTREE

Specifies a CPB+-tree index for row store tables. CPB+-tree stands for Compressed Prefix B+- Tree, which is based on pkB-tree. CPB+-tree is a very small index because it uses 'partial key' that is only part of full key in index nodes. CPB+-tree shows better performance than B+-Tree for larger keys. Specify this type of tree for the following scenarios:

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

##### drop_primary_key_clause

Drops the primary key.

```sql
<drop_primary_key_clause> ::= DROP PRIMARY KEY
```

#### preload_clause

Sets or removes the preload flag of the given tables or columns.

```sql
<preload_clause> ::=
 PRELOAD ALL
 | PRELOAD ( <column_name> )
 | PRELOAD NONE
```

When the preload flag is set, tables are automatically loaded into memory after an index server start. This setting is available for column store tables.

The current status of the preload flag is visible in the system table **TABLES** in the IS_PRELOAD and IS_PARTIAL_PRELOAD columns and in the system table **TABLE_COLUMNS** in the PRELOAD column. Possible values are TRUE, FALSE, and NULL. Preload information can be NULL in the case of a row store, virtual columns, or tables on extended storage.

Using PRELOAD with ALL sets preload flags of all columns in the table.

PRELOAD (`<column_name>`) sets the flags of the specified column.

PRELOAD NONE removes the preload flag from all columns.

#### table_conversion_clause

Converts the table storage from ROW to COLUMN or from COLUMN to ROW.

```sql
<table_conversion_clause> ::= [ALTER TYPE] {
   ROW [THREADS <number_of_threads>]
   | COLUMN [ THREADS <number_of_threads> [ BATCH <batch_size> ] ]
}
```

##### THREADS number_of_threads

Specifies how many parallel execution threads should be used for the table conversion.

```sql
THREADS <number_of_threads>
 <number_of_threads> ::= <unsigned_integer>
```

The optimal value for the number of threads is the number of available CPU cores. If THREADS is not provided, then the default value of the number of CPU cores specified in the `indexserver.ini` file is used.

##### BATCH batch_size

Specifies the number of rows to be inserted in a batch.

```sql
BATCH <batch_size>
 <batch_size> ::= <unsigned_integer>
```

If BATCH is not specified, then the default value of 2,000,000 is used. Inserts into column tables are immediately committed after every `<batch_size>` records have been inserted. You can only use the BATCH option when a table is converted from ROW to COLUMN storage.

#### association_clauses

Defines the association operations you can perform.

```sql
[<add_association_clause>]
[<drop_association_clause>]
```

##### add_association_clause

Adds an association clause. Associations are checked at runtime.

```sql
<add_association_clause> ::= ADD ASSOCIATION ( <association_def> )
<association_def> ::= [ <join_cardinality> ] JOIN <table_name> [ AS
<identifier> ] ON <predicate> WITH DEFAULT FILTER <predicate>
<join_cardinality> ::=
 MANY TO ONE
 | MANY TO MANY
 | ONE TO ONE
 | ONE TO MANY
<table_name> ::= <identifier>
```

The WITH DEFAULT FILTER clause specifies a default predicate to filter column values.

##### drop_association_clause

Drops an association clause

```sql
<drop_association_clause> ::= DROP ASSOCIATION <identifier>
```

#### partition_clauses

For clauses to alter heterogeneous and non-heterogeneous partitions, see the topic Non-heterogeneous Partition Clauses or Heterogeneous Partition Clauses in this guide.

- Non-heterogeneous Alter Partition Clauses.
- Heterogeneous Alter Partition Clauses.

#### load_unit

Specifies how to load data into memory when the table is queried. Specifying the load unit is only supported on column-store tables. `<load_unit>` can be set at column, table, and partition levels.

```sql
<load_unit> ::= { COLUMN | PAGE | DEFAULT } LOADABLE [ CASCADE ]
```

In the case of competing or unspecified `<load_unit>` settings, the logic described in CREATE TABLE for `<load_unit>` is applied.

##### COLUMN LOADABLE

In-memory loading - the entire column is loaded into memory. COLUMN LOADABLE boosts performance at the cost of higher memory usage. This is the default behavior unless another value is inherited.

##### PAGE LOADABLE

Inbuffer cache loading - column data is loaded by page into the buffer cache. PAGE LOADABLE reduces memory usage for specific columns by not requiring those columns to be fully memory resident.

##### DEFAULT LOADABLE

If you specify DEFAULT, then there is no explicit preference for the paging attribute that is used when the results are loaded from the table. If there is an inherited loading unit from another object, then that loading unit is used.

##### CASCADE

Specify CASCADE when you want the paging attribute to apply to all objects below the specified object in the object hierarchy, so table paging attributes apply to partitions.

#### alter_persistent_memory_spec_clause

Alters the persistent memory storage preference at the table, partition, or column level, depending on where the clause is situated in the ALTER statement. For example, when specified inside `<column_definition>`, it enables or disables persistent memory for the column. When specified inside `<add_range_partition_clause>`, it enables or disables persistent memory for the new partition.

> **Note**
>
> This clause is not supported for heterogeneous range partitions.

```sql
<alter_persistent_memory_spec_clause> ::= PERSISTENT MEMORY
<alter_pm_preference> [ IMMEDIATE | DEFERRED ] [ CASCADE ]
<alter_pm_preference> ::= { ON | OFF | DEFAULT }
```

##### ON IMMEDIATE

Enables persistent memory usage and populates the underlying PERSISTENT MEMORY storage.

##### ON or ON DEFERRED

Enables persistent memory usage without populating the underlying PERSISTENT MEMORY storage. PERSISTENT MEMORY storage population happens as part of next load from disk or delta merge. DEFERRED is the default behavior when ON is specified without IMMEDIATE or DEFERRED.

##### OFF IMMEDIATE

Disables persistent memory usage and reloads data into DRAM. Cleanup of underlying persistent memory is handled asynchronously.

##### OFF or OFF DEFERRED

Disables persistent memory usage without switching in memory data to DRAM. Data is loaded into DRAM as part of next delta merge or reload. Deletion of persistent memory is driven via delta merge cleanup and subsequent savepoint. DEFERRED is the default behavior when OFF is specified without IMMEDIATE or DEFERRED. Cleanup of underlying persistent memory is handled asynchronously.

##### DEFAULT

No explicit preference is set for persistent memory usage at the specified object level (table, partition or column). Instead, the SAP server, falls back to default behavior, which is to use the inherited persistent memory preference, if any.

IMMEDIATE and DEFERRED actions are not supported when DEFAULT is specified.

##### CASCADE

The userspecified persistent memory preference is applied to all objects below the specified object in the object hierarchy. CASCADE is not supported at the partition level, and is meaningless at the column level.

#### replica_clauses

Defines the alter operations you can perform with regards to replicas.

##### add_replica_clause

Adds a replica.

```sql
<add_replica_clause> ::= ADD [ <sync_or_async> ] [ <column_or_row> ]
REPLICA [ ( <src_table_column_list> ) ] [ <replica_partition> ]
 [ AT <replica_locations> ]
```

###### column_or_row

Replica type is specified by `<column_or_row>`. If it is not specified, then the type is the same as that of table.

```sql
<column_or_row> ::= { COLUMN | ROW }
```

###### sync_or_async

Specifies whether the replica is immediately activated.

```sql
<sync_or_async> ::= { SYNCHRONOUS | ASYNCHRONOUS }
```

SYNCRONOUS replicas are activated immediately. ASYNCRONOUS replicas are created in an empty state; execute an ALTER SYSTEM ENABLE ALL ASYNCHRONOUS TABLE REPLICAS statement to activate them.

###### src_table_column_list

Specifies a subset of the columns in the source table. A replica that has a subset of the columns from the source table is called a **column-wise replica**.

```sql
<src_table_column_list> ::= <column_name> [, <column_name> [,…] ]
```

Although you can specify the columns in any order, the order of the columns in the replica matches the order of columns in the source table.

If you specify all of the columns from the source table, then the replica that is created is no longer considered a column-wise replica.

###### replica_partition

Specifies the partitions for the replicated table.

```sql
<replica_partition> ::= <partition_table_clause>
```

The `<replica_partition>` clause supports all partition types not using time selection. See the definition for `<partition_table_clause>`.

###### AT replica_locations

Adds the replica to the specified locations.

```sql
<replica_locations> ::= { <indexserver_host_port> |
( <indexserver_host_port>, … ) }
<indexserver_host_port> ::= '<host_name>:<port_number>'
```

If `<replica_locations>` is not specified, then the replica table is added based on the table placement rule. If no table placement rule is also defined, then the replica table is added one of the slave nodes that is not a source table location and where there is not already an existing replica of the table. If there are no more replica nodes to add a replica table, then an error is returned.The former syntax, `AT { ALL LOCATIONS | <num_replicas> LOCATIONS }`, is supported but deprecated. Specify locations using the AT `<replica_locations>` syntax instead.

##### drop_replica_clause

Drops a replica at the specified location.

```sql
<drop_replica_clause> ::= DROP REPLICA AT LOCATIONS <replica_locations>
<replica_locations> ::= { '<indexserver>:<port>' |
( '<indexserver>:<port>' [, '<indexserver>:<port>' [,…] ]  ) }
```

The use of the `AT {ALL | <num_replicas> LOCATIONS}` syntax supported in previous versions of SAP HANA is deprecated. Use the `<replica_locations>` syntax instead.

##### enable_disable_replica_clause

Enables or disables the replication operation for the specified table.

```sql
<enable_disable_replica_clause> ::=
<source_schema_name>.<source_table_name> { ENABLE | DISABLE }
[ SYNCHRONOUS | ASYNCHRONOUS ] REPLICA
 [ PARTITION <partition_number> ]
<source_schema_name> ::= <identifier>
<source_table_name> ::= <identifier>
```

If [SYNCHRONOUS | ASYNCHRONOUS] is not specified, the default is SYNCHRONOUS.

The optional PARTITION `<partition_number>` syntax enables or disables the overall asynchronous replication for the specified table partition. `<partition_number>` is allowed only for an actual partition, not for a historical partition.

SYNCHRONOUS is not supported for remote table replication.

##### move_replica_clause

Moves replicas from one index server to another.

```sql
<move_replica_clause> ::=
 MOVE REPLICA [ PARTITION <partition_number> ] FROM [ LOCATION ]
<from_location> TO [ LOCATION ] <to_location>

<from_location> ::= <indexserver_host_port>
<to_location> ::= <indexserver_host_port>
<indexserver_host_port> ::= '<host_name>:<port_number>'
```

##### set_replica_clause

Swaps the source and replica for replication, so that the replica becomes the source and the source becomes the replica.

This clause is only supported if the columns in the source table and replica are the same.

```sql
<set_replica_clause> ::= SET REPLICA SOURCE AT '<host_name>:<port_number>'
```

`<host_name>` and `<port_number>`

#### redo_log_option

Enables or disables the redo log creation for the table.

```sql
<redo_log_option> ::= { ENABLE | DISABLE } DELTA LOG
```

After enabling, you must perform a savepoint to be certain that all data is persisted. Also you have to perform a data backup, otherwise it is not possible to recover this data.

If logging is disabled, then log entries do not persist for this table. Changes to this table are only written to the data store when a savepoint is carried out. This can cause loss of committed transaction should the indexserver terminate. In the case of a termination, you must truncate this table and insert all data again. Only use this option during initial load.

This clause leads to data differences between a primary and secondary site; therefore, use this clause cautiously.

#### auto_merge_option

Enables or disables automatic delta merge on the specified table.

```sql
<auto_merge_option> ::= {ENABLE | DISABLE} AUTOMERGE
```

The delta merge feature is only supported on column store tables.

#### unload_priority

Sets the priority of table to be unloaded from memory.

```sql
<unload_priority_option> ::= UNLOAD PRIORITY <unload_priority>
<unload_priority> ::= <digit>
```

`<unload_priority>` are can be 0 ~ 9, where 0 means not-unloadable and 9 means earliest unload.

#### schema_flexibility_option

Enables, disables, or alters schema flexibility for the specified table.

```sql
<schema_flexibility_option> ::=
 { {ENABLE | DISABLE} SCHEMA FLEXIBILITY}
 | ALTER SCHEMA FLEXIBILITY <flexibility_option> [<flexibility_option> […] ]
```

##### ALTER SCHEMA FLEXIBILITY

Alters the schema flexibility for the specified table.

```sql
ALTER SCHEMA FLEXIBILITY <flexibility_option> [ <flexibility_option> […] ]
```

All schema flexibility options that are listed in the CREATE TABLE statement in the WITH SCHEMA FLEXIBILITY section can be used here.

#### trigger_option

Enables or disables the specified trigger on the specified table.

```sql
<trigger_option> ::= { ENABLE | DISABLE } TRIGGER [<trigger_name>]
```

If `<trigger_name>` is not specified, then this setting enables or disables all triggers on the specified table.

#### group_option_clasues

Defines the group option operations that you can set.

```sql
[<set_group_option>]
[<unset_group_option>]
```

##### set_group_option

Sets one or more table group option for the table. Table group settings are stored in the TABLE_GROUPS system view.

```sql
<set_group_options> ::= SET <option> [...]
<option> ::=
 GROUP TYPE <identifier>
 | GROUP SUBTYPE <identifier>
 | GROUP NAME <identifier>
 | GROUP LEAD
```

##### unset_group_option

Unsets (removes) all table group attributes for the table (type, subtype, name, and so on).

```sql
<unset_group_option> ::= UNSET GROUP
```

#### row_order_clauses

Defines the row order clauses you can set.

```sql
[<set_row_order>]
[<unset_row_order>]
```

##### set_row_order

Sets the row order and type.

```sql
<set_row_order> ::= SET <row_order_definition>
<row_order_definition> ::= <row_order_specification>
(<unique_column_name_list>)
<row_order_specification> ::= ROW ORDER [BY VALUE]
<unique_column_name_list> ::= <unique_column_name> [,…]
```

Rows are sorted exactly by value for a given set of columns. BY VALUE is the default.

##### unset_row_order

Unsets the row order and type.

```sql
<unset_row_order> ::= UNSET ROW ORDER
```

#### unused_retention_period

Unloads a table or table partition from memory if it was not accessed for the number of seconds defined as the retention period.

```sql
<unused_retention_period> ::= UNUSED RETENTION PERIOD { <retention_period> |
( <retention_period> [,…] )}
<retention_period> ::= <unsigned_integer>
```

A single value specifies the retention period at table-level, including all of the table partitions. Multiple values specify specific retention periods for each of the table partitions. If multiple values are specified, then the number of values must match the number of table partitions.

The default value and behavior of UNUSED_RETENTION_PERIOD is 0 (inactive). To activate UNUSED_RETENTION_PERIOD, change the value to something other than 0. However, use of the UNUSED_RETENTION_PERIOD setting on a table requires that the global unused_retention_period setting in the `global.ini` configuration file be set to something other than 0.

#### reclaim_data_space_clause

Reclaims data space of the specified table. This clause is only for use on row store tables.

```sql
<reclaim_data_space_clause> ::= RECLAIM DATA SPACE
```

This statement has the same effect as defragmentation by restructuring table data space. However, this behavior does not always guarantee that restructured data space uses less memory than before. In some optimized cases, restructured data space uses much memory.

#### series_reorganize_clause

Reorganizes a series table.

```sql
<series_reorganize_clause> ::=
 SERIES REORGANIZE [ PART <int_const_partnum> ] [ LIMIT
<inst_const_reorganize_limit> ]
```

All table partitions are reorganized by default. If an error occurs during the reorganize operation, then it is returned from the blocking statement.

By default, the statement blocks until all reorganized work is completed.

##### PART int_const_partnum

Reorganizes the specified partition.

##### LIMIT inst_const_reorganize_limit

Limits the number of rows processed by the statement.

#### owner_to_clause

Specifies a new owner for the table.

```sql
<owner_to_clause> ::= OWNER TO <user_name>
```

The new owner becomes the grantor for all of the privileges on the table that were granted by the old owner. Also, the old owner is granted all privileges for the table by the new owner so that they can continue running jobs on the table.

#### alter_mask_settings_clause

Add a new mask expression or drop an existing mask expression. Data masking transforms confidential data so that it appears meaningless to users who don't have the privileges required to view it. `<alter_mask_settings_clause>` does not change the table's column definitions.

```sql
<alter_mask_settings_clause> ::=
 { ADD | ALTER } [{ DEFAULT | SESSION USER }] MASK ( <columns_name> USING
<mask_expression> [,…] )
 | ALTER MASK ( <columns_name> USING <mask_expression> [,…] )
 | DROP MASK ( <column_name_list> )
<mask_expression> ::= <expression>
<column_name_list> ::= <column_name>[,…]
```

When adding a mask expression, the mask behavior is defined for the object. New column masks must use the same mask mode. When altering, you can change the mask expression, but not the mode. Once all existing masks are dropped, you can add new masks using a different mask mode.

Masking behavior is supported on row and column tables, and SQL row and calculation views. It is not supported on any other type of tables (virtual tables, extended tables, temporary tables etc.) and views (Join/Olap/Hierarchy views).

Only one masking behavior, definer owner-based (DEFAULT MASK) or session user based masking (SESSION USER MASK), is supported on a table or view with masked columns. You can combine both masking behaviors in an object hierarchy. For example, a view with session user based masking can be created on a table with owner-based masking.

If not specified, DEFAULT is the default.

`<mask_expression>` can be any type of expression, including a userdefined function, that returns the same data type and length as the original column.

For more information on data masking, see the SAP HANA Cloud, SAP HANA Database Security Guide.

#### set_movable_clause

Controls whether the table can be moved to another location.

```sql
<set_movable_clause> ::= SET [NOT] MOVABLE
```

When a table is set to NOT MOVABLE, it cannot be moved to another location. By default, tables are movable.

#### numa_node_preference_clause

Alters the NUMA node preferences. Although this clause is defined here at the table level, `<numa_node_preference_clause>` can be set in various locations such as range partition definitions (not hash or round-robin) and column definitions, as indicated in the syntax within the topic. `<numa_node_preference_clause>` is not supported for heterogeneous partitions.

```sql
<numa_node_preference_clause> ::= NUMA NODE { ( <numa_node_index_spec> ) |
NULL } [ IMMEDIATE | DEFERRED ]
<numa_node_index_spec> :: = <numa_node_spec> [, <numa_node_spec> [,…] ]
<numa_node_spec> ::= { <single_node_spec> | <range_node_spec> }
<single_node_spec> :: =  <integer_const>
<range_node_spec> :: =  <integer_const> TO <integer_const>
```

##### NULL

To unset existing NUMA node preferences on the associated object (table, column, partition, or replica), specify NUMA NODE NULL.

##### IMMEDIATE, DEFERRED

Specify whether to apply the NUMA node preferences immediately (IMMEDIATE) or to defer applying the preferences until the next time the table is reloaded (DEFERRED). If you specify IMMEDIATE, then the associated table, column, or table partition is immediately moved according to the altered preference settings.

##### integer_const

`<integer_const>` cannot be a negative number.

##### numa_node_spec

Specify one or more single NUMA nodes (`<single_node_spec>`), or one or more NUMA node ranges (`<range_node_spec>`), or a mixture of both.

NUMA node indexes should be specified in the range of 0 to one less than max_numa_node_count, where max_numa_node_count is the number of NUMA nodes configured for the system. If the NUMA node index specified is greater than or equal to max_numa_node_count, then a random NUMA node in the range of 0 to one less than max_numa_node_count is selected for allocation. For example, on a system where max_numa_node_count is set to 8, if you specify a NUMA node index of 10, then any node in the range of 0 to 7 (inclusive) is chosen randomly for allocation.

## Description

This statement is not for use with virtual tables. To alter a virtual table, use the ALTER VIRTUAL TABLE statement.

## Examples

Create Table t, and then alter the default value of column b to 10.

```sql
CREATE ROW TABLE t (a INT, b INT, c INT);
ALTER TABLE t ALTER (b INT DEFAULT 10);
```

Alter table t adding a new column d.

```sql
ALTER TABLE t ADD (d NVARCHAR(10) DEFAULT 'NCHAR');
```

Drop a primary key on an existing table t.

```sql
ALTER TABLE t DROP PRIMARY KEY;
```

Add a primary key on table t to columns c and d.

```sql
ALTER TABLE t ADD PRIMARY KEY (c,d);
```

Add a primary key constraint, prim_key, on columns a and b of existing table t.

```sql
ALTER TABLE t ADD CONSTRAINT prim_key PRIMARY KEY (a, b);
```

Change the table type of table t to COLUMN storage.

```sql
ALTER TABLE t COLUMN;
```

Set the preload flags of column b and c on table t.

```sql
ALTER TABLE t PRELOAD (b, c);
```

Change the unload priority of table t to 2:

```sql
ALTER TABLE t UNLOAD PRIORITY 2;
```

Apply the midsize LOB threshold system property to the data column of the t table.

```sql
ALTER TABLE t LOB REORGANIZE (a);
```

Apply the midsize LOB threshold system property to all LOB columns on the t table.

```sql
ALTER TABLE t LOB REORGANIZE;
```

Create table T3 with page loadable columns C3, C4 and C5. Then, C3 becomes column loadable and C6 page loadable.

```sql
CREATE COLUMN TABLE T3 (C1 INT PRIMARY KEY, C2 DATE, C3 VARCHAR(80) PAGE
LOADABLE NOT NULL,
   C4 VARCHAR(5000) PAGE LOADABLE, C5 VARCHAR(5000) PAGE LOADABLE NOT NULL,
C6 VARCHAR(5000));
 ALTER TABLE T3 ALTER (C3 VARCHAR(80) COLUMN LOADABLE, C6 ALTER PAGE
LOADABLE);
```

Set group type and name of T3, and then unset it:

```sql
ALTER TABLE T3 SET GROUP TYPE group_type1 GROUP NAME group_name1;
ALTER TABLE T3 UNSET GROUP;
```

Execute the following statements to create and populate table t1 and then perform a drop operation on column a that does not serialize with concurrent DML operations:

```sql
CREATE TABLE t1 (a INT, b INT);
ALTER TABLE t1 DROP (a) ONLINE;
```

Alter the primary key index on Table T1 to an inverted HASH type.

```sql
ALTER TABLE T1 ALTER PRIMARY KEY INVERTED HASH;
```

#### JOIN

Retrieve, display, and delete column join data statistics.

```sql
DROP TABLE A;
CREATE COLUMN TABLE A ( NVARCHAR(2), ab INT);
DROP TABLE B;
CREATE COLUMN TABLE B (b1 INT, b2 NVARCHAR(1));
INSERT INTO A (, ab) VALUES ('', 1);
INSERT INTO A (, ab) VALUES ('BB', 2);
INSERT INTO B (b1, b2) VALUES (1, 'a');
INSERT INTO B (b1, b2) VALUES (3, 'f');
MERGE DELTA OF A;
MERGE DELTA OF B;
```

Perform a join on tables A and B.

```sql
SELECT * FROM A INNER JOIN B ON A.ab = B.b1;
```

View the column join data statistics for tables A and B.

```sql
SELECT COUNT(*) FROM M_JOIN_DATA_STATISTICS WHERE schema_name1 = 'SYSTEM' AND
table_name1 IN ('A', 'B');
SELECT * FROM M_JOIN_DATA_STATISTICS;
```

Clear the column join data statistics from the system.

```sql
ALTER SYSTEM CLEAR COLUMN JOIN DATA STATISTICS;
```

Clear the column join data statistics from table A.

```sql
ALTER TABLE A CLEAR COLUMN JOIN DATA STATISTICS;
```

#### Schema flexibility

Create table T1 and then turn on the schema flexibility of the table. You test the schema flexibility of table T1 by inserting a new record. A new column F is automatically created and a record is inserted:

```sql
CREATE COLUMN TABLE T1 (C INT);
 ALTER TABLE T1 ENABLE SCHEMA FLEXIBILITY;
 INSERT INTO T1 (C, F) VALUES (1, 'NVAR1');
```

#### Fuzzy searching

Create table T2 with a fuzzy search index and fuzzy search mode. You then switch off the fuzzy search index of COL1 and finally reset fuzzy search mode of COL2.

```sql
CREATE COLUMN TABLE T2 (KEY INT, COL1 VARCHAR(10) FUZZY SEARCH INDEX ON, COL2
NVARCHAR(10) FUZZY SEARCH MODE 'postcode');
 ALTER TABLE T2 ALTER (COL1 VARCHAR(10) FUZZY SEARCH INDEX OFF);
 ALTER TABLE T2 ALTER (COL2 NVARCHAR(10) FUZZY SEARCH MODE NULL);
```

#### Identity columns

Create table T5, and add an identity column B with starting value of 100 and an increment of 10.

```sql
CREATE COLUMN TABLE T5 (A INT);
 ALTER TABLE T5 ADD (B INT GENERATED ALWAYS AS IDENTITY (START WITH 100
INCREMENT BY 10));
```

Create table T_ALWAYS with identity column B that has a start value of 100 and increments by 10.

```sql
CREATE COLUMN TABLE T_ALWAYS (A INT);
ALTER TABLE T_ALWAYS ADD (B INT GENERATED ALWAYS AS IDENTITY (START WITH 100
INCREMENT BY 10));
INSERT INTO T_ALWAYS (A) VALUES (1);
INSERT INTO T_ALWAYS (A) VALUES (2);
SELECT * FROM T_ALWAYS;
```

| **A** | **B** |
| --- | --- |
| 1 | 100 |
| 2 | 110 |

Create table T_DEFAULT with identity column B that has a start value of 100 and increments by 10.

```sql
CREATE COLUMN TABLE T_DEFAULT (A INT);
ALTER TABLE T_DEFAULT ADD (B INT GENERATED ALWAYS AS IDENTITY (START WITH 100
INCREMENT BY 10));
INSERT INTO T_DEFAULT (A) VALUES (1);
INSERT INTO T_DEFAULT (A) VALUES (2);
INSERT INTO T_DEFAULT (A, B) VALUES (3, 105);
INSERT INTO T_DEFAULT (A) VALUES (4);
INSERT INTO T_DEFAULT (A, B) VALUES (5, 205);
INSERT INTO T_DEFAULT (A) VALUES (6);
SELECT * FROM T_DEFAULT;
```

In the results table below, the Description column isn't part of the results, it is provided to explain the values in column B.

| **A** | **B** | **Description** |
| --- | --- | --- |
| 1 | 100 | The START WITH value |
| 2 | 110 | The next INCREMENT value |
| 3 | 105 | A specified value that is lower than the current sequence |
| 4 | 120 | The next INCREMENT value |
| 5 | 205 | The specified value that resets the internal sequence to 200 |
| 6 | 210 | The next INCREMENT value |

#### Table replication

Create an additional asynchronous table replica for table `SRC_SCHEMA.TAB1`.

```sql
ALTER TABLE SRC_SCHEMA.TAB1 ADD ASYNCHRONOUS REPLICA;
```

Drop the table replicas of `SRC_SCHEMA.TAB1` in all locations.

```sql
ALTER TABLE SRC_SCHEMA.TAB1 DROP REPLICA AT ALL LOCATIONS;
```

Drop the table replica of `SRC_SCHEMA.TAB1` on `hostb:30301`.

```sql
ALTER TABLE SRC_SCHEMA.TAB1 DROP REPLICA AT 'hostb:30301';
```

Enable asynchronous table replication for the table `SRC_SCHEMA.TAB1`.

```sql
ALTER TABLE SRC_SCHEMA.TAB1 ENABLE ASYNCHRONOUS REPLICA;
```

Disable asynchronous table replication for the table `SRC_SCHEMA.TAB1`.

```sql
ALTER TABLE SRC_SCHEMA.TAB1 DISABLE ASYNCHRONOUS REPLICA;
```

Create table T4 with replicas in all indexservers. Then, you drop all replicas and create a replica at the specific indexserver. Then, you move the replica to the other indexserver.

```sql
CREATE ROW TABLE T4 (C1 INT PRIMARY KEY) REPLICA AT ALL LOCATIONS;
 ALTER TABLE T4 DROP REPLICA AT ALL LOCATIONS;
 ALTER TABLE T4 ADD REPLICA AT 'host_name:30040';
 ALTER TABLE T4 MOVE REPLICA FROM 'host_name:30040' TO 'host_name:30042';
```

Add a replica to table SRC_TABLE.

```sql
CREATE COLUMN TABLE SRC_TABLE (C1, C2, C3) PARTITION BY HASH (C1) PARTITIONS
32;
ALTER TABLE SRC_TABLE ADD REPLICA PARTITION BY HASH (C2) PARTITIONS 8;
```

#### Client-side encryption

The following statements create a table T6 and enable client-side encryption on column `Name` using the `myCEK` column encryption key.

```sql
CREATE ROW TABLE T6 ( ID INT PRIMARY KEY, Name NVARCHAR(32) );
ALTER TABLE T6 ALTER ( Name ALTER CLIENTSIDE ENCRYPTION ON WITH myCEK
RANDOM );
```

The following example changes the column encryption key used to encrypt column `T6.Name` to `myCEK2`, and changes the encryption mode to DETERMINISTIC:

```sql
ALTER TABLE T6 ALTER ( Name ALTER CLIENTSIDE ENCRYPTION WITH myCEK2
DETERMINISTIC );
```

The following statement cancels the interrupted encryption operation that is taking place on column `T6.Name` and rolls back the column to how it was before the encryption operation began:

```sql
ALTER TABLE T6 CANCEL CLIENTSIDE ENCRYPTION;
```

The following statement disables column encryption on `T6.Name`:

```sql
ALTER TABLE T6 ALTER ( Name ALTER CLIENTSIDE ENCRYPTION OFF );
```

The following statement applies a new version of the encryption key to column encryption on T1.C2.

```sql
ALTER TABLE T1 ALTER ( C2 ALTER CLIENTSIDE ENCRYPTION ACTIVATE NEW VERSION);
```

#### Data masking

Alter the Personal_Information table to use masking for the SSN column:

```sql
ALTER TABLE PERSONAL_INFORMATION ADD MASK (SSN USING '****');
```

Alter the Personal_Information table to drop masking from the SSN column:

```sql
ALTER TABLE PERSONAL_INFORMATION DROP MASK (SSN);
```

#### Constraints

Create two tables and then add a foreign key constraint to table REFERENCING_T.

```sql
CREATE COLUMN TABLE REFERENCED_T ( A INT PRIMARY KEY, B INT);
CREATE COLUMN TABLE REFERENCING_T (A INT, B INT);
ALTER TABLE REFERENCING_T ADD CONSTRAINT fk1 FOREIGN KEY(A) REFERENCES
REFERENCED_T(A);
```

Populate the tables REFERENCED_T and REFERENCING_T.

```sql
INSERT INTO REFERENCED_T VALUES (1, 1);
INSERT INTO REFERENCING_T VALUES (1, 1);
```

Executing the following statement fails with a foreign key constraint violation:

```sql
INSERT INTO REFERENCING_T VALUES (2, 1);
```

Alter table REFERENCING_T so that the foreign key constraint is not enforced.

```sql
ALTER TABLE REFERENCING_T ALTER CONSTRAINT fk1 NOT ENFORCED;
```

Now, running the following statement succeeds:

```sql
INSERT INTO REFERENCING_T VALUES (2, 1);
```

If you then run the following statement, it fails as the constraint is violated by the value that was just inserted:

```sql
ALTER TABLE REFERENCING_T ALTER CONSTRAINT fk1 ENFORCED;
```

However, if you add NOT VALIDATED to the statement above and re-run it, it succeeds.

```sql
ALTER TABLE REFERENCING_T ALTER CONSTRAINT fk1 ENFORCED NOT VALIDATED;
```

Running the same INSERT statement as above now fails because the ENFORCED NOT VALIDATED clause means that only existing data is not checked, but modified rows cannot violate the constraint.

```sql
INSERT INTO REFERENCING_T VALUES (2, 1);
```

Create a table and add a unique constraint UK.

```sql
CREATE ROW TABLE R (A INT PRIMARY KEY, B NVARCHAR(10));
 ALTER TABLE R ADD CONSTRAINT UK UNIQUE (B);
```

Drop the unique constraint UK from table R.

```sql
ALTER TABLE R DROP CONSTRAINT UK;
```

Create table S. You add a referential constraint FK to table S that references column A of table R with delete cascade option.

```sql
CREATE ROW TABLE S (FA INT, B NVARCHAR(10));
 ALTER TABLE S ADD CONSTRAINT FK FOREIGN KEY(FA) REFERENCES R(A) ON DELETE
CASCADE;
```

The following example creates a column table, creates a history table, and then alters the column table to configure and enable system versioning:

```sql
CREATE COLUMN TABLE account (
  account_id INT PRIMARY KEY,
  account_owner_id NVARCHAR(10),
  account_balance DOUBLE
 );
CREATE COLUMN TABLE account_history (
  account_id INT,
  account_owner_id NVARCHAR(10),
  account_balance DOUBLE,
  valid_from TIMESTAMP NOT NULL,
  valid_to TIMESTAMP NOT NULL
 );
ALTER TABLE account ADD (valid_from TIMESTAMP NOT NULL GENERATED ALWAYS AS
ROW START);
ALTER TABLE account ADD (valid_to TIMESTAMP NOT NULL GENERATED ALWAYS AS ROW
END);
ALTER TABLE account ADD PERIOD FOR SYSTEM_TIME(valid_from, valid_to);
ALTER TABLE account ADD SYSTEM VERSIONING HISTORY TABLE account_history;
```

#### Persistent memory

Alter a table’s PERSISTENT MEMORY specification and cascade the setting to partitions and columns:

```sql
ALTER TABLE myTable1 PERSISTENT MEMORY ON IMMEDIATE CASCADE;
```

Alter a column’s PERSISTENT MEMORY specification:

```sql
ALTER TABLE myTable2 ALTER (C1 INT PERSISTENT MEMORY DEFAULT);
```

Add a partition with a PERSISTENT MEMORY specification:

```sql
ALTER TABLE myTable3 ADD RANGE (C1) (PARTITION '0' <= VALUES < '10',
PARTITION OTHERS PERSISTENT MEMORY ON DEFERRED);
```

Partition a table with a PERSISTENT MEMORY specification for selected partitions:

```sql
ALTER TABLE myTable4 PARTITION BY RANGE (C1) (PARTITION '0' <= VALUES < '10'
PERSISTENT MEMORY ON IMMEDIATE, PARTITION OTHERS);
```

Alter a partition’s PERSISTENT MEMORY specification:

```sql
ALTER TABLE myTable5 ALTER PARTITION 10 PERSISTENT MEMORY DEFAULT;
```

#### Non-heterogeneous partitions

Convert a non-partitioned column store table named T1 to a range partitioned table.

```sql
CREATE COLUMN TABLE T1 (a INT, b INT);
ALTER TABLE T1 PARTITION BY RANGE (a) ( PARTITION 10 <= VALUES < 20);
```

Add a new second-level partition to an existing range-partitioned table, making it a range-range partitioned table.

```sql
ALTER TABLE T1 PARTITION BY
   RANGE (a) ( PARTITION 10 <= VALUES < 20),
   RANGE (b) ( PARTITION 100 <= VALUES < 150);
```

Redefine the existing firstlevel partition to ranges 10 - 15 and 15 - 20.

```sql
ALTER TABLE T1 PARTITION BY
   RANGE (a) ( PARTITION 10 <= VALUES < 15, PARTITION 15 <= VALUES < 20),
   RANGE (b) ( PARTITION 100 <= VALUES < 150);
```

Add a new partition to the second-level partition.

```sql
ALTER TABLE T1 ADD PARTITION (b) USING DEFAULT STORAGE (150 <= VALUES < 200);
```

Move a partition.

```sql
ALTER TABLE T1 MOVE PARTITION 1 TO 'myhost:30201';
```

Drop second-level partition range 10 - 15.

```sql
ALTER TABLE T1 DROP PARTITION (a) 10 <= VALUES < 15;
```

Merge all partitions into a single non-partitioned table.

```sql
ALTER TABLE T1 MERGE PARTITIONS;
```

```sql
ALTER TABLE T1 PARTITION BY RANGE (a) (PARTITION 15 <= VALUES < 20 NUMA NODE
('3') DEFERRED);
```

Alter column table T1, setting the NUMA node preference at the partition level on NUMA node index 3. Since DEFERRED is specified, it sets only the NUMA preference for the partition; the actual allocations are made when the table is reloaded. IMMEDIATE alters column table T1, setting the NUMA node preference on partition 1, which already exists. The allocations are made immediately, and the table partition is reloaded to node 4.

```sql
ALTER TABLE T1 ALTER PARTITION 1 NUMA NODE ('4') IMMEDIATE;
```

Create a non-partitioned table named T2, convert the table to a range partitioned table, and then add an additional partition.

```sql
CREATE COLUMN TABLE T2 (a INT, b INT);
ALTER TABLE T2 PARTITION BY RANGE (a) (PARTITION VALUE = 1, PARTITION OTHERS);
ALTER TABLE T2 ADD PARTITION (a) 2 <= VALUES < 10;
```

Create a non-partitioned table named T3 and then convert the table to a range-range partitioned table.

```sql
CREATE COLUMN TABLE T3 (a INT, b INT);
ALTER TABLE T3 PARTITION BY RANGE (a) (PARTITION VALUE = 1, PARTITION OTHERS),
RANGE (b) (PARTITION 2 <= VALUES < 10);
```

Convert an existing hash partitioned table named T4 to a range partitioned table.

```sql
CREATE TABLE T4 (A INT, B INT) PARTITION BY HASH (A) PARTITIONS 2;
ALTER TABLE T4 PARTITION BY RANGE (A) (PARTITION 10 <= values < 20, PARTITION
OTHERS);
```

Convert an existing range partitioned table named T5 to a hash partitioned table.

```sql
CREATE TABLE T5 (A INT, B INT) PARTITION BY RANGE (A) (PARTITION 10 <= values
< 20, PARTITION OTHERS);
ALTER TABLE T5 PARTITION BY HASH (A) PARTITIONS 2;
```

Convert a range-range partitioned (time selection) table named T6 to a range partitioned table (convert RANGE-RANGE to RANGE).

```sql
CREATE COLUMN TABLE T6 (A INT PRIMARY KEY, B INT, _DATAAGING NVARCHAR(8))
    PARTITION BY RANGE(A) (PARTITION VALUE = 1, PARTITION 10 <= VALUES < 20,
PARTITION OTHERS), RANGE (_DATAAGING)
    (USING DEFAULT STORAGE (PARTITION value = '00000000' IS CURRENT,
    PARTITION '20100101' <= VALUES < '20110101', PARTITION OTHERS))
    WITH PARTITIONING ON ANY COLUMNS ON
    FOR NON CURRENT PARTITIONS UNIQUE CONSTRAINTS OFF
    FOR DEFAULT STORAGE NON CURRENT PARTITIONS PAGE LOADABLE;
ALTER TABLE T6 PARTITION BY RANGE(A) (PARTITION VALUE = 1, PARTITION 10 <=
VALUES < 20, PARTITION OTHERS);
```

##### Dynamic Range Partitioning

These examples are based on table A1 using this CREATE TABLE statement.

```sql
CREATE COLUMN TABLE A1 (A INT, B INT NOT NULL) PARTITION BY RANGE (A)
(PARTITION VALUES = 10),
   RANGE (B) (PARTITION VALUES = 20, PARTITION OTHERS);
```

Enable dynamic range partitioning on the OTHERS partition.

```sql
ALTER TABLE A1 PARTITION OTHERS DYNAMIC;
```

Add another partition from OTHERS.

```sql
ALTER TABLE A1 ADD PARTITION FROM OTHERS;
```

Drop any empty OTHERS partitions.

```sql
ALTER TABLE A1 DROP EMPTY PARTITIONS;
```

Change the dynamic threshold to 2, which uses the value defined in the DYNAMIC_RANGE_THRESHOLD field of the TABLE_PLACEMENT table.

```sql
ALTER TABLE A1 PARTITION OTHERS DYNAMIC THRESHOLD 2;
```

Disable dynamic range partitioning on the OTHERS partition.

```sql
ALTER TABLE A1 PARTITION OTHERS NO DYNAMIC;
```

#### Heterogeneous partitions

Convert the non-partitioned table T1 to a range-range partitioned table. The table has four firstlevel partitions (10-20,20-30,40,OTHERS). Range 10-20 has three subpartition ranges (0-10, 10-100, others). Range 40 has two subpartitions ranges (0-10, OTHERS). Both subpartitions have dynamic range partitioning enabled.

```sql
CREATE COLUMN TABLE T1 (a INT, b INT NOT NULL);
ALTER TABLE T1 PARTITION BY RANGE (a)
   ((PARTITION 10 <= VALUES < 20 INSERT OFF, PARTITION 20 <= VALUES < 30
INSERT OFF)
       SUBPARTITION BY RANGE (b) (PARTITION 0 <= VALUES < 10, PARTITION 10 <=
VALUES < 100, PARTITION OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION VALUES = 40)
       SUBPARTITION BY RANGE(B) (PARTITION 0 <= VALUES < 10, PARTITION OTHERS
DYNAMIC THRESHOLD 2),
    (PARTITION OTHERS));
```

Convert the non-partitioned table T2 to a range-hash partitioned table. The first level has two partition ranges (10-20, 20-30). The INSERT OFF property means you can't add data to the partitions. The second level is a hash with two partitions.

```sql
CREATE COLUMN TABLE T2 (a INT, b INT);
ALTER TABLE T2 PARTITION BY RANGE (a) ((PARTITION 10 <= VALUES < 20 INSERT
OFF, PARTITION 20 <= VALUES < 30 INSERT OFF)
   SUBPARTITION BY HASH (b) PARTITIONS 2);
```

Add a new firstlevel range partition 41-50 to table T1. The new partition has a subpartition with one range 0-10.

```sql
ALTER TABLE T1 ADD PARTITION RANGE (a) ((PARTITION 41 <= VALUES < 50 )
   SUBPARTITION by RANGE (b) (PARTITION 0 <= VALUES < 10 ));
```

Redefine the existing firstlevel partition range 10-20 to ranges 5-10 and 15-20. Each redefined range retains its original subpartition. All existing range values must be accounted for in the redefined structure or they will be dropped if they do not contain data.

```sql
ALTER TABLE T1 PARTITION BY RANGE (a)
   ((PARTITION 5 <= VALUES < 10, PARTITION 10 <= VALUES < 20 INSERT OFF,
PARTITION 20 <= VALUES < 30 INSERT OFF)
        SUBPARTITION BY RANGE (b) (PARTITION 0 <= VALUES < 10, PARTITION 10
<= VALUES < 100, PARTITION OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION VALUES = 40) SUBPARTITION BY RANGE(B) (PARTITION 0 <= VALUES <
10, PARTITION OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION 41 <= VALUES < 50 ) SUBPARTITION by RANGE (b) (PARTITION 0 <=
VALUES < 10),
    (PARTITION OTHERS));
```

Move partition 1 (range 5-10) on table T1 to host myhost on port 30203.

```sql
ALTER TABLE T1 MOVE PARTITION 1 TO 'myhost:30203';
```

Move range 5-10 with subpartition range 0 - 10 on table T1 to host myhost on port 30203.

```sql
ALTER TABLE T1 MOVE RANGE (a) ((PARTITION 5 <= VALUES < 10) SUBPARTITION BY
RANGE (b) (PARTITION 0 <= VALUES < 10)) TO 'myhost:30203';
```

Move the hash subpartition of range 10-20 on table T2 to host myhost1 port 30203 and myhost2 port 30203.

```sql
ALTER TABLE T2 MOVE SUBPARTITIONS OF RANGE (a) ((PARTITION 10 <= VALUES < 20)
to ('myhost1:30203', 'myhost2:30203);
```

Drop the firstlevel partition range 5-10 on table 1. The subpartitions for that range only are dropped. The subpartition ranges 10-20 and 20-30 remain.

```sql
ALTER TABLE T1 DROP PARTITION RANGE (a) (( PARTITION 10 <= VALUES < 15 ));
```

Drop subpartition range 10-100 in range 15-20 on table T1..

```sql
ALTER TABLE T1 ALTER PARTITION RANGE (a) ((PARTITION 10 <= VALUES < 20)) DROP
PARTITION RANGE (b) ((PARTITION 10 <= VALUES < 100));
```

Assign the group name GROUP1 to partition 2 on table T1.

```sql
ALTER TABLE T1 ALTER PARTITION 2 SET GROUP NAME "GROUP1";
```

Assign the group name GROUP2 and the group type HR to the partition range 10 - 20 and all its subpartitions on table T1.

```sql
ALTER TABLE T1 ALTER PARTITION RANGE (a) ((PARTITION 20 <= VALUES < 30)) SET
GROUP NAME "GROUP2" GROUP TYPE "HR" CASCADE;
```

Remove the GROUP value from partition 2 on table T1.

```sql
ALTER TABLE T1 ALTER PARTITION 2 UNSET GROUP;
```

Remove the GROUP value from the partition range 10 -20 and its subpartitions on table T1.

```sql
ALTER TABLE T1 ALTER PARTITION RANGE (a) ((PARTITION 20 <= VALUES < 30))
UNSET GROUP CASCADE;
```

This example creates a multilevel heterogeneous partitioned table and then applies the `<load_unit>` attribute first by partition number (1) and then to partition range (10 to 20).

```sql
CREATE COLUMN TABLE T4 (a INT, b INT) PARTITION BY RANGE(a)
   ( ( PARTITION 10 <= VALUES < 20 ) SUBPARTITION BY RANGE (b) ( PARTITION
VALUES = 100 ));
ALTER TABLE T4 ALTER PARTITION 1 COLUMN LOADABLE;
ALTER TABLE T4 ALTER PARTITION RANGE (a) ((PARTITION 10 <= VALUES < 20)
   SUBPARTITION BY RANGE (b) (PARTITION VALUES = 100)) PAGE LOADABLE;
```

##### Dynamic Range Partitioning

These examples are based on table A1 using this CREATE TABLE statement.

```sql
CREATE COLUMN TABLE A1 (A INT, B INT NOT NULL) PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20)
      SUBPARTITION BY RANGE (B) (PARTITION 15 <= VALUES < 20, PARTITION
OTHERS),
    (PARTITION VALUES = 30)
      SUBPARTITION BY RANGE (B) (PARTITION VALUES=20, PARTITION OTHERS),
    (PARTITION OTHERS));
```

Enable dynamic range partitioning on range 10-20, subpartition 15-20 on table A1.

```sql
ALTER TABLE A1 PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20)
      SUBPARTITION BY RANGE (B) (PARTITION 15 <= VALUES < 20, PARTITION
OTHERS DYNAMIC),
    (PARTITION VALUES = 30)
      SUBPARTITION BY RANGE (B) (PARTITION VALUES=20, PARTITION OTHERS),
    (PARTITION OTHERS));
```

Add another partition from OTHERS or subpartition 15-20 on table A1.

```sql
ALTER TABLE A1 ADD PARTITION FROM OTHERS;
```

Drop any empty OTHERS partitions on table A1.

```sql
ALTER TABLE A1 DROP EMPTY PARTITIONS;
```

Set the threshold to 2 for dynamic range partitioning on the subpartition of range 10-20 on table A1.

```sql
ALTER TABLE A1 PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20)
      SUBPARTITION BY RANGE (B) (PARTITION 15 <= VALUES < 20, PARTITION
OTHERS DYNAMIC THRESHOLD 2),
    (PARTITION VALUES = 30)
      SUBPARTITION BY RANGE (B) (PARTITION VALUES = 20, PARTITION OTHERS),
    (PARTITION OTHERS));
```

Disable dynamic range partitioning on the subpartition on range 10-20 on table A1.

```sql
ALTER TABLE A1 PARTITION BY RANGE (A)
   ((PARTITION 10 <= VALUES < 20)
      SUBPARTITION BY RANGE (B) (PARTITION 15 <= VALUES < 20, PARTITION
OTHERS),
    (PARTITION VALUES = 30)
      SUBPARTITION BY RANGE (B) (PARTITION VALUES = 20, PARTITION OTHERS),
    (PARTITION OTHERS));
```

#### Altering annotations

The following example creates a table with annotations and then alters the annotations:

```sql
CREATE COLUMN TABLE t1(c1 INT) WITH ANNOTATIONS(
    SET 't_k1'='t_v1', 't_k2'='t_v2'
    COLUMN c1 SET 'c_k1'='c_v1', 'c_k2' = 'c_v2');
ALTER TABLE t1 WITH ANNOTATIONS(
    UNSET ALL SET 'k1' = 'v1', 'k2'='v2'
    COLUMN c1 UNSET ALL SET 'k1'='v1', 'k2'='v2');
```

#### NUMA node preferences

This example immediately unsets the NUMA node preference at the table level. The table is reloaded and allocations are performed by using the HASH scheme available in the attribute engine.

```sql
ALTER TABLE T1 NUMA NODE NULL IMMEDIATE;
```

This example alters column table T1, setting the NUMA node preference at the partition level on NUMA node index 3. Since DEFERRED is specified, it sets only the NUMA preference for the partition; the actual allocations are made when the table is reloaded.

```sql
ALTER TABLE T1 PARTITION BY RANGE (colint) (PARTITION '0' <= VALUES < '20'
NUMA NODE ('3') DEFERRED);
```

This example immediately alters column table T1, setting the NUMA location preference to partition P0, which already exists. The allocations are made immediately, and the table partition is reloaded to node 4.

```sql
ALTER TABLE T1 ALTER PARTITION P0 NUMA NODE ('4') IMMEDIATE;
```

This example moves table T1 to NUMA node index 4, immediately allocating the entire table to NUMA node index 4:

```sql
ALTER TABLE T1 NUMA NODE ('4') IMMEDIATE;
```

#### Load unit

Alter the load unit for a table:

```sql
ALTER TABLE T PAGE LOADABLE CASCADE;
```

Alter the load unit of any range partition in default storage:

```sql
ALTER TABLE T PARTITION BY RANGE (C1)
   (PARTITION 0 <= VALUES < 10 PAGE LOADABLE,
    PARTITION OTHERS DEFAULT LOADABLE);
```

Add a range partition and specify the load unit:

```sql
ALTER TABLE T ADD RANGE (C1) (
   PARTITION 0 <= VALUES < 10,
   PARTITION OTHERS COLUMN LOADABLE);
```

Alter the load unit for a range partition:

```sql
ALTER TABLE T ALTER PARTITION 10 DEFAULT LOADABLE;
```

Altering the load unit for a column:

```sql
ALTER TABLE T ALTER (C1 INT DEFAULT LOADABLE);
```

## Related Information

Non-heterogeneous Alter Partition Clauses [→](4.10.01.20.01-Non-heterogeneous-Alter-Partition-Clauses.md) Heterogeneous Alter Partition Clauses [→](4.10.01.20.02-Heterogeneous-Alter-Partition-Clauses.md) CREATE SEQUENCE Statement (Data Definition) [→](../CREATE-SEQUENCE-Statement-Data-Definition.md) SELECT Statement (Data Manipulation) [→](../4.10.01.144-SELECT/README.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) REFERENTIAL_CONSTRAINTS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/REFERENTIAL_CONSTRAINTS-System-View.md) CREATE TABLE Statement (Data Definition) [→](../4.10.01.68-CREATE-TABLE/README.md) CREATE TABLE Statement (Multistore Table) [Dynamic Tiering] [→](../../../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/CREATE-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md) CREATE VIRTUAL TABLE Statement (Data Definition) [→](../CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) TABLE_PARTITIONS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md) Predicates [→](../../../4.07-Predicates/README.md) TABLES System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md)

## Contenido de esta sección

- [4.10.1.20.1 Non-heterogeneous Alter Partition Clauses](4.10.01.20.01-Non-heterogeneous-Alter-Partition-Clauses.md)
- [4.10.1.20.2 Heterogeneous Alter Partition Clauses](4.10.01.20.02-Heterogeneous-Alter-Partition-Clauses.md)
