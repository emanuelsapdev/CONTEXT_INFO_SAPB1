# IndividualCounter — Contadores individuales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `IndividualCounter`
- **Descripción (ES):** Contadores individuales
- **Description (EN):** Individual Counter

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `CounterID` | Edm.Int32 | Yes | Counter ID | ID del contador |
| 3 | `CounterType` | [CounterTypeEnum](../Enums/CounterTypeEnum.md) | Yes | Counter Type | Tipo de contador |
| 4 | `CounterName` | Edm.String | Yes | Counter Name | Nombre del contador |
| 5 | `CounterNumber` | Edm.Int32 | Yes | Counter Number | Número del contador |
| 6 | `CounterVisualOrder` | Edm.Int32 | Yes | Counter Visual Order | Orden visual del contador |

## Used by (properties)

- [InventoryCounting](../Entidades/InventoryCountings.md).`IndividualCounters`
