# 6.2.171 M_LOG_SEGMENTS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1889–1890

Provides log segment statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_LOG_SEGMENTS. Refer to M_LOG_SEGMENTS for information about the structure and use of this view.

In addition to the members mentioned in M_LOG_SEGMENTS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_LOG_SEGMENTS System View](M_LOG_SEGMENTS-System-View.md)
