# 4.10.1.19.11 ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 485–486

Adds a new data volume partition to all index servers in the current tenant database or to a secondary system replication site. This statement must be executed on the indexserver, not on SystemDB.

## Syntax

```sql
ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION [ <path> ] [ SYSTEM REPLICATION SITE
<site> ]
```

## Syntax Elements

#### path

Specifies a location for the new data volume. The path must be accessible from all nodes and services that reference the data volume.

```sql
<path> ::= PATH '/<directory>[/<subdirectory>[/…]]'
```

When this option is specified, the database server creates the folder structure `mnt<xxxxx>/ hdb<yyyyy>.<zzzzz>` beneath the specified `<path>`

Use of the `<path>` option must be enabled by setting the PERSISTENCE_DATAVOLUME_PARTITION_MULTIPATH setting in `global.ini` to TRUE.

#### site

Specifies the ID or name of the secondary site for the new data volume partition.

```sql
<site> ::= { <site_id> | <site_name> }
<site_id> ::= <unsigned_integer>
<site_name> ::= <string_literal>
```

## Description

Use this command to add a new data volume partition to all index servers in the current tenant database or to a secondary system replication site.

When an ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION statement is executed without specifying the PATH option, the SAP HANA server performs the following actions:

1. reserves a new partition on all index servers in the topology. Each reservation returns the reserved partition ID on that index server. If more than one partition ID is returned, the command fails.
2. adds information about the new partition to the `indexserver.ini` file.
3. activates the reserved partitions on all index servers in the topology. Activation is complete after the next save point on each index server. Once the new partition is active, new or changed data is distributed over it, as well as over all active data volume partitions.

Data volume partition IDs are stored in the M_DATA_VOLUME_PARTITION_STATISTICS system view.

When a new datavolume partition is added, it is inactive (M) and is activated on next savepoint.

## Example

In the example below, a new data volume partition is added:

```sql
ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION;
```

In the example below, a new data volume partition is added in the specified location:

```sql
ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION PATH '/main/datavolumes';
```

## Related Information

ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION Statement (System Management) [→](ALTER-SYSTEM-ALTER-DATAVOLUME-DROP-PARTITION-Statement.md) M_DATA_VOLUME_PARTITION_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md)
