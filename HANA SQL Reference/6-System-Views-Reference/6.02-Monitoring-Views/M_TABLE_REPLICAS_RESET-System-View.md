# 6.2.317 M_TABLE_REPLICAS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2092

Provides detailed information on asynchronous/synchronous table replicas.

This view contains values accumulated since the last reset of the main view M_TABLE_REPLICAS. Refer to M_TABLE_REPLICAS for information about the structure and use of this view.

In addition to the members mentioned in M_TABLE_REPLICAS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_TABLE_REPLICAS System View](M_TABLE_REPLICAS-System-View.md)
