# 6.2.282 M_SQL_PLAN_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2041

Provides statistics of a live or evicted individual execution plan since the last reset.

This view contains values accumulated since the last reset of the main view M_SQL_PLAN_STATISTICS. Refer to M_SQL_PLAN_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_SQL_PLAN_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_SQL_PLAN_STATISTICS System View](M_SQL_PLAN_STATISTICS-System-View.md)
