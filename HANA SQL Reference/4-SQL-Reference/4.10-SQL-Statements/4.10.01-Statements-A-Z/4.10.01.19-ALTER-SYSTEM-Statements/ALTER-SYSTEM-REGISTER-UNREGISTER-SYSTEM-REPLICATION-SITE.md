# 4.10.1.19.9 ALTER SYSTEM {REGISTER | UNREGISTER} SYSTEM REPLICATION SITE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 480–482

Register or unregister a system replication secondary site.

## Syntax

```sql
ALTER SYSTEM {REGISTER | UNREGISTER} SYSTEM REPLICATION SITE <site_name>
REMOTE HOST <remote_host_name> REPLICATION MODE <replication_mode>
[ OPERATION MODE <operation_mode> ] [ FORCE ] [ FULL REPLICA ]
```

## Syntax Elements

**site_name** The name of the secondary site.

```sql
<site_name> ::= <identifier>
```

**remote_host_name** The hostname of the primary site master host.

```sql
<remote_host_name> ::= <string>
```

**replication_mode** The system replication mode.

```sql
<replication_mode> ::= 'sync'
| 'syncmem'
| 'async'
```

**operation_mode** The system replication operation mode.

```sql
<operation_mode> ::= 'delta_datashipping'
| 'logreplay'
| 'logreplay_readaccess'
```

**[FORCE]** This optional clause omits host-mapping checks. **[FULL REPLICA]** This optional clause forces an initial full data shipping.

## Description

Attach or remove a secondary site to a system replication primary system.

## Example

The following statement registers the secondary site SiteB to the remote host `<primary_host>`.

```sql
ALTER SYSTEM REGISTER SYSTEM REPLICATION SITE 'SiteB'
REMOTE HOST '<primary_host>' REPLICATION MODE 'sync'
OPERATION MODE 'logreplay';
```

## Related Information

ALTER SYSTEM {ENABLE | DISABLE} SYSTEM REPLICATION Statement (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-SYSTEM-REPLICATION-Statement.md) ALTER SYSTEM {ENABLE | DISABLE} ALL [ASYNCHRONOUS | SYNCHRONOUS] TABLE REPLICAS Statement (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-ALL-ASYNCHRONOUS-SYNCHRONOUS.md)
