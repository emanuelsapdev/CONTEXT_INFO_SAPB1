# 4.10.1.148 SET [SESSION] Statement (Session Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1100–1101

Sets a session variable for the current session.

## Syntax

```sql
SET [SESSION] <variable_string_literal> = <value_string_literal>
```

## Syntax Elements

#### variable

Specifies the variable to set. The maximum length of `<variable>` is 5000 characters.

#### value

Specifies the value for the specified variable. The maximum length of `<value>` is 5000 characters.

## Description

The maximum number of session variables is 1024 per session by default (or as defined by the max_session_variables setting in the `indexserver.ini` configuration file.

Session variable settings may be overridden by options specified in a query.

Session variables with the `XS_` prefix are protected and cannot be overwritten with the standard SQL SET command.

Session variables can be retrieved by using the SESSION_CONTEXT function or by querying the M_SESSION_CONTEXT system view.

## Example

Set the session variable MY_VAR to abc:

```sql
SET 'MY_VAR' = 'abc';
```

Select the variable MY_VAR from the current session.

```sql
SELECT SESSION_CONTEXT('MY_VAR') FROM DUMMY;
```

or

```sql
SELECT * FROM SYS.M_SESSION_CONTEXT WHERE CONNECTION_ID = CURRENT_CONNECTION;
```

## Related Information

M_SESSION_CONTEXT System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md) UNSET [SESSION] Statement (Session Management) [→](UNSET-SESSION-Statement-Session-Management.md) SESSION_CONTEXT Function (Miscellaneous) [→](../../4.09-SQL-Functions/4.09.01-Functions-A-Z/SESSION_CONTEXT-Function-Miscellaneous.md) Session Variables [→](../../4.08-Session-Variables.md)
