# GeneratedAsset — Activos generados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `GeneratedAsset`
- **Descripción (ES):** Activos generados
- **Description (EN):** Generated Asset

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 4 | `AssetCode` | Edm.String | Yes | Asset Code | Código de activo |
| 5 | `Status` | [GeneratedAssetStatusEnum](../Enums/GeneratedAssetStatusEnum.md) | Yes | Status | Estado |
| 6 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 7 | `SerialNumber` | Edm.String | Yes | Serial Number | Número de serie |
| 8 | `amount` | Edm.Double | Yes | Amount | Importe |
| 9 | `amountSC` | Edm.Double | Yes | Amount SC (system currency) | Importe (moneda del sistema) |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`GeneratedAssets`
