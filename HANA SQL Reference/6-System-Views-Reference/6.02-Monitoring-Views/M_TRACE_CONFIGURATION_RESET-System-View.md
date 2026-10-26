# 6.2.338 M_TRACE_CONFIGURATION_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2115–2116

Provides information about trace configuration statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_TRACE_CONFIGURATION. Refer to M_TRACE_CONFIGURATION for information about the structure and use of this view.

In addition to the members mentioned in M_TRACE_CONFIGURATION, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_TRACE_CONFIGURATION System View](M_TRACE_CONFIGURATION-System-View.md)
