# 3.20–3.21 CORS and the Ping Pong API

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3.20–3.21 (paraphrased technical reference).
>
> **Resumen (ES):** habilitar CORS para llamar al Service Layer desde aplicaciones web de otro origen y usar el endpoint `/ping` para monitorear el balanceador y cada nodo.

## 3.20 Cross-Origin Resource Sharing (CORS)

Supported since 9.1 PL08 (HANA). By default browsers block cross-domain calls; enable CORS in `conf/b1s.conf` (or in the Service Layer Controller):

| Option (`b1s.conf`) | Default | Meaning | Significado (ES) |
|---|---|---|---|
| `CorsEnable` | `false` | Turns CORS on | Activa CORS |
| `CorsAllowedOrigins` | `""` | Semicolon-separated trusted origins, e.g. `"http://host1:8080;https://host2:8443"`; `"*"` allows all (not recommended in production) | Orígenes permitidos |
| `CorsAllowedHeaders` (9.2 PL07+) | `"content-type, accept"` | Comma-separated request headers allowed, e.g. `"content-type, accept, B1S-CaseInsensitive"` | Cabeceras permitidas |

```json
"CorsEnable": true,
"CorsAllowedOrigins": "http://host1:8080;https://host2:8443",
"CorsAllowedHeaders": "content-type, accept, B1S-CaseInsensitive"
```

**Flow:** the browser first sends a **preflight `OPTIONS`** request, and only if allowed sends the real request (the preflight can be cached). In the SL log you'll see pairs like `OPTIONS /b1s/v1/Login` then `POST /b1s/v1/Login`, `OPTIONS /b1s/v1/Items` then `POST /b1s/v1/Items`.

## 3.21 Ping Pong API (9.3 PL10+ HANA)

Apache (load balancer or node) answers directly with a `pong`, **without going through the B1 core**. Uses: isolate network latency from B1 processing time, check server clock, monitor/debug availability, and monitor the load balancer and each node separately.

| Request | Who answers | Example response | Respuesta (ES) |
|---|---|---|---|
| `GET https://<server>:<port>/ping/` | Load balancer | `200 {"message": "pong", "sender": "load balancer", "timestamp": "1555998764.740"}` | Responde el balanceador |
| `GET .../ping/load-balancer` | Load balancer | `200 {"message": "pong", "sender": "load balancer", ...}` | Balanceador |
| `GET .../ping/node/1` | Node 1 | `200 {"message": "pong", "sender": "node1", ...}` | Nodo 1 |
| `GET .../ping/node/2` | Node 2 | `200 {"message": "pong", "sender": "node2", ...}` | Nodo 2 |
| `GET .../ping/node` | Node 1 (default) | `200 {"message": "pong", "sender": "node1", ...}` | Nodo por defecto |
| `GET .../ping/node/4` (node down) | — | `503 {"message": "Service Unavailable"}` | Nodo caído |
| `GET .../ping/node/5` (doesn't exist) | Load balancer | `503 {"message": "node 5 does not exist", "sender": "load balancer", ...}` | Nodo inexistente |

`timestamp` is the server's Unix time (seconds.milliseconds).
