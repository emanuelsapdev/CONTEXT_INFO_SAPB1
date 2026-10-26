# 4.10.1.155 UNSET [SESSION] Statement (Session Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1112–1113

Unsets a session variable for the current session.

## Syntax

```sql
UNSET [SESSION] <key>
```

## Syntax Elements

#### key

Specifies the session variable to unset.

```sql
<key> ::= <string_literal>
```

## Description

The list of session variables in use for the current session can be found by querying the M_SESSION_CONTEXT system view.

## Example

Set the session variable MY_VAR to abc.

```sql
SET 'MY_VAR' = 'abc';
```

Select the variable MY_VAR from the current session.

```sql
SELECT SESSION_CONTEXT('MY_VAR') FROM DUMMY;
```

Unset the session variable MY_VAR.

```sql
UNSET 'MY_VAR';
```

## Related Information

SET [SESSION] Statement (Session Management) [→](SET-SESSION-Statement-Session-Management.md) M_SESSION_CONTEXT System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md) Session Variables [→](../../4.08-Session-Variables.md)
