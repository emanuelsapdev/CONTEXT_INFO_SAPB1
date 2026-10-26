# 6.2.129 M_HOST_NETWORK_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1821–1822

Provides information about the network statistics of a host.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name the network statistics refer to. |
| TCP_SEGMENTS_RECEIVED | BIGINT | Displays the total number of TCP segments received. |
| TCP_SEGMENTS_SENT_OUT | BIGINT | Displays the total number of TCP segments sent out. |
| TCP_SEGMENTS_RETRANSMITTED | BIGINT | Displays the number of TCP segments that had to be retransmitted. |
| TCP_BAD_SEGMENTS_RECEIVED | BIGINT | Displays the number of TCP segments that were broken upon receiving. |

## Additional Information

Most columns correspond to the similarly named values reported by `netstat -s`.

In a SystemDB the view returns one row for each physical host system present. In a tenant database, the view returns one row for each physical host system on which at least one service process of the respective tenant database is running.

## Related Information

M_HOST_INFORMATION System View [→](M_HOST_INFORMATION-System-View.md) M_HOST_RESOURCE_UTILIZATION System View [→](M_HOST_RESOURCE_UTILIZATION-System-View.md)
