# 6.2.207 M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1934

Reports the statistics of physical lifecycle events of blocks managed by SAP HANA services on the persistent memory volumes since the last reset.

This view contains values accumulated since the last reset of the main view M_PERSISTENCE_MEMORY_VOLUME_STATISTICS. Refer to M_PERSISTENCE_MEMORY_VOLUME_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_PERSISTENCE_MEMORY_VOLUME_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_PERSISTENT_MEMORY_VOLUME_STATISTICS System View](M_PERSISTENT_MEMORY_VOLUME_STATISTICS-System-View.md)
