# 4.10.1.19.37 ALTER SYSTEM RECLAIM DATA SPACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 527–528

Executes row store memory reorganization at runtime.

## Syntax

```sql
ALTER SYSTEM RECLAIM [ROW] DATA SPACE [IMMEDIATE] [<host_port>]
```

## Syntax Elements

#### IMMEDIATE

Executes row store reorganization right away. The same for omitted case.

#### host_port

Specifies the host and port of the service to reorganize the row store.

```sql
<host_port> ::= '<hostname>:<port_number>'
```

If this value is omitted, then the reorganization is executed on the host which the connection is made.

## Description

Before the store is reorganized, there is an inspection of the system to analyze the current status of row store memory utilization. After that, it calculates how much memory can be reduced.

When this inspection is complete, a table list is generated. It then locks the member tables in the table list and executes actual row store memory reorganization.

The table list is determined at runtime and it can affect a number of row tables.

## Example

Execute the row store memory reorganization.

```sql
ALTER SYSTEM RECLAIM DATA SPACE;
```
