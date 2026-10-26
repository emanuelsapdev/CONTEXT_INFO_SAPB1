# IssuePrimarilyByEnum — Emitir principalmente por

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `IssuePrimarilyByEnum`
- **Descripción (ES):** Emitir principalmente por
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ipbSerialAndBatchNumbers` | 0 | Serial And Batch Numbers | Números de serie y lote |
| `ipbBinLocations` | 1 | Bin Locations | Ubicaciones |

## Used by (2 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`IssuePrimarilyBy`
- [Item](../Entidades/Items.md).`IssuePrimarilyBy`
