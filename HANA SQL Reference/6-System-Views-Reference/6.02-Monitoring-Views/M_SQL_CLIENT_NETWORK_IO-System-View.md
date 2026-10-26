# 6.2.274 M_SQL_CLIENT_NETWORK_IO System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2018–2019

Provides the client and server elapsed time as well as message sizes for client network messages.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CLIENT_HOST | NVARCHAR(256) | Displays the host of the client machine, also found in M_CONNECTIONS.CLIENT_HOST. |
| CONNECTION_ID | INTEGER | Displays the connection ID of the physical server connection. |
| MESSAGE_ID | BIGINT | Displays the client message ID on the physical server connection. |
| CLIENT_DURATION | BIGINT | Displays the elapsed time on the client side including send, server execution, and receive. |
| SERVER_DURATION | BIGINT | Displays the execution time on the server side. Transport time is the delta between CLIENT_DURATION and SERVER_DURATION. |
| SERVER_RECEIVED_TIME | TIMESTAMP | Displays the time when the message was received on the server side and begin of execution. |
| RECEIVED_MESSAGE_SIZE | BIGINT | Displays the size of messages received on the server side in bytes. |
| SEND_MESSAGE_SIZE | BIGINT | Displays the size of the messages sent to the client side in bytes. |

## Additional Information

By default, collection of statistics related to client network I/O is controlled by the sql_client_network_io parameter in the `indexserver.ini` configuration file.

## Related Information

[M_CONNECTIONS System View](M_CONNECTIONS-System-View.md)
