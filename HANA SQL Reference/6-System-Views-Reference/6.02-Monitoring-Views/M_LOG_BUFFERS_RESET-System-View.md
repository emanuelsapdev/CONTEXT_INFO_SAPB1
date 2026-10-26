# 6.2.165 M_LOG_BUFFERS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1880–1881

Provides log buffer statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_LOG_BUFFERS. Refer to M_LOG_BUFFERS for information about the structure and use of this view.

In addition to the members mentioned in M_LOG_BUFFERS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_LOG_BUFFERS System View](M_LOG_BUFFERS-System-View.md)
