# InternalReconciliationOpenTrans — Transacciones abiertas para conciliación interna

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InternalReconciliationOpenTrans`
- **Descripción (ES):** Transacciones abiertas para conciliación interna
- **Description (EN):** Internal Reconciliation Open Trans

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReconDate` | Edm.DateTimeOffset | Yes | Recon Date | Fecha de conciliación |
| 2 | `CardOrAccount` | [CardOrAccountEnum](../Enums/CardOrAccountEnum.md) | Yes | Card Or Account | Socio de negocios o cuenta |
| 3 | `BPLId` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 4 | `InternalReconciliationOpenTransRows` | Collection([InternalReconciliationOpenTransRow](../Tipos-Complejos/InternalReconciliationOpenTransRow.md)) | Yes | Internal Reconciliation Open Trans Rows | Líneas de transacciones abiertas de la conciliación interna |
| 5 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |

## Used by (service operations)

- [`InternalReconciliationsService_GetOpenTransactions`](../Servicios/InternalReconciliationsService.md#internalreconciliationsservice_getopentransactions)
