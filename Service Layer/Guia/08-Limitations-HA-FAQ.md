# 8–10. Limitations, High Availability and Load Balancing, FAQ

> Source: *Working with SAP Business One Service Layer* v1.29, chapters 8–10 (paraphrased technical reference).
>
> **Resumen (ES):** limitaciones del protocolo OData y frente a la DI API, cómo funciona la alta disponibilidad (balanceo y sesiones compartidas) y preguntas frecuentes (diferencias con DI API/DI Server, PUT vs PATCH, `X-HTTP-Method-Override`, servicios Linux, cliente HANA).

## 8.1 OData protocol limitations

| Limitation | Limitación (ES) |
|---|---|
| OData v1.0 and v2.0 not supported (only v3 `/b1s/v1` and v4 `/b1s/v2`) | Sin OData v1/v2 |
| XML request/response format not supported for general entity CRUD (JSON only) | Sin XML en CRUD |
| Accessing a property of a complex type is not allowed (e.g. `/Orders(1)/TaxExtension/TaxId0`) | No se accede a propiedades de tipos complejos |
| Managing values and properties directly not supported | No se gestionan valores/propiedades directamente |
| Batch **rollback** operation not supported (a failing change set is rolled back automatically, but the client can't request a rollback) | Sin rollback explícito en batch |
| `odata=fullmetadata` (v3) and `odata.metadata=full` (v4) not supported | Sin metadata completa en respuestas |
| Arithmetic operators (`add/sub/mul/div/mod`) in standard OData queries not yet supported (they work inside `$crossjoin` selects/filters, see 3.6.9) | Aritmética en consultas no soportada |
| Some OData query functions not supported (date, math, type-cast and some string functions) | Algunas funciones OData no soportadas |
| JSONP not supported | Sin JSONP |

## 8.2 Functional limitations vs. DI API

| Limitation | Workaround | Limitación (ES) |
|---|---|---|
| No `Recordset` (direct SQL) | OData queries, `SQLQueries` (ch. 4), Semantic Layer / SQL views (3.7–3.8) | Sin Recordset |
| No `ImportFromXML` / `ExportToXML` | Use JSON | Sin importar/exportar XML |
| Newly created UDO/UDF/UDT not accessible until **Service Layer is restarted** | Restart SL after metadata changes | Reiniciar tras crear UDF/UDT/UDO |
| No user transactions (`StartTransaction/EndTransaction`); each request (including a `$batch`) is its own transaction; transactions can't span requests | `$batch` change sets (3.9) or JavaScript extensions with transactions (3.19) | Sin transacciones entre requests |

## 9. High availability and load balancing

- SL installs **Apache Multi-Processing Modules (MPMs)** and is configured as a **load-balancing cluster**: a central load balancer distributes HTTP requests among nodes (by number of requests).
- **Sticky sessions** avoid unnecessary logins (login is expensive in B1): requests of the same session go to the same node.
- Nodes can run in a clustered system with hardware/software redundancy.
- **Failover:** if the LB detects a failed node, it sends subsequent requests to another valid node. That node validates the session through **shared session info stored in the database** and logs the user in automatically — the user only notices a small delay.

## 10. FAQ

| Question | Answer | Respuesta (ES) |
|---|---|---|
| SL vs. DI API vs. DI Server? | All three share the **DI core** and similar business objects. DI API: Microsoft COM, best for Windows-native apps. DI Server: SOAP-based integration. **Service Layer: OData/REST**, easy web mashups and add-ons in any language (Java, JavaScript, .NET…) with third-party OData libraries (http://www.odata.org/libraries/), plus HA and scalability | SL comparte el núcleo DI; es REST/OData |
| Implications of a RESTful architecture? | Lightweight, fast, simple transactions (CRUD); queries are just URIs; `$batch` covers atomic multi-request scenarios. Not ideal for complex/distributed transactions requiring server-side state | REST: simple y rápido; no para transacciones complejas con estado |
| PUT vs. PATCH? | `PUT` = replacement (missing properties → default values); `PATCH` = differential (only sent properties change). **Prefer PATCH** | Preferir PATCH |
| My HTTP client doesn't support PATCH | Since 9.1 PL04 use `POST` with header **`X-HTTP-Method-Override: PATCH`** (also works for `PUT`, `MERGE`, `DELETE`). `PATCH /Orders(1)` ≡ `POST /Orders(1)` + `X-HTTP-Method-Override: PATCH` | Usar X-HTTP-Method-Override |
| Does SL start with the OS? | On HANA/Linux yes: services `b1s` and `b1s<port>`. Check with `chkconfig | grep b1s` (e.g. `b1s50000` = load balancer, `b1s50001`–`b1s50003` = nodes). Disable/enable per node: `chkconfig b1s50001 off` / `on` | Arranque automático |
| HANA client not in the default path? | Default `/usr/sap/hdbclient`. Since 9.1 PL04 SL detects it via `/var/opt/.hdb/{hostname}/installations.client`. Older: symlink (`mkdir /usr/sap; ln -s /your/path/hdbclient /usr/sap/hdbclient`) or add the path to `/etc/ld.so.conf` and run `ldconfig` | Cliente HANA en otra ruta |
