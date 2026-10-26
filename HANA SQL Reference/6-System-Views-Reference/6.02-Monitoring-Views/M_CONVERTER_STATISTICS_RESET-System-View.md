# 6.2.54 M_CONVERTER_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1706–1707

Provides converter statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_CONVERTER_STATISTICS. Refer to M_CONVERTER_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_CONVERTER_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_CONVERTER_STATISTICS System View](M_CONVERTER_STATISTICS-System-View.md)
