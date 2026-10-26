# BoDocWhsAutoIssueMethod — Método de emisión automática desde ubicaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDocWhsAutoIssueMethod`
- **Descripción (ES):** Método de emisión automática desde ubicaciones
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `whsBinSingleChoiceOnly` | 0 | Bin Single Choice Only | Solo opción única |
| `whsBinBinCodeOrder` | 1 | Bin Bin Code Order | Orden por código de ubicación |
| `whsBinAltSortCodeOrder` | 2 | Bin Alt Sort Code Order | Orden por código de clasificación alternativo |
| `whsBinQtyDescendingOrder` | 3 | Bin Quantity Descending Order | Cantidad descendente |
| `whsBinQtyAscendingOrder` | 4 | Bin Quantity Ascending Order | Cantidad ascendente |
| `whsBinFIFO` | 5 | Bin FIFO | FIFO |
| `whsBinLIFO` | 6 | Bin LIFO | LIFO |
| `whsBinSingleBinPreferred` | 7 | Bin Single Bin Preferred | Ubicación única preferida |

## Used by (1 properties)

- [Warehouse](../Entidades/Warehouses.md).`AutoAllocOnIssue`
