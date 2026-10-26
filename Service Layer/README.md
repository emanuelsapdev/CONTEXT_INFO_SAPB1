# SAP Business One Service Layer — Documentation for agents

> **ES:** Documentación del Service Layer de SAP Business One 10.0 en inglés, con columna en español en todas las tablas. Se armó con dos fuentes: la guía oficial *Working with SAP Business One Service Layer* (v1.29, 2026-07-27), reescrita como referencia técnica, y el `$metadata` (OData v4) de la sociedad. Del metadata se quitaron todos los UDF, UDT y UDO creados por usuarios. Solo se conservaron los UDF de la **localización argentina de SAP** (`U_B1SYS_*`), marcados como **[Loc. AR]**.

## Folder structure

| Path | Content | Contenido (ES) |
|---|---|---|
| [Guia/](Guia/) | The user guide, chapter by chapter (17 files) | Guía de uso, por capítulos |
| [_INDICE-Entidades.md](_INDICE-Entidades.md) → [Entidades/](Entidades/) | 319 entity sets (CRUD endpoints, key, DB tables, properties, navigation, bound actions, ETag) | Entidades (colecciones) |
| [_INDICE-Tipos-Complejos.md](_INDICE-Tipos-Complejos.md) → [Tipos-Complejos/](Tipos-Complejos/) | 760 complex types (document lines, sub-collections, service parameter types) | Tipos complejos (líneas, subcolecciones, parámetros) |
| [_INDICE-Enums.md](_INDICE-Enums.md) → [Enums/](Enums/) | 463 enumerations with every member, value and meaning | Enumeraciones con todos sus valores |
| [_INDICE-Servicios.md](_INDICE-Servicios.md) → [Servicios/](Servicios/) | 234 services + global operations (594 operations: request, parameters, body sample, return type) | Servicios y operaciones globales |
| [../Tablas SAP B1/](../Tablas%20SAP%20B1/_INDICE.md) | Database tables reference (linked from each entity's "DB tables") | Tablas de la base de datos |

## Guide chapters

| File | Topic | Tema (ES) |
|---|---|---|
| [01-Introduction-and-Getting-Started](Guia/01-Introduction-and-Getting-Started.md) | What SL is, requirements, architecture, installation topology | Qué es, requisitos, arquitectura, instalación |
| [03-01-Basics-Login-Session-Metadata](Guia/03-01-Basics-Login-Session-Metadata.md) | URL anatomy, Login/Logout, session cookies, `$metadata` (incl. annotated metadata FP 2608), service document | URL, login, sesión, metadatos |
| [03-02-CRUD-and-Actions](Guia/03-02-CRUD-and-Actions.md) | POST/GET/PATCH/PUT/DELETE, `Prefer: return-no-content`, bound and global actions, `*_Preview` | CRUD y acciones |
| [03-03-Query-Options](Guia/03-03-Query-Options.md) | `$filter`, `$select`, `$orderby`, `$top/$skip`, paging, `$count`, `$inlinecount`, `$apply` aggregate/groupby, `$crossjoin`, `QueryService_PostQuery`, `$expand` | Opciones de consulta |
| [03-04-Semantic-Layer-Views](Guia/03-04-Semantic-Layer-Views.md) | HANA Semantic Layer views (`sml.svc`) | Vistas Semantic Layer (HANA) |
| [03-05-SQL-View-Exposure](Guia/03-05-SQL-View-Exposure.md) | SQL Server views (`view.svc`, `SQLViews`) | Vistas SQL (SQL Server) |
| [03-06-Batch-Operations](Guia/03-06-Batch-Operations.md) | `$batch`, change sets, `Content-ID` | Operaciones batch |
| [03-07-Properties-Associations-Schemas](Guia/03-07-Properties-Associations-Schemas.md) | Single properties, `$value`, navigation/associations, `B1S-Schema` | Propiedades, navegación y esquemas |
| [03-08-UDF-UDT-UDO](Guia/03-08-UDF-UDT-UDO.md) | `UserFieldsMD`, `UserTablesMD`, `UserKeysMD`, `UserObjectsMD`, UDO CRUD/Cancel/Close | Campos, tablas y objetos de usuario |
| [03-09-Attachments-Streams-Images](Guia/03-09-Attachments-Streams-Images.md) | `Attachments2`, CIFS on Linux, multipart upload, `Slug`, `ItemImages`, `EmployeeImages` | Anexos e imágenes |
| [03-10-JavaScript-Extensions](Guia/03-10-JavaScript-Extensions.md) | Server-side JavaScript (V8), SDK, transactions, deployment | Extensiones JavaScript |
| [03-11-CORS-and-Ping](Guia/03-11-CORS-and-Ping.md) | CORS configuration, `/ping` API | CORS y ping |
| [04-SQL-Query](Guia/04-SQL-Query.md) | `SQLQueries` + `List`, allowlist, supported SQL, parameters, errors, permissions | Consultas SQL |
| [05-ETag-Optimistic-Concurrency](Guia/05-ETag-Optimistic-Concurrency.md) | ETag, `If-Match`, `412 Precondition Failed` | Concurrencia optimista |
| [06-Configuration-and-Logs](Guia/06-Configuration-and-Logs.md) | Service Layer Controller, `b1s.conf`, `B1S-*` headers, logs | Configuración y logs |
| [07-Webhooks](Guia/07-Webhooks.md) | Webhooks (FP 2602+): subscriptions, handshake, auth, payload, messenger, filter formulas | Webhooks |
| [08-Limitations-HA-FAQ](Guia/08-Limitations-HA-FAQ.md) | Limitations, high availability, FAQ | Limitaciones, alta disponibilidad, FAQ |
| [09-Appendix-SL-vs-DI-API](Guia/09-Appendix-SL-vs-DI-API.md) | DI API ↔ SL equivalents, naming differences | Equivalencias con la DI API |

## Quick reference

| Topic | Key facts | Resumen (ES) |
|---|---|---|
| Base URL | `https://<server>:50000/b1s/v2/` (OData v4, recommended) · `/b1s/v1/` (OData v3) | URL base |
| Login | `POST /Login {"CompanyDB","UserName","Password"}` → cookies `B1SESSION` (+ `ROUTEID`); send them on every call; default timeout 30 min | Login y cookies |
| Keys | String keys quoted `('C001')`, numeric unquoted `(22)`, composite `(Code='AK',Type=-3)` | Claves |
| Enums | Send the member name (`"CardType": "cCustomer"`) or the DB value (`"C"`) | Enums |
| Update | Prefer `PATCH`; `PUT` resets omitted fields. No PATCH support → `POST` + `X-HTTP-Method-Override: PATCH` | Actualizar |
| Paging | 20 rows by default; follow `@odata.nextLink`; `Prefer: odata.maxpagesize=n` | Paginación |
| Documents | Can't be deleted → `POST /Orders(n)/Close`, `/Cancel`, `/Reopen`; preview with `OrdersService_Preview` | Documentos |
| Copy from base document | Line fields `BaseType`, `BaseEntry`, `BaseLine` (e.g. delivery from order: `BaseType=17`) | Copiar desde documento base |
| Atomic multi-step | `$batch` change set (all-or-nothing) or JavaScript extension with `startTransaction` (max 10 ops) | Transacciones |
| Concurrency | `If-Match: <ETag>` → `412` if someone else changed it | Concurrencia |
| Line-level filtering | `POST /QueryService_PostQuery` with `$crossjoin(Orders,Orders/DocumentLines)` | Filtrar por líneas |
| Ad-hoc SQL (read-only) | `POST /SQLQueries` + `GET /SQLQueries('code')/List?param=value` (allowlisted tables only) | SQL de solo lectura |
| New UDF/UDT/UDO | Visible in SL **only after restarting Service Layer** | Reiniciar tras crear UDF/UDT/UDO |
| Per-request config | Headers `B1S-PageSize`, `B1S-CaseInsensitive`, `B1S-Schema`, `B1S-WCFCompatible`, `B1S-ReplaceCollectionsOnPatch` | Configuración por request |

## Argentina localization UDFs kept (`U_B1SYS_*`)

| Where | Fields | Dónde (ES) |
|---|---|---|
| `BusinessPartner` | `U_B1SYS_VATCtg` (condición IVA), `U_B1SYS_FiscIdType` (tipo de documento), `U_B1SYS_GrsIncCtg` / `U_B1SYS_GrsIncId` (Ingresos Brutos), `U_B1SYS_IncTaxCtg` (Ganancias), `U_B1SYS_MonoCtg` / `U_B1SYS_MonoAct` (monotributo), `U_B1SYS_Employer`, `U_B1SYS_ReproWebSta`, `U_B1SYS_ShareFromO` | Socios de negocios |
| `Document` (all marketing documents) and `StockTransfer` | `U_B1SYS_CAI`, `U_B1SYS_CAI_DATE`, `U_B1SYS_ECM2_LINK` | Documentos y transferencias |
| `Item` | `U_B1SYS_MTXCode` (unidad de medida AFIP) | Artículos |
| `Warehouse` | `U_B1SYS_COT_code` (COT) | Almacenes |
| `AddressExtension`, `StockTransferTaxExtension` | `U_B1SYS_IncotermsTxt`, `U_B1SYS_TrailerId` | Extensiones de dirección/impuestos |
| `EDFEntry`, `EcmAction` (electronic documents) | `U_B1SYS_FCE_*` (FCE MiPyME: estado de aceptación, CBU, folio, punto de venta, importes, motivos de rechazo…), `U_B1SYS_XMLAmount`, `U_B1SYS_SendDateINTM` | Documentos electrónicos / FCE |
| `WTDCode` (entity set `WitholdingTaxDefinition`), `WTDBP`, `WTDEffectiveDate` | `U_B1SYS_WhtType`, `U_B1SYS_JurisFrom/To`, `U_B1SYS_AccumGroup`, `U_B1SYS_ResultMin`, `U_B1SYS_WTCSeries`, `U_B1SYS_ReproWeb`, `U_B1SYS_HighRisk`, `U_B1SYS_CheckSetByPd`, `U_B1SYS_ExemptID`, `U_B1SYS_FixedAmount`, `U_B1SYS_NonDedAcc`, … | Definición de retenciones/percepciones |

Excluded from the source metadata: 21 user entity sets/UDOs (`U_GNA_*`, `U_INT_LOG`, `COLORES`, `CURVAS`, `DISCIPLINA`, `EDAD`, `GENERO`, `PARAMVALID`, `TALLES`, `TIPOPROD`, `Temporada`), 22 auxiliary types (their `…Params`, `SEI_PARAMVALID_D`), 66 user UDF properties on standard objects (e.g. `U_GNA_*`, `U_TipoFCE`, `U_RefComFCE`, `U_FechaFCE`, `U_MotivoNCE`, `U_NroCompEsp(ec)`, `U_ProvEvent(ual)`, `U_CanMisMonExt`, `U_NIF`) and the UDO action `Cancel(Temporada)`.

## Notes on accuracy

- Structural data (entity sets, keys, properties, types, nullability, navigation, actions, parameters, enum values) comes **verbatim from the metadata**.
- *Description (EN)* columns are derived from the technical names; *Descripción (ES)* columns are translations using standard SAP Business One Spanish (Latin America) terms. The metadata itself has no descriptions.
- *DB tables* per entity set were added only when the mapping is certain and were checked against the `Tablas SAP B1` reference. If the annotated metadata of FP 2608+ (`$metadata?scope=entityset&annotation=labelWithTable`) is available, it gives the official mapping.
- Entity docs use OData v4 URLs (`/b1s/v2`). For OData v3, replace with `/b1s/v1` (some annotations differ, e.g. `odata.nextLink` vs `@odata.nextLink`).
