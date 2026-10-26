# ElectronicDocuments — Documentos electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ElectronicDocuments`
- **Descripción (ES):** Documentos electrónicos
- **Entity type:** `EDFProtocol`
- **Key:** `Code` (ElectronicDocProtocolCodeStrEnum)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ElectronicDocuments?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ElectronicDocuments/$count` | Contar |
| Get by key | `GET /b1s/v2/ElectronicDocuments('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ElectronicDocuments` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ElectronicDocuments('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ElectronicDocuments('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ElectronicDocuments('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |

## Service operations that use this type

- [`ElectronicDocumentService_GetProtocols`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getprotocols)
