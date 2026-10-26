# AssetDocumentTypeEnum — Tipo de documento de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AssetDocumentTypeEnum`
- **Descripción (ES):** Tipo de documento de activo
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `adtOrdinaryDepreciation` | 0 | Ordinary Depreciation | Amortización ordinaria |
| `adtUnplannedDepreciation` | 1 | Unplanned Depreciation | Amortización no planificada |
| `adtSpecialDepreciation` | 2 | Special Depreciation | Amortización especial |
| `adtAppreciation` | 3 | Appreciation | Revalorización |
| `adtAssetTransfer` | 4 | Asset Transfer | Transferencia de activo |
| `adtSales` | 5 | Sales | Venta |
| `adtScrapping` | 6 | Scrapping | Desguace |
| `adtAssetClassTransfer` | 7 | Asset Class Transfer | Transferencia de clase de activo |

## Used by (1 properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`DocumentType`
