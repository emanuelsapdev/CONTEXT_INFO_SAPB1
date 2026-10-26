# 6.2.52 M_CONTEXT_MEMORY_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1704

Provides memory allocator statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_CONTEXT_MEMORY. Refer to M_CONTEXT_MEMORY for information about the structure and use of this view.

In addition to the members mentioned in M_CONTEXT_MEMORY, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_CONTEXT_MEMORY System View](M_CONTEXT_MEMORY-System-View.md)
