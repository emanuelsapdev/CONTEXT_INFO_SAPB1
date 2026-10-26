# TrackingNotes — Notas de seguimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TrackingNotes`
- **Descripción (ES):** Notas de seguimiento
- **Entity type:** `TrackingNote`
- **Key:** `TrackingNoteNumber` (Edm.Int32)
- **DB tables (main / lines):** [OTCN](../../Tablas%20SAP%20B1/OTCN.md), [TCN1](../../Tablas%20SAP%20B1/TCN1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TrackingNotes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TrackingNotes/$count` | Contar |
| Get by key | `GET /b1s/v2/TrackingNotes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/TrackingNotes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TrackingNotes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TrackingNotes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/TrackingNotes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrackingNoteNumber` 🔑 | Edm.Int32 | No | Tracking Note Number | Número de la nota de seguimiento |
| 2 | `CCDNumber` | Edm.String | Yes | CCD Number | Número de declaración aduanera de carga |
| 3 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 4 | `CustomsTerminal` | Edm.String | Yes | Customs Terminal | Terminal aduanera |
| 5 | `CountryOfOrigin` | Edm.String | Yes | Country Of Origin | País de origen |
| 6 | `IsDirectImport` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Direct Import | Es importación directa |
| 7 | `TrackingNoteItemCollection` | Collection([TrackingNoteItem](../Tipos-Complejos/TrackingNoteItem.md)) | Yes | Tracking Note Item Collection | Colección de artículos de la nota de seguimiento |
| 8 | `TrackingNoteBrokerCollection` | Collection([TrackingNoteBroker](../Tipos-Complejos/TrackingNoteBroker.md)) | Yes | Tracking Note Broker Collection | Colección de agentes de la nota de seguimiento |
