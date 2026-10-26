# 6.2.25 M_BUFFER_CACHE_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1667

Provides a cache level overview of the configuration, cache status, and memory usage since the last reset.

This view contains values accumulated since the last reset of the main view M_BUFFER_CACHE_STATISTICS. Refer to M_BUFFER_CACHE_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_BUFFER_CACHE_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_BUFFER_CACHE_STATISTICS System View](M_BUFFER_CACHE_STATISTICS-System-View.md)
