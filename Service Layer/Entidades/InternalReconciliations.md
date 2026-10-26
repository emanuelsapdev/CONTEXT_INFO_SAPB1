# InternalReconciliations — Conciliaciones internas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `InternalReconciliations`
- **Descripción (ES):** Conciliaciones internas
- **Entity type:** `InternalReconciliation`
- **Key:** `ReconNum` (Edm.Int32)
- **DB tables (main / lines):** [OITR](../../Tablas%20SAP%20B1/OITR.md), [ITR1](../../Tablas%20SAP%20B1/ITR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/InternalReconciliations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/InternalReconciliations/$count` | Contar |
| Get by key | `GET /b1s/v2/InternalReconciliations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/InternalReconciliations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/InternalReconciliations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/InternalReconciliations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/InternalReconciliations(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/InternalReconciliations(1)/Cancel` | Cancelar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReconNum` 🔑 | Edm.Int32 | No | Recon Number | Número de conciliación |
| 2 | `ReconDate` | Edm.DateTimeOffset | Yes | Recon Date | Fecha de conciliación |
| 3 | `CardOrAccount` | [CardOrAccountEnum](../Enums/CardOrAccountEnum.md) | Yes | Card Or Account | Socio de negocios o cuenta |
| 4 | `ReconType` | [ReconTypeEnum](../Enums/ReconTypeEnum.md) | Yes | Recon Type | Tipo de conciliación |
| 5 | `Total` | Edm.Double | Yes | Total | Total |
| 6 | `CancelAbs` | Edm.Int32 | Yes | Cancel Abs | Entrada de cancelación |
| 7 | `InternalReconciliationRows` | Collection([InternalReconciliationRow](../Tipos-Complejos/InternalReconciliationRow.md)) | Yes | Internal Reconciliation Rows | Líneas de la conciliación interna |
| 8 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |

## Bound actions (1)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/InternalReconciliations(1)/Cancel`


## Service operations that use this type

- [`InternalReconciliationsService_RequestApproveCancellation`](../Servicios/InternalReconciliationsService.md#internalreconciliationsservice_requestapprovecancellation)
