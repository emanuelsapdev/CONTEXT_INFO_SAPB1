# 4.10.1.19.42 ALTER SYSTEM RECLAIM VERSION SPACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 531–532

Triggers the row-store garbage collector to free up memory space and enhance system responsiveness.

## Syntax

```sql
ALTER SYSTEM RECLAIM VERSION SPACE
```

## Description

You do not need to use this command if only short transactions are being executed on the system because the garbage collector is automatically triggered when a transaction ends. If there are long-running transactions on the system, then this command helps overall system performance if the m_mvcc_tables monitoring view shows a large number of row-store versions (for example, over 1M).

## Example

Check the number of row-store versions on the system by using the m_mvcc_tables monitoring view:

```sql
SELECT * FROM m_mvcc_tables;
```

Trigger row-store garbage collection:

```sql
ALTER SYSTEM RECLAIM VERSION SPACE;
```

## Related Information

[M_MVCC_TABLES System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_MVCC_TABLES-System-View.md)
