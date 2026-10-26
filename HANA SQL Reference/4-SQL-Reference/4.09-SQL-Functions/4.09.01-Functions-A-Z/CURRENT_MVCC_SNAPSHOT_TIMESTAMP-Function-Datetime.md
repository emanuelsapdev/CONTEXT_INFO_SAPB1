# 4.9.1.53 CURRENT_MVCC_SNAPSHOT_TIMESTAMP Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 163–164

Returns the timestamp of the current MVCC snapshot in SSSS format (seconds past midnight).

## Syntax

```sql
CURRENT_MVCC_SNAPSHOT_TIMESTAMP()
```

## Description

The CURRENT_MVCC_SNAPSHOT_TIMESTAMP function returns the timestamp of the current MVCC snapshot in SSSS format.

## Example

The following example returns the timestamp of the current MVCC snapshot:

```sql
SELECT CURRENT_MVCC_SNAPSHOT_TIMESTAMP() FROM DUMMY;
```
