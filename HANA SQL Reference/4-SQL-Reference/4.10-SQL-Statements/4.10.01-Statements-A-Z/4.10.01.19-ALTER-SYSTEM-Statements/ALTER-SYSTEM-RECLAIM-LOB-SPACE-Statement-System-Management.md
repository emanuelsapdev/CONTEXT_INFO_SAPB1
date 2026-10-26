# 4.10.1.19.40 ALTER SYSTEM RECLAIM LOB SPACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 530

Runs LOB garbage collection and removes any non-referenced LOB files.

## Syntax

```sql
ALTER SYSTEM RECLAIM [ROW|COLUMN] LOB SPACE
```

## Description

Runs the LOB garbage collection, which removes any non-referenced LOB files.
