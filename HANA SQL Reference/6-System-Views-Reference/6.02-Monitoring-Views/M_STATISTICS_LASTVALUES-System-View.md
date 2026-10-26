# 6.2.283 M_STATISTICS_LASTVALUES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2041–2042

Provides an in-memory version of _SYS_STATISTICS.STATISTICS_LASTVALUES.

## Structure

| HOST | VARCHAR(64) | Displays the host name. |
| --- | --- | --- |
| PORT | INTEGER | Displays the port name. |
| NAME | NVARCHAR(128) | Displays the value name. |
| INDEX | NVARCHAR(1024) | Displays the index of value. |
| REACHED_AT | TIMESTAMP | Displays the value reached at. |
| VALUE | NVARCHAR(5000) | Displays the last value. |

## Additional Information

The Statistics Server when running has a view _SYS_STATISTICS.STATISTICS_LASTVALUES on which this view is based.

> **Note**
>
> The new Embedded Statistics Service (ESS) does not use the view _SYS_STATISTICS.STATISTICS_LASTVALUES, which means this view is therefore empty.

## Related Information

[LAST_VALUE Function (Aggregate)](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LAST_VALUE-Function-Aggregate.md)
