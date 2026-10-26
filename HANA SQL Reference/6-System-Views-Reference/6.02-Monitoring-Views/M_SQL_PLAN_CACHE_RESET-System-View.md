# 6.2.280 M_SQL_PLAN_CACHE_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2033–2034

Provides statistics of an individual execution plan since the last reset.

This view contains values accumulated since the last reset of the main view M_SQL_PLAN_CACHE. Refer to M_SQL_PLAN_CACHE for information about the structure and use of this view.

In addition to the members mentioned in M_SQL_PLAN_CACHE, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_SQL_PLAN_CACHE System View](M_SQL_PLAN_CACHE-System-View.md)
