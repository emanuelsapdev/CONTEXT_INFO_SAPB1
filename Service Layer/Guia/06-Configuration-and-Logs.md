# 6. Configuring Service Layer (Controller, b1s.conf, per-request options, logs)

> Source: *Working with SAP Business One Service Layer* v1.29, chapter 6 (paraphrased technical reference).
>
> **Resumen (ES):** el Service Layer Controller (web), opciones de configuración en `b1s.conf` y en los `.conf` de Apache, cómo sobrescribirlas por request con cabeceras `B1S-*`, y el monitor de logs.

## Where configuration lives

| File | Content | Contenido (ES) |
|---|---|---|
| `ServiceLayer/conf/b1s.conf` | Main JSON configuration (options are **case-sensitive**) | Configuración principal (JSON) |
| `ServiceLayer/conf/httpd-b1s-lb.conf` | Apache load balancer settings (sticky session, request/response dump) | Balanceador Apache |
| `ServiceLayer/conf/httpd-b1s-lb-member.conf` | Apache member settings (e.g. MaxConnectionsPerChild) | Miembros del balanceador |
| `ServiceLayer/conf/b1s_sqltable.conf` | SQL Query table/column allowlist (see [04](04-SQL-Query.md)) | Lista blanca de SQL Query |

- **All options take effect after restarting Service Layer.**
- The config applies only to local components: with members on other machines, keep each machine's files in sync (the guide notes the same for schema files).
- Log-file configuration: SAP KBA **3157498**.

## Service Layer Controller

Web UI available since 10.0 (PL00 HANA / PL02 SQL): **`https://<server>:<port>/ServiceLayerController`**.

- On SQL Server/Windows, first make sure the PowerShell execution policy is `Unrestricted` (64-bit PowerShell: `Get-ExecutionPolicy`; if needed `Set-ExecutionPolicy Unrestricted`).
- Limitation: it **can't manage all nodes in a distributed installation** (members on other machines than the LB).
- On HANA/Linux SL runs as Linux services `b1s` and `b1s<port>`; Apache `httpd` daemons serve the configured nodes. The controller periodically uses read-only tools (`ps`, `ss`, `grep`, `awk`) to display status.

### 6.1 Service Layer Settings tab

Functions: stop / force-restart the service; add and remove nodes dynamically; edit configuration options; download logs and dump files.

**Node management (Apache balancer) fields:**

