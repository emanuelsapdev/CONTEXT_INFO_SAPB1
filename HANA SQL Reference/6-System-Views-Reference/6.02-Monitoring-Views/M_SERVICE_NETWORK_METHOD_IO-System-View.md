# 6.2.257 M_SERVICE_NETWORK_METHOD_IO System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1992–1993

Displays the number of calls and amount of data that is sent and received.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SENDER_HOST | VARCHAR(64) | Displays the host name of the sender. |
| SENDER_PORT | INTEGER | Displays the host port number of the sender. |
| RECEIVER_HOST | NVARCHAR(256) | Displays the host name of the receiver. |
| RECEIVER_PORT | NVARCHAR(256) | Displays the host port number of the receiver. |
| THREAD_METHOD | NVARCHAR(256) | Displays the originating method name. |
| OPERATOR | NVARCHAR(256) | Displays additional details. |
| REQUEST_COUNT | BIGINT | Displays the total number of requests for the method. |
| SEND_SIZE | BIGINT | Displays the total number of bytes sent. |
| RECEIVE_SIZE | BIGINT | Displays the total number of bytes received. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last updated timestamp. |

## Related Information

[M_SERVICE_NETWORK_METHOD_IO_RESET System View](M_SERVICE_NETWORK_METHOD_IO_RESET-System-View.md)
