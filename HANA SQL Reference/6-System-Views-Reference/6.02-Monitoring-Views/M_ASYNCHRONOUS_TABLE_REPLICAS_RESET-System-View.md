# 6.2.13 M_ASYNCHRONOUS_TABLE_REPLICAS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1652

Shows aggregated information on caches (since last reset).

This view contains values accumulated since the last reset of the main view M__ASYNCHRONOUS_TABLE_REPLICAS. Refer to M__ASYNCHRONOUS_TABLE_REPLICAS for information about the structure and use of this view. In addition to the members mentioned in M__ASYNCHRONOUS_TABLE_REPLICAS, this view also contains a timestamp field RESET_TIME, which indicates the last time the data was reset.
