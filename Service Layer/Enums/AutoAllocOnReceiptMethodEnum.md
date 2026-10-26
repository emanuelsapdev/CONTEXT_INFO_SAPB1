# AutoAllocOnReceiptMethodEnum — Método de asignación automática en recepción

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AutoAllocOnReceiptMethodEnum`
- **Descripción (ES):** Método de asignación automática en recepción
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aaormDefaultBin` | 0 | Default Bin | Ubicación predeterminada |
| `aaormItemCurrentAndHistoricalBins` | 1 | Item Current And Historical Bins | Ubicaciones actuales e históricas del artículo |
| `aaormItemCurrentBins` | 2 | Item Current Bins | Ubicaciones actuales del artículo |
| `aaormLastBinReceivedItem` | 3 | Last Bin Received Item | Última ubicación en que se recibió el artículo |

## Used by (1 properties)

- [Warehouse](../Entidades/Warehouses.md).`AutoAllocOnReceipt`