| Field | Meaning / default | Campo (ES) |
|---|---|---|
| Max Members | Number of members configured | Cantidad de miembros |
| Sticky Session | ON/OFF (configurable, see below) | Afinidad de sesión |
| Disable Failover | Default Off, read-only | Desactivar failover |
| Timeout | Max seconds to wait for a free worker; default 0 (don't wait), read-only | Espera máxima |
| Failover Attempts | Max failovers before giving up; default workers − 1 (or 1) | Reintentos de failover |
| Method | Scheduler algorithm; default `bybusyness` | Algoritmo |
| Active | Yes if the LB service is running | Activo |
| Worker URL | Members of the balancing group | URL del worker |
| RouteRedir | Redirection route of the worker | Redirección |
| Factor | Load factor 1.0–100.0 (weight) | Factor de carga |
| Set | lbset the worker belongs to | Conjunto |
| Elected | Requests processed since restart | Requests atendidos |
| Busy | 1 if busy, else 0 | Ocupado |
| Load | Requests currently assigned | Carga |
| To / From | Bytes out (responses) / in (requests) | Bytes salida/entrada |
| Status | `Ok`, `Init`, `Dis` (disabled, retried), `Stop` (admin stopped), `Ign` (ignore errors), `Spar` (hot spare), `Stby` (hot standby), `Err` (error, retried), `Drn` (drain: only existing sticky sessions), `HcFl` (failed health check) | Estado del worker |

**Configuration options (controller):**

| Option | Default | Description | File / key | Opción (ES) |
|---|---|---|---|---|
| CorsEnable | off | Enable CORS | `b1s.conf` `"CorsEnable": false` | Habilitar CORS |
| CorsAllowedOrigins | `""` | `;`-separated trusted origins; `"*"` = all (not for production) | `b1s.conf` | Orígenes CORS |
| CorsAllowedHeaders | `"content-type, accept"` | `,`-separated allowed request headers (e.g. add `B1S-PageSize`, `B1S-CaseInsensitive`) | `b1s.conf` | Cabeceras CORS |
| Request & Response Logs | off | Dumps every request/response handled by Apache, one file per day `dumphttp.log_%Y_%m_%d` | `httpd-b1s-lb.conf` | Log de request/response |
| WCFCompatible | off | Makes SL consumable by Microsoft WCF: enums exposed as `Edm.String`; property names can't equal type names (e.g. `BatchNumber.BatchNumber` → `BatchNumberProperty`); `Edm.DateTime` instead of `Edm.Time` | `b1s.conf` `"WCFCompatible": true` | Compatibilidad WCF |
| Max Connections Per Child | 1024 | How often Apache recycles worker processes | `httpd-b1s-lb-member.conf` | Reciclado de procesos |
| Log Levels | `Error` | B1 logs of the SL process: `httpd.servicelayer.YYYYMMDD_HHMMSS.pidxxxxx.log`, `httpd.b1logger.YYYYMMDD_HHMMSS.pidxxxxx.log` | `b1s.conf` `"LogLevel": "Error"` | Nivel de log |
| Session Timeout | 30 (minutes) | Idle timeout per session | `b1s.conf` `"SessionTimeout": 30` | Expiración de sesión |
| CoreDump | off | Write a core dump if the SL process crashes | `b1s.conf` `"EnableCoreDump": true` | Volcado de memoria |
| Enable Access Log | off (since FP 2305; enabled by default before) | Apache access log | `b1s.conf` `"EnableAccessLog": true` | Log de accesos |
| Session Sticky | on | Same client → same node; if off, load is spread equally across nodes | `httpd-b1s-lb.conf` | Afinidad de sesión |

**Log locations:**

| Log | Linux | Windows | Log (ES) |
|---|---|---|---|
| Request/response dump, access log | `/usr/sap/SAPBusinessOne/ServiceLayer/logs/` | `C:\Program Files\SAP\SAP Business One ServerTools\ServiceLayer\logs` | Dump y accesos |
| B1 process logs (LogLevel) | `/usr/sap/SAPBusinessOne/home/b1service0/SAP/SAP Business One/Log/BusinessOne/` | `C:\ProgramData\SAP\SAP Business One\Log\SAP Business One\<ServiceUserName>\BusinessOne` | Logs de B1 |
| Core dumps | `/var/lib/systemd/coredump` | `C:\Program Files\SAP\SAP Business One ServerTools\ServiceLayer\logs\` | Volcados |
| JavaScript extension logs | `{SL install}/logs/script/` | same | Logs de scripts |

Logs can be downloaded from the controller (**Download Logs**).

**Logging an HTTP header in the Apache access log:** edit the `LogFormat` in `ServiceLayer/conf/httpd-b1s-lb.conf`, adding `%{Header}i`, then restart SL:

```apache
<IfModule log_config_module>
  LogFormat "%t %h %D \"%r\" %>s %b ssl=%{SSL_PROTOCOL}x t=%Ts pid=%P sid=%{B1SESSION}C n=%{ROUTEID}C %X host=%{Host}i" common
</IfModule>
```

## 6.2 Other `b1s.conf` options

| Option | Type | Description | Default | Opción (ES) |
|---|---|---|---|---|
| `Server` | String | Database server | — | Servidor de BD |
| `SLDAddress` | String | License server and SLD address (they share it); since 9.1 PL05 | — | Dirección SLD/licencias |
| `Schema` | String | File name (in `conf`) of the default user-defined schema (see [03-07](03-07-Properties-Associations-Schemas.md#312-user-defined-schemas-91-pl03)); since 9.1 PL03 | empty | Esquema por defecto |
| `PageSize` | Integer | Page size for queries | 20 | Tamaño de página |
| `EnableAudienceValidation` | Boolean | Validate the *audience* claim of tokens issued by extensions (e.g. SPAs). Set `false` only for dev/test | true | Validar audiencia del token |

## 6.3 Configuration by request (9.1 PL01+)

Every option except the connection ones can be overridden **for one request** with a header `B1S-<option name>: <value>`:

```http
B1S-WCFCompatible: True
B1S-PageSize: 100
```

Other SL-specific headers seen in this guide: `B1S-Schema` (user-defined schema), `B1S-CaseInsensitive` (case-insensitive queries on HANA), `B1S-ReplaceCollectionsOnPatch` (replace collections on PATCH — see webhooks), plus the standard `Prefer: odata.maxpagesize=n` and `Prefer: return-no-content`.

## 6.4 Log monitor (FP 2202+)

Controller → **Monitor** tab; pick a recent day (1–10 days); 20 rows per page.

| View | Fields | Vista (ES) |
|---|---|---|
| Normal requests – list (grouped by Method + URL) | No., Method, URL, Count, Detail | Requests normales (lista) |
| Normal requests – detail | Time, URL, Duration, Sid (session), Node, HTTP Code, Pid, Client IP | Requests normales (detalle) |
| Error requests – list | No., Method, URL, Count, Details | Requests con error (lista) |
| Error requests – detail | Time, URL, Duration, Sid, Node, HTTP Code, Pid, Client IP | Requests con error (detalle) |
| Request/response detailed logs | Enable **Request & Response Logs** in configuration; download by duration | Logs detallados |
