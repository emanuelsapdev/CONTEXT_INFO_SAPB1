# 6.2.63 M_CS_LOG_REPLAY_QUEUE_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1724

Provides information about column store log replay queue statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_CS_LOG_REPLAY_QUEUE_STATISTICS. Refer to M_CS_LOG_REPLAY_QUEUE_STATISTICS for information about the structure and use of this view.

In addition to the members mentioned in M_CS_LOG_REPLAY_QUEUE_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

[M_CS_LOG_REPLAY_QUEUE_STATISTICS System View](M_CS_LOG_REPLAY_QUEUE_STATISTICS-System-View.md)
