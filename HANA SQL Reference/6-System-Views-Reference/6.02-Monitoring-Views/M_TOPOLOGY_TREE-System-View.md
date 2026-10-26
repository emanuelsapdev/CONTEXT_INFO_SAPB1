# 6.2.334 M_TOPOLOGY_TREE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2111–2112

Provides information about SAP HANA nameserver topology content.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PATH | NVARCHAR(1024) | Displays the path to the key. |
| NAME | NVARCHAR(256) | Displays the key name. |
| VALUE | NVARCHAR(256) | Displays the key value. |
| LEAF | NVARCHAR(5) | Displays the leaf flag: TRUE/FALSE. |

## Additional Information

Use '/' as the root path. For deeper paths, use PATH+'/'+NAME. If NAME contains '/', then you must enclose it in CHR(1), For example:

```sql
SELECT * FROM M_TOPOLOGY_TREE WHERE PATH='/index/'||CHR(1)||'SYSTEM:A/B'||
CHR(1)||'#15046'
```

To change topology tree values, use ALTER SYSTEM ALTER CONFIGURATION ('topology.ini','system') SET (PATH,NAME)=VALUE.

To delete values use ALTER SYSTEM ALTER CONFIGURATION ('topology.ini','system') UNSET (PATH,NAME).
