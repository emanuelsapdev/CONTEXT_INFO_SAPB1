# 6.2.178 M_MEMORY_RECLAIM_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1900

Provides statistics for reclaiming memory (for example, defragmentation, unloading of memory objects, and so on) since the last reset.

This view contains values accumulated since the last reset of the main view M_MEMORY_RECLAIM_STATISTICS. Refer to M_MEMORY_RECLAIM_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_MEMORY_RECLAIM_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_MEMORY_RECLAIM_STATISTICS System View](M_MEMORY_RECLAIM_STATISTICS-System-View.md)
