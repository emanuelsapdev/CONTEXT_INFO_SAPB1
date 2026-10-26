# 4.10.1.19.13 ALTER SYSTEM ALTER SESSION SET Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 488–489

Sets session variables for database sessions.

## Syntax

```sql
ALTER SYSTEM ALTER SESSION <session_id> SET <key> = <value>
```

## Syntax Elements

#### session_id

Specifies the session ID of the session where the variable should be set.

```sql
<session_id> ::= <unsigned_integer>
```

#### key

Specifies the key of a session variable.

```sql
<key> ::= <string_literal>
```

The maximum length of key is 32 characters.

#### value

Specifies the desired value of a session variable.

```sql
<value> ::= <string_literal>
```

The maximum length of `<value>` is 512 characters.

## Description

For a list of predefined variables, see the M_SESSION_CONTEXT system view.

Session variables can be retrieved using the SESSION_CONTEXT command or from the M_SESSION_CONTEXT system view, and unset by using the ALTER SYSTEM ALTER SESSION UNSET statement.

## Example

Run each command in this example in the same SQL editor you use. The same database session is required to make the example work properly.

Obtain your current session ID.

```sql
SELECT connection_id FROM m_connections WHERE OWN = 'TRUE';
```

Set the variable MY_VAR to 'some_value' in your session. In the command below, replace `<your_session_id>` with the session ID from the previous query.

```sql
ALTER SYSTEM ALTER SESSION <your_session_id> SET 'MY_VAR'= 'some_value';
```

Check the current value of MY_VAR in your session.

```sql
SELECT SESSION_CONTEXT('MY_VAR') FROM dummy;
```
