# EWBTransporters — Transportistas EWB

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EWBTransporters`
- **Descripción (ES):** Transportistas EWB
- **Entity type:** `EWBTransporter`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EWBTransporters?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EWBTransporters/$count` | Contar |
| Get by key | `GET /b1s/v2/EWBTransporters(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EWBTransporters` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EWBTransporters(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EWBTransporters(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EWBTransporters(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `TransporterCode` | Edm.String | Yes | Transporter Code | Código del transportista |
| 3 | `TransporterName` | Edm.String | Yes | Transporter Name | Nombre del transportista |
| 4 | `TransporterID` | Edm.String | Yes | Transporter ID | ID del transportista |
| 5 | `EWBTransporter_Lines` | Collection([EWBTransporter_Line](../Tipos-Complejos/EWBTransporter_Line.md)) | Yes | EWB Transporter Lines | Líneas de transportista EWB |

## Navigation properties (1)

Use `GET /b1s/v2/EWBTransporters(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
