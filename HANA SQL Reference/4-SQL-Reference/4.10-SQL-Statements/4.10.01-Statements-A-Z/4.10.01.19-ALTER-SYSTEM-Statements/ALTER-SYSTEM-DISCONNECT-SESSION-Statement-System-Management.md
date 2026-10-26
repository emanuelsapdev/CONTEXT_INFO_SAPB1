# 4.10.1.19.30 ALTER SYSTEM DISCONNECT SESSION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 516–517

Disconnects the specifed connection session from the database.

## Syntax

```sql
ALTER SYSTEM DISCONNECT SESSION <session_id>
```

## Syntax Elements

#### session_id

Specifies the external (client) session to be disconnected.

```sql
<session_id> ::= <string_literal>
```

## Description

Before disconnecting, any currently running operations associated with the session are terminated.

If `<session_id>` is an internal connection, the statement is ignored.

## Example

The following query obtains the session IDs of idle sessions.

```sql
SELECT CONNECTION_ID, IDLE_TIME FROM M_CONNECTIONS
  WHERE CONNECTION_STATUS = 'IDLE' AND CONNECTION_TYPE = 'Remote'
  ORDER BY IDLE_TIME DESC;
```

To disconnect a session, replace `<connection_id>` with a connection ID from the query above.

```sql
ALTER SYSTEM DISCONNECT SESSION '<connection_id>';
```
