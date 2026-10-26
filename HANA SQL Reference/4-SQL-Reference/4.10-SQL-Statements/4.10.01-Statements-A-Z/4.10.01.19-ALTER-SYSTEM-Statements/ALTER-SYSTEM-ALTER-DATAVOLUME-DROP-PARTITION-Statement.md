# 4.10.1.19.12 ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 486–488

Drops a data volume partition from all index servers in the topology or from a secondary system replication site.

## Syntax

```sql
ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION <partition_id> [ SYSTEM REPLICATION
SITE <site> ]
```

## Syntax Elements

#### partition_id

The ID of the data volume partition to drop.

#### site

Specifies the secondary site ID or name to drop the data volume partition from.

```sql
<site> ::= { <site_id> | <site_name> }
<site_id> ::= <unsigned_integer>
<site_name> ::= <string_literal>
```

## Description

Use this command to drop a data volume partition from all index servers in the current topology.

Data volume partition IDs are stored in the M_DATA_VOLUME_PARTITION_STATISTICS system view.

When an ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION statement is executed, the SAP HANA server:

1. moves all data that is stored in the partition to be dropped over to the remaining partitions. This operation can take considerable time depending on the size of the partition to be dropped.
2. removes information about the partition to be dropped from the `indexserver.ini` file.
3. removes the empty partition on each index server in the topology.

When system replication is running, you cannot drop an active data volume partition. To drop the partition, disable system replication functionality on the system, drop the partition, and re-enable system replication again.

## Example

In the example below, data volume partition `1` is dropped:

```sql
ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION 1;
```

## Related Information

ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION Statement (System Management) [→](ALTER-SYSTEM-ALTER-DATAVOLUME-ADD-PARTITION-Statement.md) M_DATA_VOLUME_PARTITION_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md)
