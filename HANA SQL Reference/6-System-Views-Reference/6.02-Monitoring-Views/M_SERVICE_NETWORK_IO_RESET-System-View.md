# 6.2.256 M_SERVICE_NETWORK_IO_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1991–1992

Provides the service network I/O statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_SERVICE_NETWORK_IO. Refer to M_SERVICE_NETWORK_IO for information about the structure and use of this view.

In addition to the members mentioned in M_SERVICE_NETWORK_IO, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_SERVICE_NETWORK_IO System View](M_SERVICE_NETWORK_IO-System-View.md)
