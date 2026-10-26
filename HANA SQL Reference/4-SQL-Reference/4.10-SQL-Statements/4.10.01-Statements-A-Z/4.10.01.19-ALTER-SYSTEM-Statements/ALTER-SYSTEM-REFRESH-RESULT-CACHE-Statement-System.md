# 4.10.1.19.45 ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 534–535

Refreshes all result cache entries related to the specified object with up-to-date results.

## Syntax

```sql
ALTER SYSTEM REFRESH [<cache_type>] RESULT CACHE <object_name>
```

## Syntax Elements

#### cache_type

Specifies the cache type. The default value is STATIC.

```sql
<cache_type> ::= STATIC
```

#### object_name

Specifies the object name. It can be any of the objects that has a result cache.

```sql
<object_name>
```

Those objects can be found in the system view M_RESULT_CACHE.

## Description

All result cache entries related to `<object_name>` are refreshed with up-to-date results.

## Examples

Refresh all static result cache entries related to `<view-object>`.

```sql
ALTER SYSTEM REFRESH STATIC RESULT CACHE <view-object>;
```

## Related Information

[M_RESULT_CACHE System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md)
