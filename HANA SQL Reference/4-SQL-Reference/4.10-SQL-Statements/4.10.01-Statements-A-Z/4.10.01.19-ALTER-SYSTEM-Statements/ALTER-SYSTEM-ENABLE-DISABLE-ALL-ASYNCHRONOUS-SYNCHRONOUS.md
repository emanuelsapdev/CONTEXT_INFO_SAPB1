# 4.10.1.19.5 ALTER SYSTEM {ENABLE | DISABLE} ALL [ASYNCHRONOUS | SYNCHRONOUS] TABLE REPLICAS Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 474–476

Activates or deactivates the overall replication operation of all replication tables or of asynchronous or synchronous tables only.

## Syntax - Table Replica

```sql
ALTER SYSTEM { ENABLE | DISABLE } ALL [ ASYNCHRONOUS | SYNCHRONOUS ] TABLE
REPLICAS
```

## Syntax Elements

#### ENABLE

Activates the overall replication operation of all specified replication tables.

#### DISABLE

Deactivates the overall replication operation of all specified replication tables.

#### ASYNCHRONOUS

Applies the operation to all asynchronous tables.

#### SYNCHRONOUS

Applies the operation to all synchronous tables.

## Description

Activates or deactivates the overall replication operation of all replication tables or of asynchronous or synchronous tables.

## Permissions

The use of this statement requires the SERVICE ADMIN privilege.

## Examples

Activate all synchronous table replication.

```sql
ALTER SYSTEM ENABLE ALL SYNCHRONOUS TABLE REPLICAS;
```

Deactivate all asynchronous table replication.

```sql
ALTER SYSTEM DISABLE ALL ASYNCHRONOUS TABLE REPLICAS;
```

Deactivate all table replication.

```sql
ALTER SYSTEM DISABLE ALL TABLE REPLICAS;
```
