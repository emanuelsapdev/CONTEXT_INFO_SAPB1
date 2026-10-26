# 6.2.151 M_LIVECACHE_CONTAINER_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1854–1855

Provides accumulated LiveCache container statistics since last reset.

This view contains values accumulated since the last reset of the main view M_LIVECACHE_CONTAINER_STATISTICS. Refer to M_LIVECACHE_CONTAINER_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_LIVECACHE_CONTAINER_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_LIVECACHE_CONTAINER_STATISTICS System View](M_LIVECACHE_CONTAINER_STATISTICS-System-View.md)
