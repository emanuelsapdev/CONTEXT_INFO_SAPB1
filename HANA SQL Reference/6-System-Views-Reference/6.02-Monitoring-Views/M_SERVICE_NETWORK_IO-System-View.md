# 6.2.255 M_SERVICE_NETWORK_IO System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1990–1991

Provides service network I/O statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SENDER_HOST | VARCHAR(64) | Displays the host name of the sending service. |
| SENDER_PORT | INTEGER | Displays the port that the sending service listens on. |
| RECEIVER_HOST | VARCHAR(64) | Displays the host name of the receiving service. |
| RECEIVER_PORT | INTEGER | Displays the port that the receiving service listens on. |
| SEND_SIZE | BIGINT | Displays the number of bytes sent. |
| RECEIVE_SIZE | BIGINT | Displays the number of bytes received. |
| SEND_DURATION | BIGINT | Displays the time spent sending in microseconds. |
| RECEIVE_DURATION | BIGINT | Displays the time spent receiving in microseconds. |
| REQUEST_COUNT | BIGINT | Displays the number of requests handled. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_SERVICE_NETWORK_IO_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_SERVICE_NETWORK_IO_RESET;`.

## Related Information

[M_SERVICE_NETWORK_IO_RESET System View](M_SERVICE_NETWORK_IO_RESET-System-View.md)
