# 6.2.249 M_SEMAPHORES_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1984–1985

Provides semaphore statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_SEMAPHORES. Refer to M_SEMAPHORES for information about the structure and use of this view.

In addition to the members mentioned in M_SEMAPHORES, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_SEMAPHORES System View](M_SEMAPHORES-System-View.md)
