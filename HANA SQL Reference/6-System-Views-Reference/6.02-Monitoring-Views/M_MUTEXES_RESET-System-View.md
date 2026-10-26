# 6.2.185 M_MUTEXES_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1910

Provides mutex statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_MUTEXES. Refer to M_MUTEXES for information about the structure and use of this view.

In addition to the members mentioned in M_MUTEXES, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_MUTEXES System View](M_MUTEXES-System-View.md)
