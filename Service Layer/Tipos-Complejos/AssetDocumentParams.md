# AssetDocumentParams — Parámetros de baja de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetDocumentParams`
- **Descripción (ES):** Parámetros de baja de activos
- **Description (EN):** Asset Document Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `CancellationOption` | [ClosingOptionEnum](../Enums/ClosingOptionEnum.md) | Yes | Cancellation Option | Opción de cancelación |
| 3 | `CancellationDate` | Edm.DateTimeOffset | Yes | Cancellation Date | Fecha de cancelación |

## Used by (service operations)

- [`AssetCapitalizationCreditMemoService_Cancel`](../Servicios/AssetCapitalizationCreditMemoService.md#assetcapitalizationcreditmemoservice_cancel)
- [`AssetCapitalizationCreditMemoService_GetList`](../Servicios/AssetCapitalizationCreditMemoService.md#assetcapitalizationcreditmemoservice_getlist)
- [`AssetCapitalizationService_Cancel`](../Servicios/AssetCapitalizationService.md#assetcapitalizationservice_cancel)
- [`AssetCapitalizationService_GetList`](../Servicios/AssetCapitalizationService.md#assetcapitalizationservice_getlist)
- [`AssetManualDepreciationService_Cancel`](../Servicios/AssetManualDepreciationService.md#assetmanualdepreciationservice_cancel)
- [`AssetManualDepreciationService_GetList`](../Servicios/AssetManualDepreciationService.md#assetmanualdepreciationservice_getlist)
- [`AssetRetirementService_Cancel`](../Servicios/AssetRetirementService.md#assetretirementservice_cancel)
- [`AssetRetirementService_GetList`](../Servicios/AssetRetirementService.md#assetretirementservice_getlist)
- [`AssetTransferService_Cancel`](../Servicios/AssetTransferService.md#assettransferservice_cancel)
- [`AssetTransferService_GetList`](../Servicios/AssetTransferService.md#assettransferservice_getlist)
