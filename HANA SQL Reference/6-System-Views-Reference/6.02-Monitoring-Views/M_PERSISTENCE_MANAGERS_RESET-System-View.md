# 6.2.203 M_PERSISTENCE_MANAGERS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1929–1930

Provides persistence manager statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_PERSISTENCE_MANAGERS. Refer to M_PERSISTENCE_MANAGERS for information about the structure and use of this view.

In addition to the members mentioned in M_PERSISTENCE_MANAGERS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_PERSISTENCE_MANAGERS System View](M_PERSISTENCE_MANAGERS-System-View.md)
