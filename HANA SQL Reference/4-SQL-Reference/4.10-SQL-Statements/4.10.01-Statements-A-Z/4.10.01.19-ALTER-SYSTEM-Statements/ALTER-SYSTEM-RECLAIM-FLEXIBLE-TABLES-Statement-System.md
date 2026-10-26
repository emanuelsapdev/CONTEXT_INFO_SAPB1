# 4.10.1.19.39 ALTER SYSTEM RECLAIM FLEXIBLE TABLES Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 529–530

Runs garbage collection for flexible tables.

## Syntax

```sql
ALTER SYSTEM RECLAIM FLEXIBLE TABLES
```

## Description

Periodic garbage collection is specified when creating or altering a flexible table.

During the garbage collection process, SAP HANA scans, and then removes, dynamic columns of flexible tables that contain only NULL values. However, it may not immediately remove some of these columns, even if querying the table produces only NULL values for a particular column. This lag time is due to multiversion concurrency control (MVCC) and internal data representation. Merging the delta of flexible tables before calling the garbage collection may help bring these columns to a collectible state.

## Related Information

CREATE TABLE Statement (Data Definition) [→](../4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../4.10.01.20-ALTER-TABLE/README.md)
