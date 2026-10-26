# 4.10.1.156 UNSET SYSTEM LICENSE ALL Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1113–1114

Deletes all currently installed license keys.

> **Caution**
>
> Running this command immediately locks down your SAP HANA database. You will then need a new license key before you can use the system further.

## Syntax

```sql
UNSET SYSTEM LICENSE ALL
```

## Permissions

You need the LICENSE ADMIN system privilege to execute this statement.

## Description

After using this command, the SAP HANA database is immediately locked down and requires a new, valid license key before it can be used further.

## Example

Delete all currently installed license keys.

```sql
UNSET SYSTEM LICENSE ALL;
```
