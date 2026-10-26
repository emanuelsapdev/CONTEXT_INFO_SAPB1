# 5.2.2 ALTER DATABASE Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1218–1219

Alters an existing database by adding or removing a dynamic tiering `esserver` service.

## Syntax

```sql
ALTER DATABASE <database_name>
   ADD 'esserver'  [AT [LOCATION] [ '<hostname>[:<port>]' ]
   | REMOVE 'esserver' AT [LOCATION] '<hostname>:<port>'
```

## Syntax Elements

#### database_name

Specifies the name of the database to which the service is applied.

```sql
<database_name> ::= <identifier>
```

#### hostname

Specifies the name of the dedicated dynamic tiering host.

#### port

Specifies the port number where the dynamic tiering service runs. Port is comprised of 3xx16, where xx is the instance number.

## Permissions

You must have the DATABASE ADMIN privilege.

## Description

This statement can only be executed on the SYSTEM database (systemDB).

## Examples

The following code example shows you how to add the service `esserver` to the database `my_database` at `hostA`, for instance `03`.

```sql
ALTER DATABASE my_database ADD 'esserver'  AT LOCATION 'hostA:30312'
```

The following code example shows you how to remove the service `esserver` from the database `my_database` at `hostA`, for instance `03`.

```sql
ALTER DATABASE my_database REMOVE 'esserver'  AT LOCATION 'hostA:30312'
```
