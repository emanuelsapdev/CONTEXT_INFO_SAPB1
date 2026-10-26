# InternalReconciliationOpenTransParams — Parámetros de transacciones abiertas para conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InternalReconciliationOpenTransParams`
- **Descripción (ES):** Parámetros de transacciones abiertas para conciliación
- **Description (EN):** Internal Reconciliation Open Trans Parameters

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReconDate` | Edm.DateTimeOffset | Yes | Recon Date | Fecha de conciliación |
| 2 | `CardOrAccount` | [CardOrAccountEnum](../Enums/CardOrAccountEnum.md) | Yes | Card Or Account | Socio de negocios o cuenta |
| 3 | `AccountNo` | Edm.String | Yes | Account Number | Número de cuenta |
| 4 | `DateType` | [ReconSelectDateTypeEnum](../Enums/ReconSelectDateTypeEnum.md) | Yes | Date Type | Tipo de fecha |
| 5 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 6 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 7 | `InternalReconciliationBPs` | Collection([InternalReconciliationBP](../Tipos-Complejos/InternalReconciliationBP.md)) | Yes | Internal Reconciliation B Ps | Socios de negocios de la conciliación interna |

## Used by (service operations)

- [`InternalReconciliationsService_GetOpenTransactions`](../Servicios/InternalReconciliationsService.md#internalreconciliationsservice_getopentransactions)
