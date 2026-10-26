# 4.10.1.19.16 ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 495–499

Changes table classification and placement settings for table groups.

## Syntax

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT [ ( <table_classification_settings> ) ] [ SET
| UNSET ] [ ( <table_placement_settings> ) ]
| ALTER SYSTEM ALTER TABLE PLACEMENT LOCATION <custom_location_specification>
```

## Syntax Elements

#### table_classification_settings

Specifies one or more table group options.

```sql
<table_classification_settings> ::= <classification_key_value_pair> [,<...>]
<classification_key_value_pair> ::=
 SCHEMA_NAME [=> <string_literal> ]
 | TABLE_NAME [=> <string_literal> ]
 | GROUP_NAME [=> <string_literal> ]
 | GROUP_TYPE [=> <string_literal> ]
 | SUB_TYPE [=> <string_literal> ]
```

##### SCHEMA_NAME

The schema name associated with the table (for example, SAPBWP).

##### TABLE_NAME

The table name (for example, /BIC/AZFIGL00).

##### GROUP_NAME

The table group name (for example, ZFIGL).

##### GROUP_TYPE

The table group type (for example, sap.bw.cube).

##### SUB_TYPE

The table group subtype. Possible values are ACTIVE, QUEUE, or CHANGE_LOG.

#### table_placement_settings

Specifies one or more table group placement properties.

```sql
<table_placement_settings> ::= <placement_key_value_pair> [,...]
<placement_key_value_pair> ::=
 MIN_ROWS_FOR_PARTITIONING [ => <unsigned_integer> ]
 | INITIAL_PARTITIONS [=> <unsigned_integer> ]
 | REPARTITIONING_THRESHOLD [ => <unsigned_integer> ]
 | LOCATION [ => <string_literal> ]
 | SAME_PARTITION_COUNT [ => <boolean> ]
```

##### MIN_ROWS_FOR_PARTITIONING [ => unsigned_integer]

Defines the minimum number of records that must exist in a table before level 1 partitioning takes place (for example, 40,000).

##### INITIAL_PARTITIONS [ => unsigned_integer]

Defines the initial number of partitions. If the threshold value in the MIN_ROWS_FOR_PARTITIONING column is exceeded, the table redistribution performs a partitioning (for example, 3).

##### REPARTITIONING_THRESHOLD [ => unsigned_integer]

Specifies the threshold value for the number of records in a partition that triggers a repartitioning (for example, 2,000,000,000).

Once a table has been partitioned with the specified initial number of partitions, for performance reasons, the table is only repartitioned by doubling the number of partitions. For example, if the initial number of partitions is 3, this would result in 6 partitions being created during a repartitioning.

##### LOCATION [=> string_literal]

Specifies one or more indexserver volume IDs (values are MASTER, DEFAULT, SLAVE, and ALL), or the name of a custom set of indexservers previously defined (`<custom_location_specification>`) using the ALTER TABLE ALTER TABLE PLACEMENT LOCATION syntax.

##### SAME_PARTITION_COUNT [ => boolean]

Specifies that all partitions of the tables in a group will contain the same number of partitions.

#### LOCATION custom_location_specification

Defines a synonym for a list of one or more SAP HANA indexservers, or groups of indexservers, by their intended use; for example, as a worker for a specific application to isolate the workload, or to define a custom subset of indexservers that host data of a specific customer. This capabilitity relies more on volume IDs instead of host/port names.

```sql
LOCATION <custom_location_specification> ::= <custom_location_names> { SET
<location_specification> | UNSET }
```

##### custom_location_names

Specifies a synonym for one or more volum IDs to use for table placement. You can then reference this name when specifying table placement settings using the ALTER TABLE ALTER TABLE PLACEMENT syntax.

##### SET location_specification

Specifies the locations to include or exclude during table placement.

```sql
<location_specification> ::= { [ <include_list> [, <exclude_list> ] ] }
<include_list> ::= INCLUDE=>'[ { <preset_value> [, ...] | <volumn_id>
[,...] ] }'
<exclude_list> ::= EXCLUDE=>'[ { <preset_value> [, ...] | <volumn_id>
[,...] ] }'
<preset_value> ::= { MASTER | ALL | DEFAULT | SLAVE }
```

##### UNSET

Unsets the locations configured for the specified `<custom_location_specification>`.

If `<custom_location_specification>` is UNSET while also being the table placement setting currently in use, SAP HANA reverts to default table placement behaviors.

## Description

This statement allows you to set and unset attributes and placement properties for table groups. When you create a table, you can assign it to a table group. Table groups can improve the database server's ability to make decisions about how to distribute tables across servers. For example, the use of table groups can prevent frequently-joined tables from being placed on different hosts.

Table classification and the table placement settings are taken into account on two occasions: table redistribution and during table creation.

Table placement attributes and properties are stored in the TABLE_GROUPS and TABLE_PLACEMENT_LOCATIONS system views and their corresponding monitoring view counterparts..

## Permissions

You must have the TABLE ADMIN to execute this statement.

## Examples

The following statement forces all tables to be stored on the `slave` host.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT SET (LOCATION => 'slave');
```

The following statement forces all tables of the schema SAPKIT to be stored on the `master` host.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME => 'SAPKIT') SET (LOCATION =>
'master');
```

The following statement forces all tables of the schema SAPKIT and the GROUP_TYPE `sap.bw.dso` to be stored on the `slave` host with the specified properties.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME => 'SAPKIT', GROUP_TYPE =>
'sap.bw.dso')
 SET (LOCATION => 'slave', MIN_ROWS_FOR_PARTITIONING => 40000000,
REPARTITIONING_THRESHOLD => 40000000, INITIAL_PARTITIONS => 3);
```

The following example demonstrates how to unset the schema entry SAPKIT and GROUP_TYPE `sap.bw.dso`.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME => 'SAPKIT', GROUP_TYPE =>
'sap.bw.dso') UNSET;
```

The following example demonstrates how to remove the LOCATION entry for schema SAPKIT and GROUP_TYPE `sap.bw.dso`.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME => 'SAPKIT', GROUP_TYPE =>
'sap.bw.dso') UNSET (LOCATION);
```

The following example demonstrates how to set the SAME_PARTITION_COUNT table placement property for schema `SYSTEM` to `'TRUE'`.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME=>'SYSTEM') SET
(SAME_PARTITION_COUNT => 'TRUE');
```

The following example demonstrates how to unset the SAME_PARTITION_COUNT table placement property for schema `SYSTEM`.

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT (SCHEMA_NAME=>'SYSTEM') UNSET
(SAME_PARTITION_COUNT);
```

The following examples demonstrate how to include or exclude locations for table placement:

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT LOCATION MyLocation SET (INCLUDE => '2,3',
EXCLUDE => 'SLAVE');
ALTER SYSTEM ALTER TABLE PLACEMENT LOCATION MyLocation SET (INCLUDE => '2,3',
EXCLUDE => '');
```

The following example unsets the list of locations that have been set for table placement:

```sql
ALTER SYSTEM ALTER TABLE PLACEMENT LOCATION MyLocation UNSET;
```

## Related Information

TABLE_PLACEMENT System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_PLACEMENT-System-View.md) M_EFFECTIVE_TABLE_PLACEMENT System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_EFFECTIVE_TABLE_PLACEMENT-System-View.md) TABLE_PLACEMENT_LOCATIONS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_PLACEMENT_LOCATIONS-System-View.md) M_TABLE_PLACEMENT_LOCATIONS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PLACEMENT_LOCATIONS-System-View.md) TABLE_GROUPS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/TABLE_GROUPS-System-View.md)
