# 6.2.167 M_LOG_PARTITIONS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1885–1886

Provides log partition statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_LOG_PARTITIONS. Refer to M_LOG_PARTITIONS for information about the structure and use of this view.

In addition to the members mentioned in M_LOG_PARTITIONS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_LOG_PARTITIONS System View](M_LOG_PARTITIONS-System-View.md)
