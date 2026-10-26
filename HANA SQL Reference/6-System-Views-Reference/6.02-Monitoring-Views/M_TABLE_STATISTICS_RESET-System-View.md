# 6.2.320 M_TABLE_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2095

Returns the table DML runtime statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_TABLE_STATISTICS. Refer to M_TABLE_STATISTICS System View for information about the structure and use of this view.

In addition to the members mentioned in the M_TABLE_STATISTICS System View topic, this system view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_TABLE_STATISTICS System View](M_TABLE_STATISTICS-System-View.md)
