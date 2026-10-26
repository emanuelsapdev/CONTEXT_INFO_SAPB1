# CycleCountDeterminationSetup — Configuración de recuento cíclico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CycleCountDeterminationSetup`
- **Descripción (ES):** Configuración de recuento cíclico
- **Description (EN):** Cycle Count Determination Setup

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 2 | `Entry` | Edm.Int32 | Yes | Entry | Entrada |
| 3 | `CycleCode` | Edm.Int32 | Yes | Cycle Code | Código de ciclo |
| 4 | `Alert` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Alert | Alerta |
| 5 | `DestinationUser` | Edm.Int32 | Yes | Destination User | Usuario destinatario |
| 6 | `NextCountingDate` | Edm.DateTimeOffset | Yes | Next Counting Date | Siguiente fecha de recuento |
| 7 | `Time` | Edm.TimeOfDay | Yes | Time | Hora |
| 8 | `ExcludeItemsWithZeroQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exclude Items With Zero Quantity | Excluir artículos con cantidad cero |
| 9 | `ChangeExistingItems` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Change Existing Items | Modificar artículos existentes |

## Used by (properties)

- [CycleCountDetermination](../Entidades/CycleCountDeterminations.md).`CycleCountDeterminationSetupCollection`
