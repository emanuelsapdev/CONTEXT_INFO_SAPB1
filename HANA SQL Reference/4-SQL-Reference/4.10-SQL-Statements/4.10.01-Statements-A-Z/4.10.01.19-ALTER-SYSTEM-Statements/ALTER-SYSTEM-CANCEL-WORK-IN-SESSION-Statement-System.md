# 4.10.1.19.19 ALTER SYSTEM CANCEL [WORK IN] SESSION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 503–504

Cancels the currently executing statement of a session.

## Syntax

```sql
ALTER SYSTEM CANCEL [WORK IN] SESSION <connection_id>
```

## Syntax Elements

#### connection_id

Specifies the connection ID of the session.

```sql
<connection_id> ::= <string_literal>
```

## Description

The transaction of the canceled session is rolled back. The statement that was executing returns error code 139 (current operation canceled by request and transaction rolled back).

## Example

The following query returns the current database connection IDs and the statements that the sessions are executing.

```sql
 SELECT C.CONNECTION_ID, PS.STATEMENT_STRING
   FROM M_CONNECTIONS C JOIN M_PREPARED_STATEMENTS PS
        ON C.CONNECTION_ID = PS.CONNECTION_ID AND C.CURRENT_STATEMENT_ID =
PS.STATEMENT_ID
  WHERE C.CONNECTION_STATUS = 'RUNNING'
AND C.CONNECTION_TYPE = 'Remote';
```

Using the connection ID information that you obtained using the query above, you can now cancel a running query. In the statement below, replace `<connection_id>` with a connection ID from the query above.

```sql
ALTER SYSTEM CANCEL SESSION '<connection_id>';
```
