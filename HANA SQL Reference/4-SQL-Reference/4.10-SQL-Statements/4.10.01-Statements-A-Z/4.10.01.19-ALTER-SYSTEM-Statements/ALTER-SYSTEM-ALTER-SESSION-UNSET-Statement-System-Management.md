# 4.10.1.19.15 ALTER SYSTEM ALTER SESSION UNSET Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 494–495

Unsets session variables for database sessions.

## Syntax

```sql
ALTER SYSTEM ALTER SESSION <session_id> UNSET <key>
```

## Syntax Elements

#### session_id

Specifies the session ID of the session where the variable should be unset.

```sql
<session_id> ::= <unsigned_integer>
```

#### key

Specifies the key of a session variable.

```sql
<key> ::= <string_literal>
```

The maximum length of key is 32 characters.

## Description

For a list of predefined variables, see the M_SESSION_CONTEXT system view.

Session variables can be retrieved using the SESSION_CONTEXT command or from the M_SESSION_CONTEXT system view, and unset by using the ALTER SYSTEM ALTER SESSION UNSET statement.

## Example

Set the session variable MY_VAR to 'abc' in your database session.

```sql
SET 'MY_VAR' = 'abc';
```

Execute the following query to get a list of all the session variables of the current session.

```sql
SELECT * FROM M_SESSION_CONTEXT WHERE CONNECTION_ID = CURRENT_CONNECTION;
```

Remove the session variable from the specified session. In the statement below, replace `<your_session_id>` with the session ID that the previous statement returned.

```sql
ALTER SYSTEM ALTER SESSION <your_session_id> UNSET 'MY_VAR';
```

You get a list of all the session variables of the current session.

```sql
SELECT * FROM M_SESSION_CONTEXT WHERE CONNECTION_ID = CURRENT_CONNECTION;
```

From the results of this statement you can see that the MY_VAR variable has been unset.
