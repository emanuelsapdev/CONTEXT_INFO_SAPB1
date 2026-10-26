# 5.2.10 ALTER TABLE Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1250–1264

Alters the definition of a multistore table.

## Syntax

```sql
ALTER TABLE <table_name>
   [ <add_column_clause>]
   [ <drop_column_clause>]
   [ <alter_column_clause>]
   [ <add_constraint_clause>]
   [ <drop_primary_key_clause>]
   [ <drop_constraint_clause>]
   [ <move_column_store_partition_clause>]
   [ <persistent_merge_clause>]
   [ <delta_log_clause>]
   [ <auto_merge_clause>]
   [ <unload_priority_clause>]
   [ <set_group_clause>]
   [ <unset_group_clause>]
   [ <reclaim_data_space_clause>]
   [ <non-heterogeneous_partition_clauses>
   [ <heterogeneous_partition_clauses>
   [ <enable_delta_for_extended_storage>]
   | [ <owner_to_clause>]
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
ADD ( {<column_definition> [<column_constraint_short>]
 [COMMENT <string_literal>] } [, …] )
```

##### column_definition

Defines a table column.

```sql
<column_definition> ::= <column_name> <data_type>
   |<lob_data_type>} [<default_value_clause>]
```

##### column_name

The table column name.

```sql
<column_name> ::= <identifier>
```

##### data_type

The available data types.

```sql
<data_type> ::= DATE
   | TIME
   | SECONDDATE
   | TINYINT
   | SMALLINT
   | INTEGER
   | BIGINT
   | DECIMAL [, ]
   | REAL
   | DOUBLE
   | VARCHAR [ (<unsigned_integer>) ]
   | NVARCHAR [ (<unsigned_integer>) ]
   | VARBINARY [ (<unsigned_integer>) ]
```

##### lob_data_type

Specifies the column constraint rules.

```sql
<lob_data_type> ::= BLOB
   | CLOB
   | NCLOB
```

##### column_constraint_short

```sql
<column_constraint_short> ::= NULL | NOT NULL
```

##### NULL

If NULL is specified it is not considered a constraint, it represents that a column that may contain a null value. The default is NULL.

##### NOT NULL

The NOT NULL constraint prohibits a column value from being NULL.

##### default_value_clause

Specifies a value to be assigned to the column if an INSERT statement does not provide a value for the column.

```sql
<default_value_clause>  ::= DEFAULT <default_value_exp>
```

```sql
<default_value_exp> ::= NULL
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

#### drop_column_clause

Removes columns from the specified table. Columns must be dropped one at a time.

```sql
<drop_column_clause> ::= DROP ( <column_name>)
```

#### alter_column_clause

Alters a column definition.

```sql
<alter_column_clause> ::=
   ALTER ( <column_definition>
   [<column_constraint>] )
```

For more information on column definition, see column_definition [→](ALTER-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md).

Restrictions:

- To prevent data loss, you can only increase the size of a column data type. For example, changing from nvarchar(20) to nvarchar(10) or from integer to tinyint raises an error.
- ALTER does not currently follow data type conversion rules. Adding the NOT NULL constraint to an existing column is allowed if either of the following cases are true:
  - The table is empty.
  - The table does not contain a NULL-value in that column.
- Primary keys (or secondary indexes) with multiple columns are not allowed in these conditions:
  - When the total key length (sum of all column sizes) is greater than 5300 bytes.
  - When the column types include NVARCHAR and at least one column has a length greater than 1765 bytes.
- Columns with data type TEXT are not supported.
- You cannot drop or modify a partition key column.
- Multistore tables only support adding, dropping, or modifying columns one column at a time.

#### column_constraint

Specifies all column constraints.

```sql
<column_constraint>::=
   NULL
   | NOT NULL
   | <unique_specification>
```

##### NULL

If specified, it is not considered a constraint, but represents a column that may contain a null value. The default is NULL.

##### NOT NULL

Prohibits a column value from being NULL.

##### unique_specification

Specifies unique constraints.

```sql
<unique_specification>::= UNIQUE [<unique_tree_type_index>]
    | PRIMARY KEY [<unique_tree_type_index> ]
