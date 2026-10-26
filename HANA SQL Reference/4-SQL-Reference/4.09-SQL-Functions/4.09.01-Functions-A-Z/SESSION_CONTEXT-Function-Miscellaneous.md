# 4.9.1.174 SESSION_CONTEXT Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 327–328

Returns the value of the specified session variable assigned to the current user.

## Syntax

```sql
SESSION_CONTEXT(<session_variable>)
```

## Description

The `<session_variable>` can either be predefined or userdefined. Predefined session variables that can be set by the client are APPLICATION, APPLICATIONUSER, and TRACEPROFILE.

Session variables can be defined or modified using a `SET [SESSION] <variable_name> = <value>` statement, and unset using an `UNSET [SESSION] <variable_name>` statement.

SESSION_CONTEXT returns an NVARCHAR with a maximum length of 512 characters.

## Example

The following query returns the value `HDBStudio`, or a similar value depending on your settings:

```sql
SELECT SESSION_CONTEXT('APPLICATION') "session context" FROM DUMMY;
```

## Related Information

Session Management Statements [→](../../4.10-SQL-Statements/4.10.10-Session-Management-Statements.md) SESSION_USER Function (Miscellaneous) [→](SESSION_USER-Function-Miscellaneous.md) M_SESSION_CONTEXT System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md) SET [SESSION] Statement (Session Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SESSION-Statement-Session-Management.md) UNSET [SESSION] Statement (Session Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-SESSION-Statement-Session-Management.md)
