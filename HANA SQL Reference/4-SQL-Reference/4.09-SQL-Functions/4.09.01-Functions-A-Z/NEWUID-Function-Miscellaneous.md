# 4.9.1.136 NEWUID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 264–265

Creates a unique identifier within an SAP HANA database.

## Syntax

```sql
NEWUID()
```

## Description

The NEWUID function acts as an alternative to the SYSUUID function. The SYSUUID function generates a universally unique identifier, whereas the NEWUID function generates a unique identifier within one SAP HANA database. Both functions return VARBINARY(16).

## Example

The following fictitious example returns a unique value, such as `C15F6DB61C6A2B00F0000001EC2E2F00`:

```sql
SELECT NEWUID() FROM DUMMY;
```
