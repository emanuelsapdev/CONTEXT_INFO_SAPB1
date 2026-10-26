# 4.9.1.63 CURRENT_USER_ID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 171–172

Returns the current user's user ID at the current statement context.

## Syntax

```sql
CURRENT_USER_ID()
```

## Description

Returns the current user's user ID at the current statement context. This is the user's ID that is currently at the top of the authorization stack.

## Example

```sql
SELECT CURRENT_USER_ID() from DUMMY;
```