```

If you omit the index type, the SAP HANA database chooses the appropriate index automatically based on data type or constraint:

- CPBTREE:
  - Character string types
  - Binary string types
  - Decimal types
  - When the constraint is a composite key
  - When the constraint is a non-unique constraint
- BTREE: All other cases than specified for CPBTREE

##### PRIMARY KEY

A primary key constraint is a combination of a NOT NULL constraint and a UNIQUE constraint. It prohibits multiple rows from having the same value in the same column.

##### unique_tree_type_index

Specifies the index type.

```sql
<unique_tree_type_index> ::= BTREE | CPBTREE;
```

##### BTREE

BTREE specifies a B+ tree index. B+ tree is a tree that maintains sorted data, which performs efficient insertion, deletion and search of records.

##### CPBTREE

CPBTREE specifies a CPB+ tree index. CPB+ tree stands for Compressed Prefix B+ tree, which is based on pkB tree. CPB+ tree is a very small index because it uses partial key that is only part of full key in index nodes. CPB+ tree shows better performance than B+ tree for larger keys.

#### add_constraint_clause

Adds a table constraint.

```sql
<add_constraint_clause> ::=
   ADD [CONSTRAINT <constraint_name>]
   <table_constraint> [FOR {DEFAULT|EXTENDED} STORAGE]
```

```sql
<constraint_name> ::= <identifier>
```

##### table_constraint

Only unique constraints are supported on a multistore table.

```sql
<table_constraint> ::= <unique_constraint_definition>
```

##### unique_constraint_definition

The unique specification.

```sql
<unique_constraint_definition> ::= <unique_specification>
....(<unique_column_name_list>)
```

##### unique_constraint_definition

Specifies the unique column name list, which can have one or more column names.

```sql
<unique_column_name_list> ::= <unique_column_name>
[{,<unique_column_name>}...]
```

##### unique_column_name

A column name identifier.

```sql
<unique_column_name> ::= <identifier>
```

##### FOR {DEFAULT|EXTENDED} STORAGE]

Specifies the location on a multistore table where the constraint is internally created. You may create the constraint as a partial index on either the default or extended storage. If you don't specify storage, the constraint is created on both the default and extended storage.

#### drop_primary_key_clause

Drops the primary key constraint.

```sql
<drop_primary_key_clause> ::= DROP PRIMARY KEY [FOR {DEFAULT|EXTENDED}
STORAGE]
```

If you drop a primary key on a partial index for a multistore table, you may drop it from the store where it resides. For example, FOR DEFAULT STORAGE drops the default store part of the primary key. If you don't specify storage, the primary key is totally dropped.

#### drop_constraint_clause

Drops a unique constraint.

```sql
<drop_constraint_clause> ::= DROP CONSTRAINT<constraint_name> [FOR {DEFAULT|
EXTENDED} STORAGE]
<constraint_name> ::= <identifier>
```

If you drop a constraint created as a partial index, you may drop it from the store where it resides and convert it into a partial index on the other store. For example, FOR DEFAULT STORAGE drops the constraint from the default store and converts it into a partial index on the extended store. If you don't specify storage, the constraint is totally dropped.

#### move_column_store_partition_clause

Moves a table or partition to another indexserver location in a distributed environment

> **Note**
>
> The `<move_clause>` parameter is only supported on column store partitions.

```sql
<move_column_store_partition_clause> ::= MOVE [ PARTITION <partition_number> ]
   TO <indexserver_host_port> [PHYSICAL]
   | MOVE [PARTITION <partition_number>] PHYSICAL
