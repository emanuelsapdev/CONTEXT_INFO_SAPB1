# 4.9.1.62 CURRENT_USER Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 170–171

Returns the current user name at the current statement context.

## Syntax

```sql
CURRENT_USER
```

## Description

Returns the current user name at the current statement context. This is the user name that is currently at the top of authorization stack.

SESSION_USER and CURRENT_USER are similar functions, but there are differences. SESSION_USER reflects how the session connected to the server, while CURRENT_USER may be affected by the SQL SECURITY clause and reflects how permissions are applied.

## Example

The following example shows a basic function operation using the SYSTEM user and returns SYSTEM:

```sql
SELECT CURRENT_USER "current user" FROM DUMMY;
```

In the following example, USER A creates a procedure:

```sql
CREATE PROCEDURE USER_A.PROC1 LANGUAGE SQLSCRIPT SQL SECURITY DEFINER AS
 BEGIN
     SELECT CURRENT_USER "current user" FROM DUMMY;
 END;
```

USER B calls the procedure USER_A.PROC1, which returns USER_A:

```sql
CALL USER_A.PROC1;
```

USER A also creates the following procedure:

```sql
CREATE PROCEDURE USER_A.PROC2 LANGUAGE SQLSCRIPT SQL SECURITY INVOKER AS
 BEGIN
     SELECT CURRENT_USER "current user" FROM DUMMY;
 END;
```

USER B calls the procedure USER_A.PROC2, which returns USER_B:

```sql
CALL USER_A.PROC2;
```

## Related Information

[SESSION_USER Function (Miscellaneous)](SESSION_USER-Function-Miscellaneous.md)
