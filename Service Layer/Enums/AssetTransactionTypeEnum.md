# AssetTransactionTypeEnum — Tipo de transacción de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AssetTransactionTypeEnum`
- **Descripción (ES):** Tipo de transacción de activo
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `att_BeginningOfYear` | 0 | Beginning Of Year | Inicio del año |
| `att_Acquistion` | 1 | Acquistion | Adquisición |
| `att_Retirement` | 2 | Retirement | Baja |
| `att_Transfer` | 3 | Transfer | Transferencia |
| `att_WriteUp` | 4 | Write Up | Revalorización |
| `att_OrdinaryDepreciation` | 5 | Ordinary Depreciation | Amortización ordinaria |
| `att_UplannedDepreciation` | 6 | Uplanned Depreciation | Amortización no planificada |
| `att_SpecialDepreciation` | 7 | Special Depreciation | Amortización especial |
| `att_EndOfYear` | 8 | End Of Year | Fin del año |

## Used by (1 properties)

- [FixedAssetValues](../Tipos-Complejos/FixedAssetValues.md).`TransactionType`