```

##### partition_number

Specifies the partition to be moved. You see an error if you try to move a partitioned table without specifying `<partition_number>`.

```sql
<partition_number> ::= <unsigned_integer>
```

##### indexserver_host_port

The internal indexserver host name and port number where the table is to be moved.

```sql
<indexserver_host_port> ::= 'host_name:port_number'
```

##### PHYSICAL

The PHYSICAL keyword is only for column store tables. Row store tables are always moved immediately.

#### persistent_merge_clause

Enables or disables persistent merging.

> **Note**
>
> The `<persistent_merge_clause>` parameter is supported on column store partitions.

```sql
<persistent_merge_clause> ::= { ENABLE | DISABLE } PERSISTENT MERGE
```

- (Default) When enabled, the merge-manager uses persistent merges for the given column store table.
- When disabled, the merge-manager uses main-memory merges instead of persistent merges for the given column store table.

#### delta_log_clause

Enables or disables the redo log for the table.

> **Note**
>
> The `<delta_log_clause>` parameter is supported on column store partitions.

```sql
<delta_log_clause> ::= { ENABLE | DISABLE } DELTA LOG
```

Use this clause only during initial load.

If you enable logging, perform a savepoint afterward to make sure that all data persists. Next, perform a data backup so that you can recover the data.

If you disable logging, log entries do not persist for this table and savepoints only write changes to the data store. This can cause loss of committed transactions if the indexserver terminates, in which case you have to truncate this table and insert all data again.

#### auto_merge_clause

Enables or disables automatic delta merge on the specified table.

The `<auto_merge_clause>` parameter is supported on column store partitions.

If not specified, the table move will create a link inside. Specifies that a column store tables persistence storage is moved immediately to the target host. If the PHYSICAL option parameter is supported on the new host persistence pointing to the old host persistence. The link will be removed on the next merge or column store partitions. upon execution of another move operation not using the TO is not specified the table move will create a link inside the new host persistence pointing to the old host.

```sql
<auto_merge_clause> ::= { ENABLE | DISABLE } AUTOMERGE
```

#### unload_priority_clause

Specifies that priority of table to be unloaded from memory.

> **Note**
>
> The `<unload_priority_clause>` parameter is supported on column store partitions.

```sql
<unload_priority_clause> ::= UNLOAD PRIORITY <unload_priority>
<unload_priority> ::= <digit>
```

#### set_group_clause

Sets the group type, subtype, and name.

```sql
<group_clause> ::=  SET <group> [ <group> ... ]
```

```sql
<group> ::=
   GROUP TYPE <identifier>
   | GROUP SUBTYPE <identifier>
   | GROUP NAME <identifier>
