# 4.9.1.175 SESSION_USER Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 328–329

Returns the user name of the current session.

## Syntax

```sql
SESSION_USER
```

## Description

SESSION_USER and CURRENT_USER are similar functions, but there are differences. SESSION_USER reflects how the session connected to the server, while CURRENT_USER may be affected by the SQL SECURITY clause and reflects how permissions are applied.

## Example

The following query returns the user name of the current session:

```sql
SELECT SESSION_USER "session user" FROM DUMMY;
```

Consider the following fictitious definermode procedure that is declared by USER_A:

```sql
CREATE PROCEDURE USER_A.PROC1 LANGUAGE SQLSCRIPT SQL SECURITY DEFINER AS
 BEGIN
     SELECT SESSION_USER "session user" , CURRENT_USER "current user" FROM DUMMY;
 END;
```

The following fictitious query returns `USER_B` when USER_B executes USER_A.PROC:

```sql
CALL USER_A.PROC1;
```

Consider the following fictitious invoker-mode procedure that is declared by USER_A:

```sql
CREATE PROCEDURE USER_A.PROC2 LANGUAGE SQLSCRIPT SQL SECURITY INVOKER AS
 BEGIN
     SELECT SESSION_USER "session user" , CURRENT_USER "current user" FROM DUMMY;
 END;
```

The following fictitious query returns `USER_B` when USER_B executes USER_A.PROC:

```sql
CALL USER_A.PROC2;
```

## Related Information

Session Management Statements [→](../../4.10-SQL-Statements/4.10.10-Session-Management-Statements.md) M_SESSION_CONTEXT System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md) SESSION_CONTEXT Function (Miscellaneous) [→](SESSION_CONTEXT-Function-Miscellaneous.md) CURRENT_USER Function (Miscellaneous) [→](CURRENT_USER-Function-Miscellaneous.md)
