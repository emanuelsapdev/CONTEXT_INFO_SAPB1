# 6.2.346 M_VOLUME_IO_DETAILED_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2127–2128

Provides detailed statistics about file access since the last reset.

This view contains the values that have accumulated since the last reset of the main view M_VOLUME_IO_DETAILED_STATISTICS. Refer to M_VOLUME_IO_DETAILED_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_VOLUME_IO_DETAILED_STATISTICS, this view also contains a timestamp field, RESET_TIME, that indicates the last time the data was reset.

## Related Information

[M_VOLUME_IO_DETAILED_STATISTICS System View](M_VOLUME_IO_DETAILED_STATISTICS-System-View.md)
