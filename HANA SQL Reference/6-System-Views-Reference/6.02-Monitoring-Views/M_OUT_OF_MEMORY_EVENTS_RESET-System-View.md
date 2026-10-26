# 6.2.195 M_OUT_OF_MEMORY_EVENTS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1919–1920

Provides a list of the last out-of-memory (OOM) events since the last reset.

This view contains values accumulated since the last reset of the main view M_OUT_OF_MEMORY_EVENTS. Refer to M_OUT_OF_MEMORY_EVENTS for information about the structure and use of this view.

In addition to the members mentioned in M_OUT_OF_MEMORY_EVENTS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_OUT_OF_MEMORY_EVENTS System View](M_OUT_OF_MEMORY_EVENTS-System-View.md)