```

Grouping applies only to column store partitions within a multistore table.

#### unset_group_clause

Unsets the group type, subtype, and name.

```sql
<unset_group_clause> ::=  <UNSET GROUP>
```

#### reclaim_data_space_clause

Reclaims data space of the specified table.

> **Note**
>
> The `<reclaim_data_space_clause>` parameter is a row-only clause not supported on column store tables.

```sql
<reclaim_data_space_clause> ::= RECLAIM DATA SPACE
```

This statement defragments your database by restructuring table data space. However, this does not always guarantee that restructured data space uses less memory than before. In some optimized cases, restructured data space uses much memory.

#### non-heterogeneous_partition_clauses

Alter operations you can perform on a non-heterogeneous partitioned multistore table.

```sql
[ <add_range_clause>]
[ <drop_range_clause>]
[ <redefine_range_clause>
[ <alter_range_partition_attributes_clause>
[ <move_range_clause>]
```

You cannot convert a partitioned column store or extended store table directly to a non-heterogeneous partitioned multistore table. It requires multiple ALTER TABLE commands. For more information, see the Manage a Multistore Table section in the SAP HANA Dynamic Tiering Administration Guide.

##### add_range_clause

Adds a range partition to an existing multistore table with a non-heterogeneous partitioning scheme.

```sql
<add_range_clause> ::=
ADD PARTITION  ( <column_name> ) USING {DEFAULT | EXTENDED } STORAGE
( <range_values> )
```

Only one range can be added at a time. The USING {DEFAULT | EXTENDED } STORAGE parameter is required when adding a range to an extended storage partition, but optional for a default storage partition. This clause is not supported if you want to add a range to an extended storage partition and PARTITION OTHERS exists in default storage. For this scenario, you must use both the `<redefine_range_clause>` and `<move_range_clause>` clauses. For more information, see the Manage a Multistore Table section in the SAP HANA Dynamic Tiering Administration Guide.

**column_name** Specifies the name of the existing partitioning column the range refers to.

###### range_values

Specifies the range of the partition.

```sql
<range_values> ::= <min_value> <= VALUES < <max_value>
    | VALUES = <target_value>
    | OTHERS
```

###### min_value

The lower value of a partition specifier. Value cannot be negative.

```sql
<min_value> ::= <string_literal> | <numeric_literal>
```

###### max_value

The upper value of a partition specifier. Value cannot be negative.

```sql
<max_value> ::= <string_literal> | <numeric_literal>
```

###### target_value

The target value of a single partition specifier. Value cannot be negative.

```sql
<target_value> ::= <string_literal> | <numeric_literal>
```

###### OTHERS

Specifies that all other values that are not covered by the partition range values will be gathered into one partition. OTHERS can only be defined within a default store partition.

##### drop_range_partition_clause

Specifies the range of the partition to drop. Only a single range can be dropped at a time.

```sql
<drop_range_partition_clause> ::= DROP PARTITION ( <column_name> )
<range_values>
```

##### redefine_range_clause

Modifies the ranges of an existing non-heterogeneous partition.

```sql
<redefine_range_clause> ::=
    PARTITION BY RANGE (<column_name>)
    ( USING DEFAULT STORAGE ( <range_values> [ ,<range_values> ] )
      USING EXTENDED STORAGE ( <range_values> [ ,<range_values> ] ) );
```

You can add new ranges or split or merge existing ranges as long as the new ranges provide a valid partition for all existing data within the table, and no data moves between stores as a result of the redefined ranges. If the redefined ranges results in existing data falling outside of the ranges, or moving to a different store the alter command fails. If a partition is empty, and it is not included in the redefined ranges, then it is dropped.

For example, range 10-20 resides in default storage and range 20-30 resides in extended storage. The values 10 through 17 are inserted. If range 10-20 is redefined as 10-15, then the command fails because the new range excludes the existing values of 16 and 17. However, if the range is redefined to 10-18, then the command succeeds because all of the existing data is still included in the redefined range. If the range in default storage is redefined to 10-15 and in extended storage to 15-30, then the command fails because even though all the data is still included within the ranges, the redefined ranges would result in the values 16 and 17 moving to extended storage.

##### alter_range_partition_attributes_clause

Defines attributes on the partition.

```sql
<alter_range_partition_attributes_clause> ::=
    FOR NON CURRENT PARTITIONS UNIQUE CONSTRAINTS { ON | OFF }
    |  FOR DEFAULT STORAGE {ALL | NON CURRENT } PARTITIONS { PAGE |
COLUMN } LOADABLE
```

##### move_range_clause

Moves an existing partition range between stores. Only one range can be moved at a time.

```sql
<move_range_clause>  ::= ALTER PARTITION ( <column_name> )
    [ USING DEFAULT STORAGE | USING EXTENDED STORAGE ] ( <range_values> )
```

#### heterogeneous_partition_clauses

Alter operations you can perform on a heterogeneous partitioned multistore table.

```sql
[ <add_heterogeneous_range_clauses>]
[ <drop_heterogeneous_partition_clauses>]
[ <move_heterogeneous_partition_clause>]
[ <redefine_heterogeneous_range_clause>]
[ <alter_heterogeneous_partition_primary_key_clause> ]
```

You cannot convert a partitioned column store or extended store table directly to a heterogeneous partitioned multistore table. It requires multiple ALTER TABLE commands. For more information, see the Manage a Multistore Table section in the SAP HANA Dynamic Tiering Administration Guide. **add_heterogeneous_range_clauses** Alter operations you can perform to add new first or second-level range partitions to an existing multistore table.

##### add_het_range_partition_clause

Adds a range partition to either store. You must add at least one subpartition when initially adding the partition to be able to add additional subpartitions later.

```sql
<add_het_range_partition_clause> ::=
    ADD PARTITION RANGE (<column_name>)
    ( ( PARTITION <het_range_spec> <het_location>[, PARTITION
<het_range_spec> <het_location> ...]
         SUBPARTITION BY RANGE (<column_name>) ( PARTITION
<het_range_spec> [, PARTITION <het_range_spec> ...] ) );
<het_range_spec>::= <het_range_values> [INSERT {OFF | ON} ]
```

**column_name** Specifies the name of the existing partitioning column the range is being added to.

###### het_range_values

Specifies the range of the partition.

```sql
<het_range_values> ::= <min_value> <= VALUES < <max_value>
    | VALUES = <target_value>
    | OTHERS
```

###### min_value

The lower value of a partition specifier. Value cannot be negative.

```sql
<min_value> ::= <string_literal> | <numeric_literal>
```

###### max_value

The upper value of a partition specifier. Value cannot be negative.

```sql
<max_value> ::= <string_literal> | <numeric_literal>
```

###### target_value

The target value of a single partition specifier. Value cannot be negative.

```sql
<target_value> ::= <string_literal> | <numeric_literal>
```

###### OTHERS

Specifies that all other values that are not covered by the partition specification will be gathered into one partition. Can only be added to a default store partition.

###### INSERT { ON | OFF }

(Applies to heterogeneous range partitions only) Specifies if INSERT statements are allowed on a partition. The INSERT parameter can be defined on a first or second level partition. If defined at the first level, it applies to all second level partitions within the first level partition. If defined at both the first and second level, any value at the second level overrides the first level value. If not specified, default is ON.

###### het_location

Specifies where the partition resides. If a location is not specified, the partition resides in default storage.

```sql
<location> ::= AT LOCATION
   { '<HANA_host>:<HANA_port>'
   | '<ES_host>:<ES_port>' }
```

##### add_het_range_subpartition_clause

Adds second-level range partitions to existing firstlevel range partitions.

```sql
<add_het_range_subpartition_clause> ::=
    ALTER PARTITION RANGE (<column_name>) ( ( PARTITION <het_range_values>
[, PARTITION <het_range_values> ...] ) )
    ADD PARTITION RANGE (<column-name>) ( ( PARTITION <het_range_values>
[, PARTITION <het_range_values> ...] ) )
```

The existing firstlevel ranges specified can be in either store. When multiple firstlevel partitions are specified, the subpartitions are added to each firstlevel partition. You can add the same subpartition range to multiple firstlevel partitions regardless of their store at the same time. For example, in a single ALTER statement, you could add the subpartition 500-1000 to first level-partitions 10-20 and 20-30, in default storage, and partitions 30-40 in extended storage.

#### drop_heterogeneous_partition_clauses

Drops first or second-level range partitions. Dropping a firstlevel range partition drops all associated subpartitions and deletes any data contained within the partition or associated subpartitions.

##### drop_het_range_partition_clause

Specifies the first level range being dropped.

```sql
<drop_het_range_partition_clause> ::=
   DROP PARTITION RANGE ( <column_name> )
      ( ( PARTITION <range_values> [, PARTITION <range_values> ...] ) )
```

##### drop_het_range_subpartition_clause

Drop a subpartition from a first level range partition. Dropping the last subpartition deletes the first level partition as well.

```sql
<drop_heterogeneous_subpartition_clause> ::=
   ALTER PARTITION RANGE (<column_name >)
      ( (PARTITION <range_values> [, PARTITION <range_values>...) )
        DROP PARTITION RANGE (<column_name>) ( ( PARTITION <range_values>
[,PARTITION <range_values> ...] ) )
```

#### move_heterogeneous_partition_clause

Move a firstlevel partition on a heterogeneous range multistore table to a new store. Any second level partitions associated with the partition being moved are also moved. The partition being moved must be a standalone defined range. To move part of an existing range, alter the partition range to isolate the part and then move it. Moving a partition requires the `<partition_number>` of the partition. To locate this value, execute:

```sql
SELECT * FROM table_partitions
```

The `<partition_number>` is the value in the `LEVEL_1_PARTITION` column on the row of the range to move.

```sql
<move_heterogeneous_partition_clause> ::= MOVE PARTITION <partition_number>
TO <move_location>
```

##### move_location

Specifies the location the partition is being moved to. The new location can be within the default store on a different indexserver or the extended store on the dynamic tiering server.

```sql
<move_location>::=
   '<hana_host>:<port>'
   | '<es_server_host>:<port>'
```

#### redefine_heterogeneous_range_clause

Modifies the existing ranges and INSERT property of first and second-level partitions. The new ranges must provide a valid partition for all existing data within the table. If a partition or subpartition is empty, and it is not included in the redefined ranges, it is dropped. Data cannot move between stores as a result of the redefined ranges.

```sql
<redefine_heterogeneous_range_clause> ::= PARTITION BY RANGE (<column_name>)
   ( ( PARTITION <range_values> [, PARTITION <range_values> ...]
         [ SUBPARTITION BY RANGE (<column_name>) ( PARTITION <range_values>
[,PARTITION <range_values> ...] ) ],
     ( PARTITION <range_values> [, PARTITION <range_values> ...]
         [ SUBPARTITION BY RANGE (PARTITION <column_name>) ( PARTITION
<range_values> [,<partition_subrange> ...] ) ]
   )  [ PRIMARY KEY UPDATE { ON | OFF } ]
```

#### alter_heterogeneous_partition_primary_key_clause

Specifies if UPDATE statements are allowed on primary key columns.

```sql
<alter_heterogeneous_partition_primary_key_clause> ::= PRIMARY KEY UPDATE {ON
| OFF}
```

#### enable_delta_for_extended_storage

Specifies whether extended storage is to use row-level versioning. This clause applies only to extended storage partitions in a multistore table.

```sql
<enable_delta_for_extended_storage> ::=
FOR EXTENDED STORAGE [ ENABLE | DISABLE ] DELTA
```

#### owner_to_clause

Specifies a new owner for the table.

```sql
<owner_to_clause> ::= OWNER TO <user_name>
```

The new owner becomes the grantor for all of the privileges on the table that were granted by the old owner. Also, the old owner is granted all privileges for the table by the new owner so that they can continue running jobs on the table.

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The ALTER TABLE (multistore table) statement changes the definition of a multistore table.

When managing partitions on a multistore table, refer to the section Manage a Multistore Table in the SAP HANA Dynamic Tiering Administration Guide for details and specific examples on supported clause behaviors.

## Examples

The following examples are based on multistore table t2:

```sql
CREATE TABLE t2 (a int primary key, b int)
   PARTITION BY HASH (a) PARTITIONS 2,
   RANGE (b)
     (USING DEFAULT STORAGE (PARTITION 1 <= VALUES < 10 )
      USING EXTENDED STORAGE (PARTITION 10 <= values <20 ));
```

This example adds column c with a data type in integer to the existing table t2.

```sql
ALTER TABLE t2 ADD (c int);
```

This example changes the data type of column c from integer to date on table t2.

```sql
ALTER TABLE t2 ALTER (c DATE);
```

This example removes column c from table t2.

```sql
ALTER TABLE t2 DROP (c);
```

This example adds the unique constraint UK to multistore table t2.

```sql
ALTER TABLE t2 ADD CONSTRAINT UK UNIQUE (B);
```

This example drops contraint UK from table t2.

```sql
ALTER TABLE t2 DROP CONSTRAINT UK;
```

This example sets a group type named test on table t2.

```sql
ALTER TABLE t2 SET GROUP TYPE "test";
```

This example removes the group from table t2.

```sql
ALTER TABLE t2 UNSET GROUP;
```

This example changes the owner of table t2 to user1.

```sql
ALTER TABLE t2 OWNER to user1;
```

#### Partitioning

This example enables delta or disables on extended storage on table t2. It syntax works on both non- and heterogeneous range multistore tables.

```sql
ALTER TABLE t2 FOR EXTENDED STORAGE ENABLE DELTA;
```

```sql
ALTER TABLE t2 FOR EXTENDED STORAGE DISABLE DELTA;
```

#### Non-heterogeneous Partitioning

The following examples are based on this non-heterogeneous partitioned multistore table:

```sql
CREATE COLUMN TABLE t1 (a INT, b INT)
    PARTITION BY RANGE (b)
    ( USING DEFAULT STORAGE ( PARTITION 10 <= VALUES < 15, PARTITION 15 <=
VALUES < 30)
      USING EXTENDED STORAGE ( PARTITION 30 <= VALUES < 40, PARTITION 40 <=
VALUES < 50) );
```

This example adds partition 5-10 to default storage.

```sql
ALTER TABLE t1 ADD PARTITION (b)
    USING DEFAULT STORAGE (5 <= VALUES < 10);
```

This example adds partition 60-70 to extended storage.

```sql
ALTER TABLE t1 ADD PARTITION (b)
    USING EXTENDED STORAGE (60 <= VALUES < 70);
```

This example redefines the existing default storage partitions on a range partitioned table. It splits range 15-30 in to 15-20 and 20-30. It also adds the OTHERS partition to default storage:

```sql
ALTER TABLE t1 PARTITION BY RANGE (b)
    ( USING DEFAULT STORAGE ( PARTITION 10 <= VALUES < 15, PARTITION 15 <=
VALUES < 20,
          PARTITION 20 <= VALUES < 30, PARTITION OTHERS)
      USING EXTENDED STORAGE ( PARTITION 30 <= VALUES < 40, PARTITION 40 <=
VALUES < 50) );
```

This example drops partition range 10-15.

```sql
ALTER TABLE t1 DROP PARTITION (b) 10 <= VALUES < 15;
```

This example moves partition range 15-20 from default storage to extended storage.

```sql
ALTER TABLE t1 USING EXTENDED STORAGE 15 <= VALUES < 20;
```

#### Heterogeneous Range Partitioining

The following examples are based on this heterogeneous range partitioned table:

```sql
CREATE COLUMN TABLE t2 (a INT, b INT)
    PARTITION BY RANGE(a)
    ( (PARTITION 5 <= VALUES < 10, PARTITION 10 <= VALUES < 15, PARTITION 15
<= VALUES < 20 USING DEFAULT STORAGE)
            SUBPARTITION BY RANGE (b) (PARTITION VALUES = 100),
      (PARTITION 50 <= VALUES < 60 USING EXTENDED STORAGE)
            SUBPARTITION BY RANGE (b) (PARTITION VALUES = 200) );
```

This example redefines two existing extended storage partition range, 5-10 and 10-15 into a single partition range.

```sql
ALTER TABLE t2 PARTITION BY RANGE (a)
    ( (PARTITION 5 <= VALUES < 15, PARTITION 15 <= VALUES < 20 )
            SUBPARTITION BY RANGE (b) (PARTITION 100 <= VALUES < 150),
      (PARTITION 50 <= VALUES < 60)
            SUBPARTITION BY RANGE (b) (PARTITION VALUES = 200)  );
```

This example adds firstlevel range partition 60-70 and subpartition 100-200 to extended storage.

```sql
ALTER TABLE t2 ADD PARTITION RANGE (a)
    ( ( PARTITION 60 <= VALUES < 70 AT LOCATION 'myDTserver:30112')
       SUBPARTITION BY RANGE (b) (PARTITION 100 <= VALUES < 200) );
```

This example adds subpartition value=200 to range partition 15-20 in default storage.

```sql
ALTER TABLE t2 ALTER PARTITION RANGE (a)
    ( ( PARTITION 15 <= VALUES < 20 ) )
       ADD PARTITION RANGE (b) ( ( PARTITION VALUES = 200 ) );
```

This example adds the OTHERS partition to default storage.

```sql
ALTER TABLE t2 ADD PARTITION RANGE (a)
    ( ( PARTITION OTHERS ) );
```

This example drops only subpartition 200 from range 15-20. Range 15-20 remains.

```sql
ALTER TABLE t2 DROP PARTITION RANGE (a)
( ( PARTITION 15 <= VALUES < 20 ) );
```

This example drops partition 60-70 from extended storage. This also drop its subpartition 100-200.

```sql
ALTER TABLE t2 DROP PARTITION RANGE (a)
    ( ( PARTITION 60 <= VALUES < 70 ) );
```

This example moves partition 5-15, which is partition 1 to extended storage.

```sql
ALTER TABLE T2 MOVE PARTITION 1 TO 'myDTserver:30112';
```

This example adds the ability to run UPDATE statements on the primary key in the multistore table.

```sql
ALTER TABLE T2 PRIMARY KEY UPDATE ON;
```

## Related Information

TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) PARTITIONED_TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/PARTITIONED_TABLES-System-View.md) TABLE_PARTITIONS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md) CREATE TABLE Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md) TABLES System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_PARTITIONS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md) TABLE_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) M_ES_TABLES System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md)
