# 6.2.215 M_READWRITELOCKS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1945

Provides read/write lock statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_READWRITELOCKS. Refer to M_READWRITELOCKS for information about the structure and use of this view.

In addition to the members mentioned in M_READWRITELOCKS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_READWRITELOCKS System View](M_READWRITELOCKS-System-View.md)
