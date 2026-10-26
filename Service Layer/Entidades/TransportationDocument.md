# TransportationDocument — Documentos de transporte

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TransportationDocument`
- **Descripción (ES):** Documentos de transporte
- **Entity type:** `TransportationDocumentData`
- **Key:** `TranspDocNumber` (Edm.Int32)
- **DB tables (main / lines):** [OTRO](../../Tablas%20SAP%20B1/OTRO.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 20 · **Navigation properties:** 0 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TransportationDocument?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TransportationDocument/$count` | Contar |
| Get by key | `GET /b1s/v2/TransportationDocument(1)` | Obtener por clave |
| Create | `POST /b1s/v2/TransportationDocument` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TransportationDocument(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TransportationDocument(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/TransportationDocument(1)` (only if the B1 object allows removal) | Borrar |
| Action `CancelTransportationDocument` | `POST /b1s/v2/TransportationDocument(1)/CancelTransportationDocument` | Cancelar documento de transporte |

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TranspDocNumber` 🔑 | Edm.Int32 | No | Transp Document Number | Número de documento de transporte |
| 2 | `NextNumber` | Edm.Int32 | Yes | Next Number | Siguiente número |
| 3 | `PostDate` | Edm.DateTimeOffset | Yes | Post Date | Fecha de contabilización |
| 4 | `ElDocGenType` | [ElectronicDocGenTypeEnum](../Enums/ElectronicDocGenTypeEnum.md) | Yes | El Document Gen Type | Tipo de generación del documento electrónico |
| 5 | `ElDocExportFormat` | Edm.Int32 | Yes | El Document Export Format | Formato de exportación del documento electrónico |
| 6 | `TransportationNumber` | Edm.String | Yes | Transportation Number | Número de transporte |
| 7 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |
| 8 | `VehicleID` | Edm.String | Yes | Vehicle ID | ID del vehículo |
| 9 | `TrailerID` | Edm.String | Yes | Trailer ID | ID del remolque |
| 10 | `CarrierCode` | Edm.String | Yes | Carrier Code | Código del transportista |
| 11 | `IssueGate` | Edm.Int32 | Yes | Issue Gate | Puerta de salida |
| 12 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 13 | `Canceled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Canceled | Cancelado |
| 14 | `Weight` | Edm.Double | Yes | Weight | Peso |
| 15 | `WeightUnit` | Edm.Int32 | Yes | Weight Unit | Unidad de peso |
| 16 | `TransportedTotalLC` | Edm.Double | Yes | Transported Total LC (local currency) | Total transportado (moneda local) |
| 17 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 18 | `COTCode` | Edm.String | Yes | COT Code | Código COT (Argentina) |
| 19 | `TransportationDocumentLineDataCollection` | Collection([TransportationDocumentLineData](../Tipos-Complejos/TransportationDocumentLineData.md)) | Yes | Transportation Document Line Data Collection | Líneas del documento de transporte |
| 20 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |

## Bound actions (1)

### CancelTransportationDocument

- **Descripción (ES):** Cancelar documento de transporte
- **Request:** `POST /b1s/v2/TransportationDocument(1)/CancelTransportationDocument`

