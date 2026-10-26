# 4.10.1.19.29 ALTER SYSTEM CREATE WAITGRAPH Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 515–516

Create a waitgraph file that contains thread information about deadlocks.

## Syntax

```sql
ALTER SYSTEM CREATE WAITGRAPH [ AT [ LOCATION ] <location_ref> ] [ ALL THREADS ]
[ INTO FILE <file_name> ]
<file_name> ::= <string_literal>
```

## Syntax Elements

#### location_ref

Specifies the location of the service.

```sql
<location_ref> ::= '<host>:<port>'
```

If no location is specified, then the trace folder of the specified service is used. **ALL THREADS** Includes details on all threads on the connected service, not just those that are part of the deadlock.

#### INTO FILE

Specifies the name for the dump file. If a filename is not specified, then the default file name `<servicename>_<hostname>.<port>.waitgraph.<YYYYMMDD-HHMMSS>.<pid>.trc` is used.

## Permissions

You need the RESOURCE_ADMIN system privilege.

## Description

This syntax lets you create a dump file containing information about threads that may participate in deadlocks.

## Examples

Write the current waitgraph on service myhost:30003 to the file named `my_waitgraph.trc`.

```sql
ALTER SYSTEM CREATE WAITGRAPH AT LOCATION 'myhost:30003' INTO FILE
'my_waitgraph.trc';
```

Write the current waitgraph (including all threads even if they do not participate on the deadlock) on the connected service into the file named `my_waitgraph.trc`.

```sql
ALTER SYSTEM CREATE WAITGRAPH ALL THREADS INTO FILE 'my_waitgraph.trc';
```
