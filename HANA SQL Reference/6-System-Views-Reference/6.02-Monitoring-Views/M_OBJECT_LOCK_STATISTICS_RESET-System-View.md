# 6.2.193 M_OBJECT_LOCK_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1918

Provides lock contention statistics, including lock wait count, wait time, and failed count for each object since the last reset.

This view contains values accumulated since the last reset of the main view M_OBJECT_LOCK_STATISTICS. Refer to M_OBJECT_LOCK_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_OBJECT_LOCK_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_OBJECT_LOCK_STATISTICS System View](M_OBJECT_LOCK_STATISTICS-System-View.md)
